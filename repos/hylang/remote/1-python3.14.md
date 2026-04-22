## `hylang:1-python3.14`

```console
$ docker pull hylang@sha256:352456a0d20d75e63a8be21603fa401c879054829805a0d39a61a0a57bdee76c
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
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `hylang:1-python3.14` - linux; amd64

```console
$ docker pull hylang@sha256:42ff8a7e029308f2ac717d0a3ad2dc75faa3987d02f808a007ef74efcef526e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51852526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4eaf8e88236fd48b8bbedfc0f742099a7063acda5fffe2de62053139142f85`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 08 Apr 2026 17:32:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:32:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Apr 2026 17:32:12 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 08 Apr 2026 17:32:12 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 08 Apr 2026 17:39:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Apr 2026 17:39:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Apr 2026 17:39:27 GMT
CMD ["python3"]
# Wed, 08 Apr 2026 18:13:24 GMT
ENV HY_VERSION=1.2.0
# Wed, 08 Apr 2026 18:13:24 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 08 Apr 2026 18:13:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Apr 2026 18:13:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3efd01bc8be0872bc48a767cd5908b126f995243670ee144c0197c31905fa71`  
		Last Modified: Wed, 08 Apr 2026 17:39:41 GMT  
		Size: 4.3 MB (4258706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2b6558739bbd1f8b1d1002a2d892b543b6d63a4d7c212e700f033cbdb0f426`  
		Last Modified: Wed, 08 Apr 2026 17:39:45 GMT  
		Size: 12.3 MB (12272343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094edf543c5de9f94a08a38c5a2df505ab2bfd3d9e032aeb6268fa312b45af7f`  
		Last Modified: Wed, 08 Apr 2026 17:39:40 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84a8497d9445ee7efdeaf552c3254a7d58c3b643e42e0a1041d41e0f2633c79`  
		Last Modified: Wed, 08 Apr 2026 18:13:32 GMT  
		Size: 5.5 MB (5545586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14` - unknown; unknown

```console
$ docker pull hylang@sha256:245c0a683bd4ebf2e2ca4ad1f51b4fd0a0d691d1ce5931c4769b22fd8331f891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e013e28b3eb493af7984b415baf68f5484da5fadbedbc9e898f9b10e6f0ccee`

```dockerfile
```

-	Layers:
	-	`sha256:e492a5e26b0763ae41f7682d058529fdf08800abd4f43f2c91c66208d7ca59c6`  
		Last Modified: Wed, 08 Apr 2026 18:13:32 GMT  
		Size: 2.2 MB (2156649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33ebe1192c54de0459769c2201f839f9a9c57234199a6229a65bf100701739ef`  
		Last Modified: Wed, 08 Apr 2026 18:13:31 GMT  
		Size: 11.6 KB (11643 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14` - linux; arm variant v5

```console
$ docker pull hylang@sha256:ffe8197dd2d9c93e0b8bfd0c4872c617fffd53aaa1b7c53f565cb8e5d1921802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49092648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e45cb98ecf07eeef67c555d20b395d3bf39157e58a5b4a92d106f9ad1e5ac57`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Wed, 08 Apr 2026 17:23:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:23:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Apr 2026 17:23:29 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 08 Apr 2026 17:23:29 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 08 Apr 2026 17:45:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Apr 2026 17:45:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Apr 2026 17:45:23 GMT
CMD ["python3"]
# Wed, 08 Apr 2026 18:19:19 GMT
ENV HY_VERSION=1.2.0
# Wed, 08 Apr 2026 18:19:19 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 08 Apr 2026 18:19:19 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Apr 2026 18:19:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de97b396cc293ac34e1b661ea7f82a0a5a7cb097f2765f5b2498e17234e594f8`  
		Last Modified: Wed, 08 Apr 2026 17:34:26 GMT  
		Size: 3.7 MB (3653685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c2c4c696eaa76771d07c4e6ccdcb8c6feed31d29303214cbc296e8cbb52033`  
		Last Modified: Wed, 08 Apr 2026 17:45:46 GMT  
		Size: 11.9 MB (11949244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a114f980df21fffd5c784cc8d14623e17ccf818c15d07fdac5215fe1724b4`  
		Last Modified: Wed, 08 Apr 2026 17:45:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99420b99005bb06f8dabf86b543b0df3cc7753ec7aedb584692b13a04d9ed3f`  
		Last Modified: Wed, 08 Apr 2026 18:19:26 GMT  
		Size: 5.5 MB (5545661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14` - unknown; unknown

```console
$ docker pull hylang@sha256:35367a9f8d73f9f865d6a2e84792d6949a66778378554d52e05f7b0a1d08ebca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9223c8aed17b7976e3112edb006dd4f2e7c4f69464dd51bdd141a3230dce4c63`

```dockerfile
```

-	Layers:
	-	`sha256:bd2c0e5b55d891eeea5d48f0d693356506a8f6217812f71b1c42bf9487eb48d9`  
		Last Modified: Wed, 08 Apr 2026 18:19:26 GMT  
		Size: 2.2 MB (2159714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea3c70286580f0451ba215dc1a1321173bc40fb39109073f7ae2a78528c6d0a`  
		Last Modified: Wed, 08 Apr 2026 18:19:26 GMT  
		Size: 11.8 KB (11819 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14` - linux; arm variant v7

```console
$ docker pull hylang@sha256:57aa1a9734628c5dd2bc7332defa7667c3ee94c568220286021dd3397780d528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46846245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1888aa67c2dc4fa35c1449922de240a645c098067d963085b8d6dd510c3c64b0`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Wed, 08 Apr 2026 17:22:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:22:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Apr 2026 17:22:41 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 08 Apr 2026 17:22:41 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 08 Apr 2026 17:33:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Apr 2026 17:33:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Apr 2026 17:33:43 GMT
CMD ["python3"]
# Wed, 08 Apr 2026 18:13:06 GMT
ENV HY_VERSION=1.2.0
# Wed, 08 Apr 2026 18:13:06 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 08 Apr 2026 18:13:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Apr 2026 18:13:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2997286a4f5d2927d6f8f011f3a68a16361903aec075ca5780a8cffb51b140`  
		Last Modified: Wed, 08 Apr 2026 17:33:51 GMT  
		Size: 3.5 MB (3455485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91d94650d7ecbff234f231380394f435f1a2b753a8f586e3e3e65a82403ea6b`  
		Last Modified: Wed, 08 Apr 2026 17:33:52 GMT  
		Size: 11.6 MB (11635249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6570083a516111518ae80d740186d42d85640421552391504bc80ff0cfad58`  
		Last Modified: Wed, 08 Apr 2026 17:33:51 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e45304fc490653be6f768f94f2aee76dc8c77fdacf060d3c8670bc674d5485`  
		Last Modified: Wed, 08 Apr 2026 18:13:14 GMT  
		Size: 5.5 MB (5545608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14` - unknown; unknown

```console
$ docker pull hylang@sha256:a2257ce0d1c5634bc4d4a9b5d61a0f71e496f7e86044e9e036124f34615b183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cfe10e679cff43b6ef8e4b79aa9c6fabdda65960cb32f23332347d0eb7c8a1`

```dockerfile
```

-	Layers:
	-	`sha256:b1f113c7cd7129c43fdcba9053c85c6de2e60a9aa3777da3adcf6208f1c38562`  
		Last Modified: Wed, 08 Apr 2026 18:13:14 GMT  
		Size: 2.2 MB (2158167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deb9daaaec67861196531e37e21145366f0fab5a0fcdf1671f94feff8a43167a`  
		Last Modified: Wed, 08 Apr 2026 18:13:14 GMT  
		Size: 11.8 KB (11819 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c7755dab5680475466d161c469bc287b4b08165c68b0f6a759b0310fcdc2eae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49167033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c9a06e1bd0e94cbf11a955b905c1bb2822f393ffbd45fd27b508306d4b023c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:00:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:00:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:00:09 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 22 Apr 2026 02:00:09 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 22 Apr 2026 02:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:07:44 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:07:44 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 02:47:57 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 02:47:57 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 02:47:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 02:47:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30430ade496b9c0573f53017e4f2c94d902451d9e06c7f712412d5636f93633b`  
		Last Modified: Wed, 22 Apr 2026 02:07:51 GMT  
		Size: 1.3 MB (1273870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6231176d9e49373836bc61512e4592cdb01182329540647435a969f9a8a8726b`  
		Last Modified: Wed, 22 Apr 2026 02:07:52 GMT  
		Size: 12.2 MB (12183715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e2c28dc105e1d0105bb477289d6f5a96ff4183c2007f95b132e690f335be4e`  
		Last Modified: Wed, 22 Apr 2026 02:07:51 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa4c258ac00fee142bb3ba8f58b1ec2293fa1c7af1a137a75d18e8e8840084`  
		Last Modified: Wed, 22 Apr 2026 02:48:04 GMT  
		Size: 5.6 MB (5565594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14` - unknown; unknown

```console
$ docker pull hylang@sha256:52b5c7bc93c03acf3bd299d0ddfc47423417669dc027e345e5abd3489e51a085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c215c032451bc973792c22ddbe251d2771bbd17765d040cc04ae8eb7255dff8`

```dockerfile
```

-	Layers:
	-	`sha256:b7e866d7a593d06788bf402b63ae667364fd07c560b0c454fd33811181265fb1`  
		Last Modified: Wed, 22 Apr 2026 02:48:04 GMT  
		Size: 2.2 MB (2157059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23857096f69057514918c79a561a65edb71411c2c8526e8bea14b930571ee8d9`  
		Last Modified: Wed, 22 Apr 2026 02:48:04 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14` - linux; 386

```console
$ docker pull hylang@sha256:702d2ca900fdb9e0026d31d9b4b854902a76d9ea2a03c41ce81ee0a799781868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50486476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab00cda76b5a313ccdd049a5a96d23921affb54fe80e89d27c942ef714c9811`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:57:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:57:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:57:14 GMT
ENV PYTHON_VERSION=3.14.3
# Tue, 07 Apr 2026 01:57:14 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Tue, 07 Apr 2026 02:14:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Apr 2026 02:14:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Apr 2026 02:14:40 GMT
CMD ["python3"]
# Tue, 07 Apr 2026 02:56:41 GMT
ENV HY_VERSION=1.2.0
# Tue, 07 Apr 2026 02:56:41 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 07 Apr 2026 02:56:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 07 Apr 2026 02:56:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3ad58e7663dac2e874d85633f012dff41d0fc985f7d40eeef495d01a4201e3`  
		Last Modified: Tue, 07 Apr 2026 02:14:47 GMT  
		Size: 1.3 MB (1297206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0272dd4cb7195931b2beb5f7d5e2da6e442a6959e5120a272961a4ab57a2a012`  
		Last Modified: Tue, 07 Apr 2026 02:14:48 GMT  
		Size: 12.4 MB (12378090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96903a511312da826b57d25e208b7d468f2e0e463902203e0ad7b039a3a56cc`  
		Last Modified: Tue, 07 Apr 2026 02:14:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b21a66bb9c3a8c0461220a9eaefc6db5bf6d07a0338fa77d47558747edd035`  
		Last Modified: Tue, 07 Apr 2026 02:56:48 GMT  
		Size: 5.5 MB (5519679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14` - unknown; unknown

```console
$ docker pull hylang@sha256:37eb874ea5b3019eac780a2e82c78289777c58cca909ab26f309f7705bbd49ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099aba0371647108d7591c594585b4bfd272da8c109080b7be661440a9d85d5e`

```dockerfile
```

-	Layers:
	-	`sha256:6d1061a4f6b9862e6f8ac06da30c0340b30cd9582bad91ccfb2f1f93af8c4ca6`  
		Last Modified: Tue, 07 Apr 2026 02:56:48 GMT  
		Size: 2.2 MB (2153762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb268c2b7e1850611e07742276dc8eebce1479c69e6cb3807fa69c70eb470eec`  
		Last Modified: Tue, 07 Apr 2026 02:56:48 GMT  
		Size: 11.6 KB (11551 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14` - linux; ppc64le

```console
$ docker pull hylang@sha256:47609ecc4fe441f5726f336ac25891a3477157ff7c14eadcc2cf321675fe39a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56351612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ca1882443d31d4dc69e7f58891103209204819b5c2e03d69c8ef14528209ff`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Wed, 08 Apr 2026 17:51:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:51:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Apr 2026 17:51:28 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 08 Apr 2026 17:51:28 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 08 Apr 2026 19:26:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Apr 2026 19:26:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Apr 2026 19:26:23 GMT
CMD ["python3"]
# Wed, 08 Apr 2026 21:41:05 GMT
ENV HY_VERSION=1.2.0
# Wed, 08 Apr 2026 21:41:05 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 08 Apr 2026 21:41:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Apr 2026 21:41:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735850e02bab0a056d2ba5e6f6358357ad06c1c5c5a39f97000557d145fd10b6`  
		Last Modified: Wed, 08 Apr 2026 18:16:16 GMT  
		Size: 4.5 MB (4525449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4472063d69bf1be5717529a8bf69b9f3c71bbf8ff17d889bad72c87021f2e8b`  
		Last Modified: Wed, 08 Apr 2026 19:26:38 GMT  
		Size: 12.7 MB (12687161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e430083e888f4c103f4c493305cbbc2d727e11ae54ab2ab98f853941942f1a`  
		Last Modified: Wed, 08 Apr 2026 19:26:37 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817b0e74b961857b2a70a2b49e2d1f7c7695e9f23e288085627a9992bf8afbcf`  
		Last Modified: Wed, 08 Apr 2026 21:41:18 GMT  
		Size: 5.5 MB (5545736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14` - unknown; unknown

```console
$ docker pull hylang@sha256:5776bc3abadb7ff2c9f34317eaf77461cc25654835b95913b6ea732846398f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2c399a0c852d9a0ac60f9a74f6d23013f320a9803639ca089c5d18c67fb1f2`

```dockerfile
```

-	Layers:
	-	`sha256:fb65d140ba3b207516140a525ada331b8b27dec6c1428d06fd0360b712b43af4`  
		Last Modified: Wed, 08 Apr 2026 21:41:18 GMT  
		Size: 2.2 MB (2160288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:109aef3933b81065e45196fe5f8d6eae6fea0685982180e9704cd353309b3983`  
		Last Modified: Wed, 08 Apr 2026 21:41:18 GMT  
		Size: 11.8 KB (11759 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14` - linux; riscv64

```console
$ docker pull hylang@sha256:c08087edfa93d5586246d6fdd233738ed6c1ed7e6bf9b5ddf85b28f0e7035a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49983428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b4cdc0e30b8bd85e1b5205260d3f35fe7782c533c38c7869cb25a0eaa9aa70`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 11:06:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 11:06:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 11:06:39 GMT
ENV PYTHON_VERSION=3.14.4
# Sat, 11 Apr 2026 11:06:39 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Sat, 11 Apr 2026 15:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Sat, 11 Apr 2026 15:42:16 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 11 Apr 2026 15:42:16 GMT
CMD ["python3"]
# Sun, 12 Apr 2026 19:25:48 GMT
ENV HY_VERSION=1.2.0
# Sun, 12 Apr 2026 19:25:48 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 12 Apr 2026 19:25:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 12 Apr 2026 19:25:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14380c29384b5ed760b6898c4ce267c4a4b26800f0f895ed3c6f7c1456191663`  
		Last Modified: Sat, 11 Apr 2026 12:44:35 GMT  
		Size: 3.9 MB (3873978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab86fcd37fc7b53388c4f61cd8e2c5296241a76af81a47c5b98ead3a59b1fa20`  
		Last Modified: Sat, 11 Apr 2026 15:43:24 GMT  
		Size: 12.3 MB (12287099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5efda4d64fd216bd9edbeeb4574548976089f27dae179ba84a8a3a1e35c9cd`  
		Last Modified: Sat, 11 Apr 2026 15:43:22 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7087e3f8062dbc354b2acb03623e9107fc1d541324d9ac8c8804612e89bdafa6`  
		Last Modified: Sun, 12 Apr 2026 19:26:48 GMT  
		Size: 5.5 MB (5546323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14` - unknown; unknown

```console
$ docker pull hylang@sha256:5b65395e2deb5991e886c263aea135c06420bffe71ccbf3b56153ab1110c0f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2162417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28b7316f3c15150911b89b6d29d2c36dbc27e9e2ade086eb33f876860e74928`

```dockerfile
```

-	Layers:
	-	`sha256:11e2930fba20fde01461b788a6441ba4946ddabd43bc614c223675b809c6ec98`  
		Last Modified: Sun, 12 Apr 2026 19:26:47 GMT  
		Size: 2.2 MB (2150659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f41af991b44688bb78da9fad6946d0956f8efcb820fe2e1edd3aad7774eef020`  
		Last Modified: Sun, 12 Apr 2026 19:26:46 GMT  
		Size: 11.8 KB (11758 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14` - linux; s390x

```console
$ docker pull hylang@sha256:0cac63336fb4e6bacfe49a130b8f35f4bdc40faeb0e0f589f454420f145ee128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51611017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d17c9af71b834f709db16faa3b0634e382b5be55e771c79f8d1a6d495d5e6a0`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Wed, 08 Apr 2026 17:48:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Apr 2026 17:48:57 GMT
ENV PYTHON_VERSION=3.14.4
# Wed, 08 Apr 2026 17:48:57 GMT
ENV PYTHON_SHA256=d923c51303e38e249136fc1bdf3568d56ecb03214efdef48516176d3d7faaef8
# Wed, 08 Apr 2026 18:02:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 08 Apr 2026 18:02:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Apr 2026 18:02:41 GMT
CMD ["python3"]
# Wed, 08 Apr 2026 18:39:05 GMT
ENV HY_VERSION=1.2.0
# Wed, 08 Apr 2026 18:39:05 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 08 Apr 2026 18:39:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Apr 2026 18:39:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b407be4ef5f30e02ccad96a2ca6c91812f5b7af81dfd8859ae4215d92a435729`  
		Last Modified: Wed, 08 Apr 2026 18:02:59 GMT  
		Size: 3.9 MB (3910076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4af9ba71429e1c2f079c302645e67be023197a5f08822e4a93c5250f9dc79bc`  
		Last Modified: Wed, 08 Apr 2026 18:02:59 GMT  
		Size: 12.3 MB (12319766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2577cd0b2a543814a3af4c449a203682ba350a981a5f0fe8573cc334b0dd8eba`  
		Last Modified: Wed, 08 Apr 2026 18:02:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec709ce392cd7e8d06ca6a9ab3342be1f2952b12776a3667cf4b69eeaf2b6df`  
		Last Modified: Wed, 08 Apr 2026 18:39:18 GMT  
		Size: 5.5 MB (5545508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14` - unknown; unknown

```console
$ docker pull hylang@sha256:a562dcaf9436fb5c520ec5453a7d83daed20527680cb6d2d9f890cf1efbe716f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b76f90cf88a43b08c48aaa3a77aafaf7d00c95dc55856e91952af53f4db4e15`

```dockerfile
```

-	Layers:
	-	`sha256:0f42f3040380d3908f7a3c1dead9ae1a0963cd2c2ee1084e9e9e48969a5d0d85`  
		Last Modified: Wed, 08 Apr 2026 18:39:18 GMT  
		Size: 2.2 MB (2158088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50d3629c9b776f9d7600696b860a0ab06416a0cdc1863622616612ae70716542`  
		Last Modified: Wed, 08 Apr 2026 18:39:18 GMT  
		Size: 11.6 KB (11642 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14` - windows version 10.0.26100.32690; amd64

```console
$ docker pull hylang@sha256:3e050a056e15cbaf59527f272587f688e7bc7abd277d09da492efeeeeee494c5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199728296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dae39329fa555563b5650a09b632273b55aff3bbcc5456b4ed42814eb2021f2`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:02:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:16:04 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Apr 2026 21:16:05 GMT
ENV PYTHON_VERSION=3.14.4
# Tue, 14 Apr 2026 21:16:06 GMT
ENV PYTHON_SHA256=b571567bd11ea98fd7a2cf85791d2c8557a63b1e04e9d1dae665a275cac87f1b
# Tue, 14 Apr 2026 21:16:49 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:16:50 GMT
CMD ["python"]
# Tue, 14 Apr 2026 22:15:04 GMT
ENV HY_VERSION=1.2.0
# Tue, 14 Apr 2026 22:15:04 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 14 Apr 2026 22:15:47 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Apr 2026 22:15:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285db92ff03740292d2e70ef81a1ebcda5d964ee8082b3dfae77c36c2f844e8e`  
		Last Modified: Tue, 14 Apr 2026 21:03:02 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d73b61104fe53636f42fdda064249b89e5aa9a9c8723cf1450c892f066c6f6e`  
		Last Modified: Tue, 14 Apr 2026 21:16:55 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310b698c0137777ec695fb39dedd7fad1425171d94d65657db8c9b473e8e9506`  
		Last Modified: Tue, 14 Apr 2026 21:16:56 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f39335fa67f9d3298c68d3a6737df2874565cf8291d4d7f7029480383e6eb2`  
		Last Modified: Tue, 14 Apr 2026 21:16:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4a08770f1c1762962f2609cbfe35b2d8098c3a1778d9879a0dc26468c5e8ed`  
		Last Modified: Tue, 14 Apr 2026 21:17:01 GMT  
		Size: 61.3 MB (61267975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8d181863f36f7dfe83219f5602e6dd0917ab9f97781f6e66843c1342064f18`  
		Last Modified: Tue, 14 Apr 2026 21:16:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8491e25f537890a0366a61bf48b9b6ed444a5d573f46b70fb8007bda26768986`  
		Last Modified: Tue, 14 Apr 2026 22:15:52 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0907eca094f68730461c96e315f8d11a0572f978e15a1ad492dc51281dcafd7`  
		Last Modified: Tue, 14 Apr 2026 22:15:52 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60f7167d0b4e4d7ad1f352f0fb9d8d3b42b5eede383dc1067b27dea95204521`  
		Last Modified: Tue, 14 Apr 2026 22:15:54 GMT  
		Size: 8.5 MB (8463711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3d723ad538b2b2a27189e362bc3a114c008759aa81fb32fab33f59750bf835`  
		Last Modified: Tue, 14 Apr 2026 22:15:52 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-python3.14` - windows version 10.0.20348.5020; amd64

```console
$ docker pull hylang@sha256:7fd1ddaec914c42ec33bc46b7296a938124c369af74c7e35e0ff3873d680fdc5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2139595501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9edca2e29613512d8f6e7021967611f09da13725f7de0a48d46de149459bf21`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:13:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:26:35 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Apr 2026 21:26:35 GMT
ENV PYTHON_VERSION=3.14.4
# Tue, 14 Apr 2026 21:26:35 GMT
ENV PYTHON_SHA256=b571567bd11ea98fd7a2cf85791d2c8557a63b1e04e9d1dae665a275cac87f1b
# Tue, 14 Apr 2026 21:27:26 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:27:27 GMT
CMD ["python"]
# Tue, 14 Apr 2026 22:17:39 GMT
ENV HY_VERSION=1.2.0
# Tue, 14 Apr 2026 22:17:40 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 14 Apr 2026 22:18:08 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Apr 2026 22:18:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123169191bc868b3dd631fce589535bd12a560eb17f3da89a78dcc3b427e5096`  
		Last Modified: Tue, 14 Apr 2026 21:14:54 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8415de4db98e61c75f40c69540f1a4ebc8d2baff9a3a13fced3a7969e830550`  
		Last Modified: Tue, 14 Apr 2026 21:27:32 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08439f2319bef6d50fd921cb2640df87872aad696f4c6d6f970bc3cde976e22e`  
		Last Modified: Tue, 14 Apr 2026 21:27:32 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d40e1ef00a05272774744ca9493b77c8ac42bb719453b16bd15c64794f6b0cf`  
		Last Modified: Tue, 14 Apr 2026 21:27:32 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23129191cd06d6d760f143093dac47b1339a486bcca350ac31eba49d7c53026f`  
		Last Modified: Tue, 14 Apr 2026 21:27:38 GMT  
		Size: 61.1 MB (61094345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d6b8bedb5bcf85b12a590540f16bb3f3c22f6a8dcef554ca4e679541719692`  
		Last Modified: Tue, 14 Apr 2026 21:27:32 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a414e17c1e6e16df5eee76886afae281443ba7385f27e9c45199e58f27224b1`  
		Last Modified: Tue, 14 Apr 2026 22:18:13 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9407b689f18e28732b2a2b9dccf852ffbe094ede5fc219a76be4b9a16fe1ae88`  
		Last Modified: Tue, 14 Apr 2026 22:18:13 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9e7d269eceeb7e7fa3c03cdc2b9a6d39b98b70b813af7314da36d2fb0dd24a`  
		Last Modified: Tue, 14 Apr 2026 22:18:14 GMT  
		Size: 8.3 MB (8279317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af832cc968afd2bfd7118f25495154daea6b21e640c300b62fd911d69dd08e4`  
		Last Modified: Tue, 14 Apr 2026 22:18:13 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
