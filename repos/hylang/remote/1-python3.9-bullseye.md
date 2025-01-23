## `hylang:1-python3.9-bullseye`

```console
$ docker pull hylang@sha256:12516d5ca0de36bebb51ebc7e268d4a7bd142f82d7c6a23f71e9699cb3400ff9
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

### `hylang:1-python3.9-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:4ddeaccc181265f3c5f8da5c4e804487c66f4ef18f2b4708c103598732dff443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48923506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06a586c7a3cd249de135001d290112a4709c08aeec6f49d5fedf6b297724580`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acbab8b9daf716b5c9dddf8c179fc53523dc89b65138cada78d23065adb71bd`  
		Last Modified: Tue, 14 Jan 2025 02:23:26 GMT  
		Size: 871.2 KB (871229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64b42dae4e0a91fe31d884d81298910395edc7476ebb5f1333678f7564a2b8b`  
		Last Modified: Tue, 14 Jan 2025 02:23:26 GMT  
		Size: 14.1 MB (14129438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dcd8de72233594d2f545dbd77ac76dfbc556343a4cae279f9146bce19ba35c`  
		Last Modified: Tue, 14 Jan 2025 02:23:26 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94473e18711a51b1159f0b3a4d1248d98a644ccb77cce4daf0d6de80af297ffd`  
		Last Modified: Thu, 23 Jan 2025 01:28:12 GMT  
		Size: 3.7 MB (3669924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:5d0a5a0598969acab251f2992bd5ce6b884e073052ec72afb2bb64e75342c2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6491cd53c276b4c61a6baa0a8cb89e85d4e8405cd6ea072128437d8c7f22a63e`

```dockerfile
```

-	Layers:
	-	`sha256:f4424d5cca9bf1b53c21e74a9ace330dcddc82f2e71083f5187ce7d398adf62d`  
		Last Modified: Thu, 23 Jan 2025 01:28:12 GMT  
		Size: 2.7 MB (2715164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb54200f94d0c42421447bd4eece24df8d66c79869e56444e2022dd40c12f98`  
		Last Modified: Thu, 23 Jan 2025 01:28:12 GMT  
		Size: 8.0 KB (8015 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:891241c600b00cbd079eeb8b2155ddc77e631669ed6f02d375ba7a1b210d7496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43371175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee35b3258482ded5a05ad522d0e366550d50166364fd0db51d5bac892a243215`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff9a61bca8b14aca8b1bfd74b3e8d00eff62671763a71563fdcb5bee1b23d20`  
		Last Modified: Tue, 14 Jan 2025 13:24:35 GMT  
		Size: 837.0 KB (836977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd63e6be4b5f090303ec7aada426eae19471700e79b588b9cda70a1542ed416`  
		Last Modified: Tue, 14 Jan 2025 14:54:08 GMT  
		Size: 13.3 MB (13329952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25954110ddd0c8fe5819aa875461e0b381252983abd80d63ae50009e94c9e28`  
		Last Modified: Tue, 14 Jan 2025 14:54:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d281bd040285eb31b1241e4d19a17b5725639f8632418a8432ab975f9dd0b0`  
		Last Modified: Tue, 14 Jan 2025 21:44:15 GMT  
		Size: 3.7 MB (3670036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:fc000a3fb568bc11d2c77b798728ff6dd01b14ec822d2585a2d6289a00d85ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6e82fbf72511e3fb0952c9242c2eec5608f20571e747daf5c3185b8c6aaa30`

```dockerfile
```

-	Layers:
	-	`sha256:c95ff99a445e90ba8361ad7b2d8a47a97d62f6170d9186c002ed9720575ac201`  
		Last Modified: Thu, 23 Jan 2025 05:16:40 GMT  
		Size: 2.7 MB (2717409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb36373e2305ca45c8a4ea3f44b16a05186f8f2b1d4b33fddb6d83cbc6d7b673`  
		Last Modified: Thu, 23 Jan 2025 05:16:40 GMT  
		Size: 8.1 KB (8090 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:9cf452750581e254bfe1a40913825d732f282f813e2ebed24e847856ffb16059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47416287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31e6710a8b1cd92c64c3e709bac3f46d98d5c3731ff75a6dc9b54ff8173a7f6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64757e3dbded90ef62713320bdf990f6a446c544004f498e303e366605b97b2f`  
		Last Modified: Tue, 14 Jan 2025 10:33:50 GMT  
		Size: 859.2 KB (859151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7a4e463481f453543874e70d491ce9613bf014309e2cc28e3aaae166cd8549`  
		Last Modified: Tue, 14 Jan 2025 11:24:11 GMT  
		Size: 14.1 MB (14141970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d1314a043187f0181e3572f0fb507a05c09d78120622b7175a614214c3da16`  
		Last Modified: Tue, 14 Jan 2025 11:24:10 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bca48efbe5737d923b962bfefb97f7e80e0b3fb48628accb9883286d00dc3f`  
		Last Modified: Thu, 23 Jan 2025 04:16:56 GMT  
		Size: 3.7 MB (3670003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:429d427a272b9aa7e6308fa918183e139ea5b1fd5fee2eec51d37c1fea9697ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf76fd6b4d5d87b61c4d03c07934d6c0f5e83423aad86da32cefa58afe93653`

```dockerfile
```

-	Layers:
	-	`sha256:f09f3d715b3431797176c945ecfc2b907b2fa1704a22f10d8519ebc5a6e4bc4e`  
		Last Modified: Thu, 23 Jan 2025 04:16:55 GMT  
		Size: 2.7 MB (2715423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb490716b4497d6c302ca7f4a1001f3dbcec3eb287316b71fc12332d340d5144`  
		Last Modified: Thu, 23 Jan 2025 04:16:55 GMT  
		Size: 8.1 KB (8116 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:07f164aeab269d96cb988d210de927d9fb8a585cc8a27e7e6f8898c0725bebfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49973007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05fbf6ac6faf6db582ef490f96279295801ab5a3f9e402840b87002488a1adc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7434a50832232bc3315fa54cdba2f7e0114d8583c03d05075b0c302d4f2d8792`  
		Last Modified: Tue, 14 Jan 2025 02:43:56 GMT  
		Size: 884.1 KB (884052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc719991804e03e11db0b5887201e4b7e1bd94defd199286aef27dd8bf60cd3`  
		Last Modified: Tue, 14 Jan 2025 02:43:57 GMT  
		Size: 14.2 MB (14239449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba6069bd5c8a6c1c60d793aaa5c187d12646c2f8c9693588a642dc5c555e3f5`  
		Last Modified: Tue, 14 Jan 2025 02:43:56 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f66e61b2ffc776530c835a6eb25cc69242287a3c0b7ef8973fd995f43ab7ce`  
		Last Modified: Thu, 23 Jan 2025 01:28:14 GMT  
		Size: 3.7 MB (3670227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:ce4fdb7b8d294f25959dfd163bd046281e9f54826bc48d9ac488c9f25d5d3bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45594a7cdac0b560722ca1f77f9a428cc90526a78a91f6315f51c7c0422d8fd8`

```dockerfile
```

-	Layers:
	-	`sha256:4563676d2f10b74075d875e040394849d7104cc3bd3d52a0999be533c65da232`  
		Last Modified: Thu, 23 Jan 2025 01:28:13 GMT  
		Size: 2.7 MB (2712276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da0a2dcfc41603eb5271d6d8776853dc98095905cd9b4a3e92b1db7a78c7bc54`  
		Last Modified: Thu, 23 Jan 2025 01:28:13 GMT  
		Size: 8.0 KB (7983 bytes)  
		MIME: application/vnd.in-toto+json
