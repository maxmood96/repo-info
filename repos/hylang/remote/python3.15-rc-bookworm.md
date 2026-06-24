## `hylang:python3.15-rc-bookworm`

```console
$ docker pull hylang@sha256:245b2039ef8039abf50d6cfc9051aa1af33ea2c4798845b910d5d44a716221e9
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

### `hylang:python3.15-rc-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:e8d19f9844de21d3d11d264028b83ed41f5d2a7f15a79d739027ea47c47d330a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51172982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cd084b4355ba401dee10ca57019c4f607eeff00c3e40cb991a2359dd745958`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:57:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:57:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:57:46 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 24 Jun 2026 01:57:46 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 24 Jun 2026 02:09:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:09:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:09:59 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 02:46:06 GMT
ENV HY_VERSION=1.3.0
# Wed, 24 Jun 2026 02:46:06 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 24 Jun 2026 02:46:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 24 Jun 2026 02:46:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1e32b2cec0c4af3e4adf2ad43a9a1b5e9bace9e159c4a0040470d047eb61bc`  
		Last Modified: Wed, 24 Jun 2026 02:10:08 GMT  
		Size: 3.5 MB (3520756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc9ee934cdbc2ceed04c72a2684040d56420917366c728f01dabef743bf938d`  
		Last Modified: Wed, 24 Jun 2026 02:10:08 GMT  
		Size: 13.6 MB (13569876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab640c9ea8135821a937f837575f8cd3892c765b988ba185f9005098233b05f7`  
		Last Modified: Wed, 24 Jun 2026 02:10:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3c16eacf8c5a327dbffcef48f05f2d3ff5d120429b1795eacf2cbba070733c`  
		Last Modified: Wed, 24 Jun 2026 02:46:13 GMT  
		Size: 5.8 MB (5844461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:74a5edf9ef81ea9c64e7b4ce27052ada011124a1d4c5bb0c260d50a8b1f52379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de15aed98fbb1c6bb7b0050b1d74d365c4dfad38bd87d44b7366da73bbf5912c`

```dockerfile
```

-	Layers:
	-	`sha256:ac9fd4c6e24765968c1b10c616cb17e2d3e2384c4879f6a548d5297356895a58`  
		Last Modified: Wed, 24 Jun 2026 02:46:12 GMT  
		Size: 2.5 MB (2530840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88034ce64d159c85a278fd6cdea8cef5126cceac3a380673aa9b9e1ad05bf84`  
		Last Modified: Wed, 24 Jun 2026 02:46:12 GMT  
		Size: 8.1 KB (8066 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:080d508797eff14e2000312bd27f647d827b406fdc3b4ffeae0c95f2b4fe96b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47832944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53413edae417acb9fb2c5088983a6edd93cff8b7f975cc5c518321f85e6fa3d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:38:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:38:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:38:31 GMT
ENV PYTHON_VERSION=3.15.0b2
# Thu, 11 Jun 2026 01:38:31 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Thu, 11 Jun 2026 01:59:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 01:59:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 01:59:40 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 03:03:25 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 03:03:25 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 03:03:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 03:03:25 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:99eb1512995af32b91c63bcd418e886af77e3c7ca088226161af558763425461`  
		Last Modified: Wed, 10 Jun 2026 23:38:28 GMT  
		Size: 25.8 MB (25773188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ce4150c705ad4dc627926707bbdab7fd6838267950e4512054b77ce02ac514`  
		Last Modified: Thu, 11 Jun 2026 01:59:48 GMT  
		Size: 3.1 MB (3093594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a649065635db00f36cbb310a8f19a6c8d496817627d16a6ef553fd6e5266f3f`  
		Last Modified: Thu, 11 Jun 2026 01:59:48 GMT  
		Size: 13.1 MB (13121469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94da4b001ba3835851f02f6a093b112842d3f80406f1cf3b5b5a2ad6a60df727`  
		Last Modified: Thu, 11 Jun 2026 01:59:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c086fe7601fa04cc947224ede394f38ab7fcef70e4a3419ab3a924ddb06667d4`  
		Last Modified: Thu, 11 Jun 2026 03:03:32 GMT  
		Size: 5.8 MB (5844444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:c11536000641d4b6df22e60ea3aa3bbb147597c1006d10c38dc41d05641a7e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626317b8c03795c8f788f4e91d488bf9e857160bef780018d5da9f267defb7fd`

```dockerfile
```

-	Layers:
	-	`sha256:6560d64b11c2dfec4355a6877e466f2fd1dee7b3a07bf560d755bda1948587a6`  
		Last Modified: Thu, 11 Jun 2026 03:03:32 GMT  
		Size: 2.5 MB (2534652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd2d59ab36db6c71dc80172c3cb95f9721fd91c95d9615b73b74bdd11887217`  
		Last Modified: Thu, 11 Jun 2026 03:03:32 GMT  
		Size: 8.1 KB (8146 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:cfcc64ab60d5cf9df2640188059e6bce47f6609b01259fa722f2339aceb05496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45675519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1dab6e4925202f740d31a1ea7d71974f6242e7aa1ded88b2e96384efec16d1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 02:14:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:14:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:14:10 GMT
ENV PYTHON_VERSION=3.15.0b2
# Thu, 11 Jun 2026 02:14:10 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Thu, 11 Jun 2026 02:37:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 02:37:54 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 02:37:54 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 03:22:19 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 03:22:19 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 03:22:19 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 03:22:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051bb655a92dd8de631fbf126f9840fa0e28ffb9c189649fe6ab812bc5b1f700`  
		Last Modified: Thu, 11 Jun 2026 02:38:02 GMT  
		Size: 2.9 MB (2928748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d03a63f41a6696068d41f5575eef91dce5ac86bf9796256f7b51473db751bf`  
		Last Modified: Thu, 11 Jun 2026 02:38:02 GMT  
		Size: 13.0 MB (12957592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31689682b57b2c3a963bd3152ce263a5df73c080a629731ea9d388895e93d2`  
		Last Modified: Thu, 11 Jun 2026 02:38:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42ebc4baebbb40e251fd9c1134452685d4c41a13d6613f96c3a8aaac9043f55`  
		Last Modified: Thu, 11 Jun 2026 03:22:26 GMT  
		Size: 5.8 MB (5844457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:0af43ee5cd29abce254ae4f6a35c021a0266c82f3a5646a579e3567890c2873e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5549db8c0666a3017234dacca8ff4b1f642b38c82041d31eb3ba87f7070f1cfb`

```dockerfile
```

-	Layers:
	-	`sha256:dd72751e43d39ddc5245f810b2e9f246f52c48c81b9b901c066c04ea49b3f022`  
		Last Modified: Thu, 11 Jun 2026 03:22:26 GMT  
		Size: 2.5 MB (2533085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:943bd053b81ff1e4a24c35a43814a931f8423132764a9fc96ee2339b12df3296`  
		Last Modified: Thu, 11 Jun 2026 03:22:26 GMT  
		Size: 8.1 KB (8146 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b854bb801dbc0ae125f93c0689a1bf13d2c594911c5afe12837bec34462b3c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50779358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9245005d1eae5dc07ff48dea7216d775e7f5ea89972c06924643abebfb0a618c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:01:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:01:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:01:52 GMT
ENV PYTHON_VERSION=3.15.0b2
# Wed, 24 Jun 2026 02:01:52 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Wed, 24 Jun 2026 02:17:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:17:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:17:11 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 03:24:18 GMT
ENV HY_VERSION=1.3.0
# Wed, 24 Jun 2026 03:24:18 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 24 Jun 2026 03:24:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 24 Jun 2026 03:24:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558af0da76d22ec1b23b8d6448fdbaebec35744074e0567c88ff08566960cf00`  
		Last Modified: Wed, 24 Jun 2026 02:17:20 GMT  
		Size: 3.4 MB (3352665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133855bf74e461bffb7b743bf55af64dee3ff33b216d6868b2fec228264287ed`  
		Last Modified: Wed, 24 Jun 2026 02:17:21 GMT  
		Size: 13.5 MB (13459641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ba5828252fb185a326ac974f4069d0aaff73f7c4dc5cf1e99035058e97db3d`  
		Last Modified: Wed, 24 Jun 2026 02:17:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ff2a01b58bf59a0e6d7f0d6ee47438f2c64aad955c5c0f1363ce159922a1a`  
		Last Modified: Wed, 24 Jun 2026 03:24:25 GMT  
		Size: 5.8 MB (5844385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:98818edf0ef72fdc672f1a6ac406eb7d7bafbe8fe918eed925b1c363cbf3abde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b83af4fa535ce6b722434981a1489cf5e6462f6e7601e942d84ceaed919149b`

```dockerfile
```

-	Layers:
	-	`sha256:d1f49e0c2dcd5bf5e487644a66acf927069e8857e09edaf2aa97c64a410740b7`  
		Last Modified: Wed, 24 Jun 2026 03:24:25 GMT  
		Size: 2.5 MB (2531105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8463abe855d17c8c054dbe89712e5224d514dd3fdafe3d05ddf61027290c734`  
		Last Modified: Wed, 24 Jun 2026 03:24:25 GMT  
		Size: 8.2 KB (8170 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:ccf072410bc55b1ea197a92eb161c0065d09467bb40d4e1d73d0a26b4b2fbe31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52211372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0949885e9a2a2db03900d4680640a18f99ff6e275bec7e8f9e8bcbb05ed77d6a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:56:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:56:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:56:47 GMT
ENV PYTHON_VERSION=3.15.0b2
# Thu, 11 Jun 2026 00:56:47 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Thu, 11 Jun 2026 01:08:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 01:08:57 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 01:08:57 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 02:39:11 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:39:11 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:39:11 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:39:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:707460b758530d4476f3fefff30544db7cf8dbd98838ccc3533bc05e79016be4`  
		Last Modified: Wed, 10 Jun 2026 23:40:00 GMT  
		Size: 29.2 MB (29225762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dd3347f2f72f48194c75174f49cd3b432f6dcbb2ee7ade388321883df7fef8`  
		Last Modified: Thu, 11 Jun 2026 01:09:04 GMT  
		Size: 3.5 MB (3521262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511da67845d6a3d710934aa42d6d8d895482eb30ecf7700cc6c6fad0cd59c25b`  
		Last Modified: Thu, 11 Jun 2026 01:09:05 GMT  
		Size: 13.6 MB (13619646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669094d05931cfda5b4929a8ec7c8c2df51699f88954eacfc56e90475146cb30`  
		Last Modified: Thu, 11 Jun 2026 01:09:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f914a6da7b889095d8e89a269764d9edb23ff5497da0545b87b6b06165f975`  
		Last Modified: Thu, 11 Jun 2026 02:39:18 GMT  
		Size: 5.8 MB (5844452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:f3404e6917140df22c3d76fb178b68f898c22a3eb516aa5cfbb9d7fe76ad7aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2536041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd772574fce395142c95b65aa07e57c00da1c4f097479d2182c71abd1294cfb`

```dockerfile
```

-	Layers:
	-	`sha256:d4a3241714763ef683d5bad2b5f4dac3e8b7ba69ad9b54738a26d6a350a3e40b`  
		Last Modified: Thu, 11 Jun 2026 02:39:17 GMT  
		Size: 2.5 MB (2528007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:737fbb80474f02837b54620eb8aa8b28da8cfb4152131f17f42ee9dfb592711f`  
		Last Modified: Thu, 11 Jun 2026 02:39:17 GMT  
		Size: 8.0 KB (8034 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:9d0de2352577da9f4fa16652ca9319fbe4f94de99c5b36e30d46f936ed5733c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55783861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a13468fb23eec165cf384e8de7b797d066dee0fa23e93c3b117e4178a4265be`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 06:26:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 06:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 06:26:38 GMT
ENV PYTHON_VERSION=3.15.0b2
# Thu, 11 Jun 2026 06:26:38 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Thu, 11 Jun 2026 07:06:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 07:06:42 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 07:06:42 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 12:30:25 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 12:30:25 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 12:30:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 12:30:25 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffff1806bb6bf93f814c216d53e5fb0eeebd91e9ad17139df973493f652d2d1b`  
		Last Modified: Thu, 11 Jun 2026 07:06:57 GMT  
		Size: 3.7 MB (3725204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab53d8d518724f883d0f76ff9e7e85550460692c540c623c63bd6a82d54ca3d`  
		Last Modified: Thu, 11 Jun 2026 07:06:58 GMT  
		Size: 14.1 MB (14131944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d3e4552339cc5bf397a9917a4450564998e00b50621b3a1e6ee96c7493fae`  
		Last Modified: Thu, 11 Jun 2026 07:06:57 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9fc1c3d7cabcfcc2192a740ea51b414697a20fc5c391c0ac91b94d3041c865`  
		Last Modified: Thu, 11 Jun 2026 12:30:39 GMT  
		Size: 5.8 MB (5844523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:b6d10c05bd2e41fe5173640fadc2c8fd6ac8c9bcb9d87a499322b939c6e67806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2543388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb352a5adfca990e7a8ee55a6448796bccaf7d75d9aad431a5a57c45775c5a8f`

```dockerfile
```

-	Layers:
	-	`sha256:82f9aad4953c34dca46e38ca1efe5657d88679d098528c9407658002a378717e`  
		Last Modified: Thu, 11 Jun 2026 12:30:39 GMT  
		Size: 2.5 MB (2535278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb39e3132a424f35252c0a55a0b72ad7f6201464b18578a70a97e4dd1591cbd`  
		Last Modified: Thu, 11 Jun 2026 12:30:38 GMT  
		Size: 8.1 KB (8110 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:ab9125fecceb4368bf0fe5ef464ff5f2cfe32b9f5989bf093d3a6a1d79112640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49346153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21883f0387157d09cf0656b6855d2e8e56d4095ecf9b4678e26ce607675721e2`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 02:17:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:17:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:17:57 GMT
ENV PYTHON_VERSION=3.15.0b2
# Thu, 11 Jun 2026 02:17:57 GMT
ENV PYTHON_SHA256=d14f474ab679e90bc734b02ff58447b6ec99a821af61d6ff0c1da0f86e341a71
# Thu, 11 Jun 2026 02:35:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 02:35:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 02:35:11 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 04:01:50 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 04:01:50 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 04:01:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 04:01:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a0a60c4602b07983dd7562e2e3d2a37486c8cc254ef820fa2f873b13a5ed28`  
		Last Modified: Thu, 11 Jun 2026 02:35:24 GMT  
		Size: 3.2 MB (3184062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355c97a4e825db64574cf0535acbef0184aab218efd9ebdc270007be2b24738b`  
		Last Modified: Thu, 11 Jun 2026 02:35:25 GMT  
		Size: 13.4 MB (13424011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288c22d84de3ac792394a9c03d5e5ecdadb7a11ed0133d1809e72aa91353a40b`  
		Last Modified: Thu, 11 Jun 2026 02:35:24 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc08b738d622fed29edb9d11a012a166b96f6c17f2522964836c33c98444558a`  
		Last Modified: Thu, 11 Jun 2026 04:02:02 GMT  
		Size: 5.8 MB (5844322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:37ea22981eb0cf80587171468c860469cec8043f0c5b8e616fcba53051c66eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce4f73c7bb9295840eb1e7e09c98249aeea2f9c43c8cb03c61ebb8fba49cda8`

```dockerfile
```

-	Layers:
	-	`sha256:e7700ce5b40b2451e1ff8186772e01f59842dd96ef11692f04e957b2916de8d1`  
		Last Modified: Thu, 11 Jun 2026 04:02:02 GMT  
		Size: 2.5 MB (2527664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbce5a98fc142758112e54eebfb88dc5d2963e9ac481a5b6342129cd0a4d5e6`  
		Last Modified: Thu, 11 Jun 2026 04:02:02 GMT  
		Size: 8.1 KB (8066 bytes)  
		MIME: application/vnd.in-toto+json
