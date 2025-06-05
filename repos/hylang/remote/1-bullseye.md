## `hylang:1-bullseye`

```console
$ docker pull hylang@sha256:4a9149f40e7350beb58138459dbb15a36a1f159f01d60fec34983e54777d1fc8
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

### `hylang:1-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:33e7d1707f5bc6e88af7cf6de42878c567e989db5953526e418f4d7eff23b7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56329061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1446372c59818aaacb97b8c9a28945a632c2d76b0721ffdf5abcd744e8f560`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6293c0652e947976499fbe2b5391b0f9dbf1cf1bc26bf1046be1dc6395fc884`  
		Last Modified: Wed, 04 Jun 2025 17:17:10 GMT  
		Size: 1.1 MB (1077878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ff1f692b917cde070856e07b50e58a0a7f39e209a2eca4858ba3bd2069001c`  
		Last Modified: Wed, 04 Jun 2025 17:17:01 GMT  
		Size: 19.4 MB (19380794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ac4101a6ba569659de7a11bfd62b977003925d7992a98cc7e9e631ac9b58b5`  
		Last Modified: Wed, 04 Jun 2025 17:16:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767119fb3dc96c029112bcffb6a50a68cc808c2b6ed38fb9b0e4a59065ffadb8`  
		Last Modified: Wed, 04 Jun 2025 21:20:02 GMT  
		Size: 5.6 MB (5614199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:f2e46a4792d37429d51c0d201120b1521e1f3af74567cbbdc269c0a1d9117c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2744677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52548108c57ff67005afc3b929b46a5d69c4861485369ab87d8da4f29cc60ee9`

```dockerfile
```

-	Layers:
	-	`sha256:c5c4818751a9dffc297c4511cfc5e846dff2cf3a52bd906569eab72831939f1d`  
		Last Modified: Wed, 04 Jun 2025 23:18:43 GMT  
		Size: 2.7 MB (2735433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac613d55733d55d2eccc91e9ee02313b9ffb9b2e36393a28633374482e7e3ae4`  
		Last Modified: Wed, 04 Jun 2025 23:18:44 GMT  
		Size: 9.2 KB (9244 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:79ab264c1d642a5d29a76e2f10ec2e9f5e8ddb813493e320c521156765d702d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49274982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5067a00a65589928dc7537b22d6f453cc0b56f9af5fd8b3fb87ec7356eea53f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2091b63a268a34467e23520ae27c312421298f420abd278e760061e42a678899`  
		Last Modified: Tue, 03 Jun 2025 13:50:37 GMT  
		Size: 25.5 MB (25543902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893d2082ba6089fc5d0baeca7c9b833b7352f591961f4fcb1f57a9ee5853503e`  
		Last Modified: Tue, 03 Jun 2025 16:00:42 GMT  
		Size: 1.0 MB (1042897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae0be319bb9d36021da2c86633d79f2c7099c0f9e86093f67e8b949cb8c626`  
		Last Modified: Wed, 04 Jun 2025 18:29:38 GMT  
		Size: 17.1 MB (17073749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24781450e87d3256048c29c9a86129dfc7210dfcd9e41fa2a8ea6fbb1ece63f`  
		Last Modified: Wed, 04 Jun 2025 18:29:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aac6a649924c161821c3255899911039dd0d3b2468829a9f10754d4ac2d720f`  
		Last Modified: Wed, 04 Jun 2025 23:18:08 GMT  
		Size: 5.6 MB (5614184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:9831d31ceb85f24198ab9e481485265534dbd73ad1431eda49d49cab4cdba0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2748659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c1c736d3e4507934cb21fb99d341c3e0df15de9ccfd64d22d28e26071dc411`

```dockerfile
```

-	Layers:
	-	`sha256:a6e8c24757fead9b9743ac1250e5c9f7af8aa329a66ddba0d125848dfebfff0e`  
		Last Modified: Thu, 05 Jun 2025 02:17:45 GMT  
		Size: 2.7 MB (2739306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5c30c556f31145ce70cbade5989dbe04082db5d6d8d00328be4ff9ff55caec`  
		Last Modified: Thu, 05 Jun 2025 02:17:46 GMT  
		Size: 9.4 KB (9353 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:9b374539258a95a6495661057a1417485707df11c2fa77586732e0d1a20b5217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53912809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94951d3837733dbd266bfb68d79adfe017079f372dcb74aeb31418db7e9aabe0`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f556b47105b4f6df5818b091be6508bc35ab4d8fd1a56c64b0210a091c667a92`  
		Last Modified: Tue, 03 Jun 2025 20:09:44 GMT  
		Size: 1.1 MB (1065681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5311e39098ec57219b204e4015d5232fe280bd22a4664411cfbef62ee8d5ca8`  
		Last Modified: Wed, 04 Jun 2025 17:57:50 GMT  
		Size: 18.5 MB (18486325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71f2224ed0adebfc46d29a47b4b0171502a46c515515474901c794e273d787`  
		Last Modified: Wed, 04 Jun 2025 17:57:49 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9815242b604bac4ff7921779d60c9aaa1f65349874821f89fb93791902de57`  
		Last Modified: Wed, 04 Jun 2025 21:48:08 GMT  
		Size: 5.6 MB (5614296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:7cbeef3b9daf69d235c00dc172e608bd6efcc619b241a7c14094b65f04037316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2745137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f35ab2ce4148b4310f55116bcc6f1500fb7a8bbd8eb24041110d2a9c2a275c`

```dockerfile
```

-	Layers:
	-	`sha256:0b5f3640a00b076406bc1ee6110691423bf3461bc9cda781a1784a95a7dcc86a`  
		Last Modified: Wed, 04 Jun 2025 23:18:51 GMT  
		Size: 2.7 MB (2735740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a562c8b858508bbf1ed4373df00403d67871212dba4b4dfa25561b327fbb934`  
		Last Modified: Wed, 04 Jun 2025 23:18:51 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:1d2062fe63a5fbdc289f286cb6319ad488ddc0facfca4b773c3a77440e9f3e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56992011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283122d18d6565458bdebaeb16e2e7a2a866ffd55ab1ba0d02e9c0a2a8606ea1`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_VERSION=3.13.4
# Wed, 04 Jun 2025 02:30:59 GMT
ENV PYTHON_SHA256=27b15a797562a2971dce3ffe31bb216042ce0b995b39d768cf15f784cc757365
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Jun 2025 02:30:59 GMT
CMD ["python3"]
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Tue, 03 Jun 2025 13:42:18 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be80168f445404444325d3ed7ea809f55e0aa5d3c2b7d78fcac4c01bb69e5bf6`  
		Last Modified: Wed, 04 Jun 2025 17:26:05 GMT  
		Size: 1.1 MB (1090525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2092f440108cb489057983b4128bbcd3b275d8cc2b85bbb7295f53e6695dfa`  
		Last Modified: Wed, 04 Jun 2025 17:26:10 GMT  
		Size: 19.1 MB (19097819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cd12ee90b978c0feb763c372bcf30f7d3bb2a7862e1ae7b3df5636e4d119be`  
		Last Modified: Wed, 04 Jun 2025 17:26:07 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9e89a1b2273ebea3911236c0664a5b896120f49ec18355c9b3ad01e4b34192`  
		Last Modified: Thu, 05 Jun 2025 02:13:50 GMT  
		Size: 5.6 MB (5614216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:e4fc227861f6770f458e29d80194a0652302b21fd9ad69b889d421157c1ec38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2741769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94171e46ac64e46858e75a09337266b1bc59f2dedefdbae90fa0d1986e029480`

```dockerfile
```

-	Layers:
	-	`sha256:1356ad319cb2842e5e651a418522474b7c34b1fdf01439634378f58d23d4e356`  
		Last Modified: Wed, 04 Jun 2025 23:18:56 GMT  
		Size: 2.7 MB (2732576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:388034f47972b4d693843d43c6e49a956852de6ceb2832d4f35a3da016ea6fa6`  
		Last Modified: Wed, 04 Jun 2025 23:18:56 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.in-toto+json
