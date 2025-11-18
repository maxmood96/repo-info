## `hylang:1-python3.13-bookworm`

```console
$ docker pull hylang@sha256:72ff89e31c9456b4744bc5900d7590c150583c4f459eeba0edf5ea757cad4ef2
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

### `hylang:1-python3.13-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:3d143c54229d4e1c22d353da9c27e66a2004f0fd0f01d556369bedcdc6f29d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49696005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2558809d6d68b6b605afa889e0165dfc8c68564820f7b04d32c8d4848a006abb`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:43:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:43:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:43:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Nov 2025 00:43:40 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 04 Nov 2025 00:43:40 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 04 Nov 2025 00:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 00:53:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 00:53:24 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 04:34:10 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 04:34:10 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 04:34:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 04:34:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a67edede8beeefdd89663f635b880706d8ef4f0ff22c80a902a314ff7dedde`  
		Last Modified: Tue, 04 Nov 2025 00:53:36 GMT  
		Size: 3.5 MB (3515863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c107a2515cc55c3c2d2c90ce976d6ad3d1d427a9ad989900777e7d4032c217`  
		Last Modified: Tue, 04 Nov 2025 00:53:36 GMT  
		Size: 12.4 MB (12414582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad412fa6884122450ab80bea740eb12cf1aed01bdbddcedd729db50166d1fa5`  
		Last Modified: Tue, 04 Nov 2025 00:53:35 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6c40c8fa4834d73bc5dfe5ee855a753b84541c11994da15ec620fb0fc1734`  
		Last Modified: Tue, 04 Nov 2025 04:34:27 GMT  
		Size: 5.5 MB (5536745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:99a7a38602cbcafab8c88578d31b8f522c4fac0931c7aae1ec64ba9b950b6efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7359d51780360693a5aa0b322120294d42600bcb9279e26f7dddb8ddbab66256`

```dockerfile
```

-	Layers:
	-	`sha256:f798d9cad4a23c3ede653df3c95bd3396cd131f17fbe89dc12436e2d712a77d8`  
		Last Modified: Tue, 04 Nov 2025 09:19:46 GMT  
		Size: 2.5 MB (2531499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6aa8b075c753f7b45d74c4b76f236cb3ed15d365222f3955c684fd464b3c72b`  
		Last Modified: Tue, 04 Nov 2025 09:19:46 GMT  
		Size: 8.1 KB (8078 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:741e0e07d2df9025578910d30b4dbe3a2ff759a15608eb861ab26a1759372834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46339653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eabad94d906c6823f101e1970936237dce894367e3cb12fc3540a23d0eb632e`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:58:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:58:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:58:45 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 18 Nov 2025 03:58:45 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 18 Nov 2025 03:58:45 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 18 Nov 2025 04:17:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 04:17:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 04:17:27 GMT
CMD ["python3"]
# Tue, 18 Nov 2025 05:32:22 GMT
ENV HY_VERSION=1.1.0
# Tue, 18 Nov 2025 05:32:22 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 18 Nov 2025 05:32:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 18 Nov 2025 05:32:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c97fff5eb07550dcbd62ce4fa3fb5ea12d73e0d973b150828279c3d911c81f0f`  
		Last Modified: Tue, 18 Nov 2025 01:13:41 GMT  
		Size: 25.8 MB (25757530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43622a1784dbe42bedfd53e0cadba9e9362f2135a9c87bea4ddcbfb608454e6c`  
		Last Modified: Tue, 18 Nov 2025 04:17:41 GMT  
		Size: 3.1 MB (3090759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e983a187bc6bb1de56b374c942420eb28e4a28227bfc47f6a47dc65eb767404`  
		Last Modified: Tue, 18 Nov 2025 04:17:41 GMT  
		Size: 12.0 MB (11954179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d629cabfabcf7fd51a2d67e7fd7add7b6eb55744b3f05a6fd98cd2eff1f221`  
		Last Modified: Tue, 18 Nov 2025 04:17:41 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555cf3214f8ec9caca5594a3c3279455bd2b9b7b74a17cb5254018c168116673`  
		Last Modified: Tue, 18 Nov 2025 05:32:36 GMT  
		Size: 5.5 MB (5536936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:7d72900405ee3fe165deb44f5a125c20bb49565f700aa705a4c86387048dea11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2543468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0910704e9ab707bd5af09a40896bb30c096a46e359574ac30480aa9933a64e64`

```dockerfile
```

-	Layers:
	-	`sha256:9ba9eafe6eab2cc077ddc8b6f9a9de964a563ec2f5ca1cc3b42e5ff2ddf44212`  
		Last Modified: Tue, 18 Nov 2025 06:20:07 GMT  
		Size: 2.5 MB (2535311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32cf9fa6cf8aa5e91ececc0432eb52de013a011bbbe286075cccee5199f15fee`  
		Last Modified: Tue, 18 Nov 2025 06:20:08 GMT  
		Size: 8.2 KB (8157 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:dc6269d4a51176b82dfc6f8fb571be17fff07ac0382159ae841c3aa8c4177aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43976043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a97f5340c79f8fdd7fcc9101401d00fd16fdf22febc85f441f42bfa19f628b`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:02:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:02:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:02:37 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Nov 2025 01:02:37 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 04 Nov 2025 01:02:37 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 04 Nov 2025 01:20:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 01:20:44 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 01:20:44 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 03:05:23 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 03:05:23 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 03:05:23 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 03:05:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25ffcfee2f87476a036e69146f86ccab29b006a902ea9fc7f55f9881757b774`  
		Last Modified: Tue, 04 Nov 2025 01:20:59 GMT  
		Size: 2.9 MB (2925468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68850c4bb8d91aeb780c1a0e10b0b30614c56fe4e53dd6fd6a8e7542a04e6252`  
		Last Modified: Tue, 04 Nov 2025 01:21:00 GMT  
		Size: 11.6 MB (11579543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2ec756c95a7fda4446bff2430a06f7dcb0ab427f1594cb9b57c95c6baebfe`  
		Last Modified: Tue, 04 Nov 2025 01:20:58 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626fece55316fc7c6474f0ced23731d3a49203ef6774aef7009d54f7ba250e2c`  
		Last Modified: Tue, 04 Nov 2025 22:59:23 GMT  
		Size: 5.5 MB (5536658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:21d556bdbdfe9701f9c9cc13291dbe60a8773780b0b4f3c2ac8d9e034e3f46d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fbc5fd2e85f46294cb69e1ea2f63f0ecab44d3fb9919d746d6c789a9b4482d`

```dockerfile
```

-	Layers:
	-	`sha256:a13dd913063105d3c80338bb6e7f2dde9b98f7ad521871e7d397636a17107664`  
		Last Modified: Tue, 04 Nov 2025 12:22:50 GMT  
		Size: 2.5 MB (2533744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d80031224081bec58f89770ef1708d45763d927789895f498f38ab3ce04338d`  
		Last Modified: Tue, 04 Nov 2025 12:22:51 GMT  
		Size: 8.2 KB (8157 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:df82886b9bf0e803720461f1c5aba3cb84b724fe4eb2f3d1d950bca19e5482b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49307696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9be0157a3c54fe57e0dfdf0d419bff622e24c55c0d34b5676c72b9cdac39e48`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:41:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:41:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:41:58 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Nov 2025 00:41:58 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 04 Nov 2025 00:41:58 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 04 Nov 2025 00:54:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 00:54:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 00:54:27 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 01:49:04 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 01:49:04 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 01:49:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 01:49:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86e9e38b6d1fdbbdb1007942c642ecf45ef2afdcce9df18ed414d3e7dc37fa4`  
		Last Modified: Tue, 04 Nov 2025 00:54:41 GMT  
		Size: 3.3 MB (3349170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b53eeca1fe6a2da8a532e80fd2913e4e87bcfb1ef8d513067226a8329ac1dd`  
		Last Modified: Tue, 04 Nov 2025 00:54:41 GMT  
		Size: 12.3 MB (12319160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36d97b48fe85b720bb233043f307df38dc1d76adab594e9bb075993bc4f3da`  
		Last Modified: Tue, 04 Nov 2025 00:54:41 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b957c8b50eb32ef624b82cd8ffc0a5fe40677d0133c1c33ad6bf4c50f4a6b7bc`  
		Last Modified: Tue, 04 Nov 2025 01:49:27 GMT  
		Size: 5.5 MB (5536742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:0e09378e42d67a1e2e30ebb1bc3a8d88131f696c9781d62d31c75825731e62fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37800f50641fbcae7e1f1c6a68f514c0a8eb3043d800386477421486dfd8a362`

```dockerfile
```

-	Layers:
	-	`sha256:a4ab9d3aaf5b317c543f8536ae7d4156b599bc5ec585f10224b068f29556a3b1`  
		Last Modified: Tue, 04 Nov 2025 12:22:57 GMT  
		Size: 2.5 MB (2531764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c21631357d5df350fe7212595668d966df72e4d639f4b6bc81cab03d5bfba08`  
		Last Modified: Tue, 04 Nov 2025 12:22:58 GMT  
		Size: 8.2 KB (8182 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:0174c01ea7765c7adf03e747f683ff2706d73818a1cb567373ff168388bc57c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50915482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50f8b12cd50e57463467fbd0cf4cd0d657cab0c03692a74d7de5e6ae0fe4e89`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:35:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:35:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Nov 2025 00:35:40 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 04 Nov 2025 00:35:40 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 04 Nov 2025 00:46:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 00:46:32 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 00:46:32 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 01:50:00 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 01:50:00 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 01:50:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 01:50:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2c58c29af2797ca749d7419a92892ae1754c44238cf3c0819fbd0cec21f679`  
		Last Modified: Tue, 04 Nov 2025 00:46:44 GMT  
		Size: 3.5 MB (3516517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545bdf0b815875afc788c33916acee90e8a73b1011e1a14e0fb27363a033f563`  
		Last Modified: Tue, 04 Nov 2025 00:46:45 GMT  
		Size: 12.7 MB (12652158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3236c0af78548aa74bedcc1bddee17e1d57297b1572498c31c849f27e0da0219`  
		Last Modified: Tue, 04 Nov 2025 00:46:44 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30d16d7971769dfc8c6b6884887c62ec6b02e377e08ebbc4f7a9d0d6d075e1c`  
		Last Modified: Tue, 04 Nov 2025 01:50:13 GMT  
		Size: 5.5 MB (5536713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:9a9d4196b62535cdcf08a4b094913a5f225fd7d4bd08a79c3c56759ce2ac3d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2536712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d47adac8000d89cca46b8ff62f545a0e2644d6dda2770a9c806d5bb98cd8d23`

```dockerfile
```

-	Layers:
	-	`sha256:f717384445d4865e7265ef6c04d5d682d6e5741e20c40546b03aa64bafd0d381`  
		Last Modified: Tue, 04 Nov 2025 09:20:01 GMT  
		Size: 2.5 MB (2528666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826a89cbb7ca93aa22ecda114905c26f6ffa10b2a5f75b2a584e824e8a17370e`  
		Last Modified: Tue, 04 Nov 2025 09:20:01 GMT  
		Size: 8.0 KB (8046 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:00e552ffb06d3f2a77b69f8d0aed81e3b2d2fa75dd126d2486a7d7698cc4e05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54282448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea47128f7e3041be8d713aadb3647ee6e050d5e94e50cb9602526f432577a3ea`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 09:01:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 09:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 09:01:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Nov 2025 09:01:43 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 04 Nov 2025 09:01:43 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 04 Nov 2025 10:32:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 10:32:28 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 10:32:28 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 20:03:00 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 20:03:00 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 20:03:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 20:03:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028f63dbeb1c092f934e6315b20e4051a0b85ef93fd499633c4ad5a23892b21e`  
		Last Modified: Tue, 04 Nov 2025 09:23:23 GMT  
		Size: 3.7 MB (3721186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61c1a5f11490dde9c08169663adc552940ebd628eba02f14b61d2381a8cd1d1`  
		Last Modified: Tue, 04 Nov 2025 10:33:04 GMT  
		Size: 13.0 MB (12955152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac05220e1e2a1448d0ce45bcc4252774f9a4e265647f71f19b21e85b16c7d03`  
		Last Modified: Tue, 04 Nov 2025 10:33:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9ca29723a14246a58950d9370786092bea21a9c654ff0582ed69c42a46a81`  
		Last Modified: Tue, 04 Nov 2025 20:03:25 GMT  
		Size: 5.5 MB (5536957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d6a5d27a34e969b82bcbb3a259fb4852d63c0e09ef08b76c4a1ed21f72fbbeaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2544059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf791d8152f41362656b7bb72e1ff7d03e3996ae96bd44dfa7eea0b00ce2b356`

```dockerfile
```

-	Layers:
	-	`sha256:e48fc314f817639a826423ecd75fca0f2b88f3c5b520f463fc0c898375a212ce`  
		Last Modified: Tue, 04 Nov 2025 21:19:42 GMT  
		Size: 2.5 MB (2535937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e743f176c16d193fd9008e75b0e67171b9e2771d945812f48b5f55759fa5e814`  
		Last Modified: Tue, 04 Nov 2025 21:19:43 GMT  
		Size: 8.1 KB (8122 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:b2e12598f56abf6cec743794042665dd711dcc1015f6dab7c08d8022bdac8320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47858376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67348924c8c47d2e40a55ca43be5bba9bcf702c01d20ed1bb9465cf9c9d0a7e2`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 04:38:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:38:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:38:38 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Nov 2025 04:38:38 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 04 Nov 2025 04:38:38 GMT
ENV PYTHON_SHA256=ed5ef34cda36cfa2f3a340f07cac7e7814f91c7f3c411f6d3562323a866c5c66
# Tue, 04 Nov 2025 05:27:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 05:27:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 05:27:53 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 13:39:45 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 13:39:45 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 13:39:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 13:39:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca4a57885b9071f1d3b5a6a799c42a41cffb2c92127d8614a2de2ed49827eff`  
		Last Modified: Tue, 04 Nov 2025 04:55:37 GMT  
		Size: 3.2 MB (3181812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533b99dccbd2622d594a0982d2ac4dcffff1fc649fe163e2f48df7c2d70e3ca7`  
		Last Modified: Tue, 04 Nov 2025 05:28:25 GMT  
		Size: 12.3 MB (12255142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a300353ef2a040119439eef94dbd8db0232fb83d17a5ff3d3b0ac802df2d13a2`  
		Last Modified: Tue, 04 Nov 2025 05:28:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9a499874fe4be0836391736cc82e9e761654237874c2f839215daade4664d1`  
		Last Modified: Tue, 04 Nov 2025 13:40:04 GMT  
		Size: 5.5 MB (5536623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:4c558b291e8cff785089f4dacebada6d5936be217d2a2aa6e848e8435e12b647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2536401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67b5fed1f6f265ae7c2e47bb3537d6e45186b4440edcbcfb2a0f9f0d94a3c13`

```dockerfile
```

-	Layers:
	-	`sha256:f0472830f3e861c6e09e15377c86c5675c300dfb82392d974fda51bfcc1d2a54`  
		Last Modified: Tue, 04 Nov 2025 15:18:37 GMT  
		Size: 2.5 MB (2528323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fe63cb28c5568bb8184a5ddc8471e48cb24ee26b3765ab3f3442d0f42c14613`  
		Last Modified: Tue, 04 Nov 2025 15:18:38 GMT  
		Size: 8.1 KB (8078 bytes)  
		MIME: application/vnd.in-toto+json
