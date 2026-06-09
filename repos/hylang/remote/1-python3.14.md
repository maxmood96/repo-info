## `hylang:1-python3.14`

```console
$ docker pull hylang@sha256:af8737fe5c7afeaeb517680011fabfa78f0644a34bf9de840be4135b9bf2aa33
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
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `hylang:1-python3.14` - linux; amd64

```console
$ docker pull hylang@sha256:9cc6e4126867002a2ab06b4035df7ec985614dc561af42731c5fc91adbb3065f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49113764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bfb3053887a6715de8851803099ac8e3c1767ef9d7599f2320e875dec9962f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:39:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:39:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:39:58 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 19 May 2026 23:39:58 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Tue, 19 May 2026 23:47:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:47:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:47:22 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:44:36 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:36 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf23796d1e8ae9b05eee16765fcf83722d2c0fdda9a27d09d25610a7ed9a0a0`  
		Last Modified: Tue, 19 May 2026 23:47:30 GMT  
		Size: 1.3 MB (1293322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99500e0cbdb98ad73639044dd5113029e40bdab38b4ea5fe594532bb79cbe57f`  
		Last Modified: Tue, 19 May 2026 23:47:30 GMT  
		Size: 12.3 MB (12328506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83fa8e4dee39a3198704bc54184a177c88e40a821cb24d55437776d8cfdf85a`  
		Last Modified: Tue, 19 May 2026 23:47:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbe9a49f0ab8da105b5629edf1ea150a93a35c77d77a7803dda8cc140764edb`  
		Last Modified: Mon, 08 Jun 2026 22:44:42 GMT  
		Size: 5.7 MB (5711761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14` - unknown; unknown

```console
$ docker pull hylang@sha256:dd6ca92a71d92c57e124c3b0fcf4f6ed02a6476f9e004a26a97130fc64ec577a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f70ef22dd5afb01875d7a8bacd966b7d1ff5d3a042afde562fd90b929336e0`

```dockerfile
```

-	Layers:
	-	`sha256:bd41a5859867e0711290dc10545fa41d668a02193af056e71a028dc69492f51c`  
		Last Modified: Mon, 08 Jun 2026 22:44:42 GMT  
		Size: 2.2 MB (2156691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de523facc8c0cb3d3c5b9707381fed5d5086a200fc3ac013ce6554bb4018424a`  
		Last Modified: Mon, 08 Jun 2026 22:44:42 GMT  
		Size: 11.6 KB (11640 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14` - linux; arm variant v5

```console
$ docker pull hylang@sha256:d0f1615403577bfd4733c4215f4cddc67f8c6d964157636f8738a7aebd3a0de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46945443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd30c1a07285a7f2d5e7e4545cad8068ee4db26ae665c5354db1564f5e350677`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:12:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:12:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:12:57 GMT
ENV PYTHON_VERSION=3.14.5
# Wed, 20 May 2026 00:12:57 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Wed, 20 May 2026 00:23:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 00:23:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 00:23:20 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:46:23 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:46:23 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:46:23 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:46:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b91efc1ff7d19d3b99581223828a3af11c46d80ce3d0ee91b8c584c5a3fe9d2`  
		Last Modified: Wed, 20 May 2026 00:23:28 GMT  
		Size: 1.3 MB (1276395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bf4741d05f20a902893cfa7fa9f5402d558e1dde7c850289c5fbbffbbcedaa`  
		Last Modified: Wed, 20 May 2026 00:23:28 GMT  
		Size: 12.0 MB (12002904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8af657bf13e050d4b198772ca600218efd6f95883bf1c5517fa5dcb198e21`  
		Last Modified: Wed, 20 May 2026 00:23:28 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af75d2597ea58099af34fe090e75248cae691f9d34c1fd41670bc950e8f58286`  
		Last Modified: Mon, 08 Jun 2026 22:46:30 GMT  
		Size: 5.7 MB (5712026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14` - unknown; unknown

```console
$ docker pull hylang@sha256:6615dc5dd5a606566e3cae362516649b37819ab974a5b19d2ec70af70a558e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9337ac8dd3163b63514c5280cfc2d08160600816cd395e98c659fb4a7431ff3b`

```dockerfile
```

-	Layers:
	-	`sha256:855ad3ebfd4ce5de5fd6b2c44941cf3d154fb97ea9c5f852452a35992a6e1561`  
		Last Modified: Mon, 08 Jun 2026 22:46:30 GMT  
		Size: 2.2 MB (2159756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afbe5956269b1ce5c78197f302c75a8a594c48dbe425e849a976da4f241d6f03`  
		Last Modified: Mon, 08 Jun 2026 22:46:30 GMT  
		Size: 11.8 KB (11819 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14` - linux; arm variant v7

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

### `hylang:1-python3.14` - unknown; unknown

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

### `hylang:1-python3.14` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:742979cb57f889b02914faa70cfd262ebef91ee5f63b2e00ec7d0ac406a8b2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49367791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a04742b16fe78318d192b934d957b242445cc48c8c7d5de49cde08a49216d6`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:44:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:44:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:44:05 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 19 May 2026 23:44:05 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Tue, 19 May 2026 23:51:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:51:45 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:51:45 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:44:40 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:40 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abbbe345e12f276b412fbc184241f97020ca6ed369442fc7196dbba6f79d3c8`  
		Last Modified: Tue, 19 May 2026 23:51:54 GMT  
		Size: 1.3 MB (1274145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba910efc9bbe1878426db62fb20bcff1cac62f76ea92a660b41baa9c4360f42`  
		Last Modified: Tue, 19 May 2026 23:51:54 GMT  
		Size: 12.2 MB (12239567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d251662416b5e9abe43cd4e0dbe473cbfab2ddf22666cf9be4ee12ddae62938e`  
		Last Modified: Tue, 19 May 2026 23:51:54 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b278357e2d85cc033eab6cc52979af232ea7d660bee07b3565bafd0d14c50fa7`  
		Last Modified: Mon, 08 Jun 2026 22:44:47 GMT  
		Size: 5.7 MB (5711910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14` - unknown; unknown

```console
$ docker pull hylang@sha256:def1f4ae9fbe10a0b469ae06fbfba10ea135ee07dd1f85764661bf90584d3d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca6410411b95b537e6c0d55538de0bc063bcfd9440da4176718ba729e8894bb`

```dockerfile
```

-	Layers:
	-	`sha256:4e2e63958c70680f25432a30e5329279fa8982dd43a2223cd520c2549ac49e42`  
		Last Modified: Mon, 08 Jun 2026 22:44:47 GMT  
		Size: 2.2 MB (2157093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece6d1c7194294d7efe48a9410489de999b3c511d73c3fff5ed5a17e83599bb9`  
		Last Modified: Mon, 08 Jun 2026 22:44:46 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14` - linux; 386

```console
$ docker pull hylang@sha256:e247d7fc543e3a96537f8f2bb2d67285a153bdf215b4c74393c7bdec7e13efd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50766727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3169c7699836d3380c0a6d5e16f300cfa0d8902124037535a5ddeaf63be96b4a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:35:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:35:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:35:31 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 19 May 2026 23:35:31 GMT
ENV PYTHON_SHA256=7e32597b99e5d9a39abed35de4693fa169df3e5850d4c334337ffd6a19a36db6
# Tue, 19 May 2026 23:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:54:12 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:54:12 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:46:10 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:46:10 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:46:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:46:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6393294242322f7c57e4290dfb0d21aec90d0376bbbd8538d4d6d813fcc180b`  
		Last Modified: Tue, 19 May 2026 23:54:19 GMT  
		Size: 1.3 MB (1297811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f492bdd7b689bf8bd961fc5b194e03f905b39e5f4693695c24507b3aad8765`  
		Last Modified: Tue, 19 May 2026 23:54:20 GMT  
		Size: 12.5 MB (12461189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1af5369e2a6c56544505227c6bc44f2a1be47b807f0236cb14bafb656e519d`  
		Last Modified: Tue, 19 May 2026 23:54:20 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec866ce2bd5be589caf182c6b35729ab66f03648086c38bd67bf537e53aeef9`  
		Last Modified: Mon, 08 Jun 2026 22:46:17 GMT  
		Size: 5.7 MB (5712142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14` - unknown; unknown

```console
$ docker pull hylang@sha256:7d008c57ebc4321420eb7af4727ec2bfe375e3945ca4236acb7e3e9d2232c396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5d3ab60e3dcff50ee98b3a0cc3c7ad48a958fa632c4ea2e8c00fccea7f0499`

```dockerfile
```

-	Layers:
	-	`sha256:cdb8762903814cc69aeeedfd2bf05626390d006ac8d1e480044c31b13fab529b`  
		Last Modified: Mon, 08 Jun 2026 22:46:16 GMT  
		Size: 2.2 MB (2153812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e6c4c95c5edbb5ca7d7dcd670c5111b8fc430b50f41b927fcc116db53c52044`  
		Last Modified: Mon, 08 Jun 2026 22:46:16 GMT  
		Size: 11.6 KB (11551 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14` - linux; ppc64le

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

### `hylang:1-python3.14` - unknown; unknown

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

### `hylang:1-python3.14` - linux; riscv64

```console
$ docker pull hylang@sha256:cf0562f078702df3536dac5fbe4d1f655ee7fe2854b4ce0492a1b7db550d34b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47585941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb2e26b31334e0d7feb55684986c824b1a88f5bceb696e6658b2145ba58282a`
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
# Thu, 28 May 2026 11:56:13 GMT
ENV HY_VERSION=1.3.0
# Thu, 28 May 2026 11:56:13 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 28 May 2026 11:56:13 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 28 May 2026 11:56:13 GMT
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
	-	`sha256:61c4d6bb0ae436436795de355ccc274023109534583f50afa31e1153ad04d254`  
		Last Modified: Thu, 28 May 2026 11:57:13 GMT  
		Size: 5.7 MB (5708762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14` - unknown; unknown

```console
$ docker pull hylang@sha256:3307182f65ac80714482b4acfed1cf6ec5d72ea102bcac088c8f8faf92a8093d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2162459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89ee1bea34f43ca48523f6bfda4f15f82c5055ae858bf92be88cf32390dd062`

```dockerfile
```

-	Layers:
	-	`sha256:53277bae91b5ec407cc234dceddec815fd298f450629411172702a9eb4c828dc`  
		Last Modified: Thu, 28 May 2026 11:57:13 GMT  
		Size: 2.2 MB (2150701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410312b2d78cd9f706b7b1ff81d86624c4e1931552cf83bcd0ea0bac75ee9718`  
		Last Modified: Thu, 28 May 2026 11:57:12 GMT  
		Size: 11.8 KB (11758 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14` - linux; s390x

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

### `hylang:1-python3.14` - unknown; unknown

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

### `hylang:1-python3.14` - windows version 10.0.26100.32860; amd64

```console
$ docker pull hylang@sha256:62ad48338a09cb7bcfde36fea74a45740cc34fe1e067caa1583e99d39da64e57
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2275802462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d8959603723c450c81071a0d264e00d725007d8a59af6a2aff4df84b29090e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:50:01 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 23:50:01 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 12 May 2026 23:50:02 GMT
ENV PYTHON_SHA256=f9c09f5ed6f796fd1a8bc5ddfa41715a494b453c4781f0e35d5077cf9fa58f6d
# Tue, 12 May 2026 23:50:43 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:50:44 GMT
CMD ["python"]
# Mon, 08 Jun 2026 22:47:22 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:47:24 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:48:52 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 08 Jun 2026 22:48:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d188d7f4a5421b58c277ec337ae635de99e29dcb259e15d0521f9f034b9389`  
		Last Modified: Tue, 12 May 2026 23:40:52 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c855b0a869238548e35027126893ffdaca30a464fd624c1620934f52c0959ecd`  
		Last Modified: Tue, 12 May 2026 23:50:49 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92122d749a5d51e526ebf6aada6f98e9e35c40733efb71ccf2a229b20c34bcb3`  
		Last Modified: Tue, 12 May 2026 23:50:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08824b384a0da70df6c9f9f748a7aefe5bdb0b9cbbc2c1618e24036a8c546b95`  
		Last Modified: Tue, 12 May 2026 23:50:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb50e2e31ecbae4894b157e17cb692176f5a3d79a0bf9346ecfb3362426195b`  
		Last Modified: Tue, 12 May 2026 23:50:55 GMT  
		Size: 61.3 MB (61338866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e53701d2b2b04d99f34efdb0a69c516cf8fcfc08f12203223dab1b275ca746`  
		Last Modified: Tue, 12 May 2026 23:50:49 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d26c4e7c3de1bb81be3ae11089fe493f4c27a90c9d40d259712a06440c36c8`  
		Last Modified: Mon, 08 Jun 2026 22:48:57 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374b8ebfe472a0a275ed9e6563d0b4e8c368a2ffa36beec0818a17bb01f8e053`  
		Last Modified: Mon, 08 Jun 2026 22:48:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d583b71c71def2c5af3954c3c3ee00531373342bbab32e4b8d4a8b66978436`  
		Last Modified: Mon, 08 Jun 2026 22:48:58 GMT  
		Size: 8.5 MB (8511251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c057d42e067336e59eeb234fde744eca08b3ec151b4a43b1d8c589d20c07ac19`  
		Last Modified: Mon, 08 Jun 2026 22:48:57 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-python3.14` - windows version 10.0.20348.5139; amd64

```console
$ docker pull hylang@sha256:facb9281051e85d0afd72abb131dddd78cfa26a0b6a26adb0c35df12c52dc02e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2192804559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490ed5867399b262fb3ee0c446e1c1543488375555afba0470a44e7d80ef8587`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:58:09 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 23:58:10 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 12 May 2026 23:58:11 GMT
ENV PYTHON_SHA256=f9c09f5ed6f796fd1a8bc5ddfa41715a494b453c4781f0e35d5077cf9fa58f6d
# Tue, 12 May 2026 23:58:51 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:58:52 GMT
CMD ["python"]
# Mon, 08 Jun 2026 22:50:20 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:50:21 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:51:08 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 08 Jun 2026 22:51:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cbb80a80947ff97fb5674c26478afa4331c7d4b2fefabd1ea650765bffae78`  
		Last Modified: Tue, 12 May 2026 23:40:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7f3cfa06a6dfb39cc22416a3fe6eff4b710bfeeccf05db45d77158ff23cf7b`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91ad01b1d407414ae266c6d5f8d9c0bb0b2689fe371c38a7571438ad85c0e7f`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74178a30e0303c0c21ed95e5ff390e5b58a1a755bd7d53d4167832a08c74400e`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c55dd5cfe2037fd17b90af958774b3cbfbd7147faa9264d71df2de5ca55808f`  
		Last Modified: Tue, 12 May 2026 23:59:02 GMT  
		Size: 61.7 MB (61678797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114d0893892b1275f89469f1046c4d8eb67d669829d0ed2b72970a4b73e53803`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5edde93fa4e79c267ee4299f8419a728124b6156316f3dad5594a086004017`  
		Last Modified: Mon, 08 Jun 2026 22:51:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f4b16880abc3d16155165272e7958f06746e5e640781273d1d428ece67c64b`  
		Last Modified: Mon, 08 Jun 2026 22:51:14 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c34534b63b359b6d91ecb88088a63c1ae1219ac733ea723805beba17d7978d`  
		Last Modified: Mon, 08 Jun 2026 22:51:16 GMT  
		Size: 8.7 MB (8694613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fcbc6c6c27c29c440d81acf7f685d61818bef52b8de9d11008797c65e27d682`  
		Last Modified: Mon, 08 Jun 2026 22:51:14 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
