## `hylang:1-python3.12-trixie`

```console
$ docker pull hylang@sha256:8ea75d77bec990a042ed31e62dbae152649b802ca4c8ab86d0ad82657448099d
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

### `hylang:1-python3.12-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:b3dc325189d7a2fc42e2d97690ac009f2e6fe58cf3b527b827ff289feed526b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48589177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef02d6bd883375cdd2ba548927d5aeaab863695b4c39413f9e423fef136b14f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:02:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:02:10 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:02:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:02:10 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 11 Jun 2026 01:02:10 GMT
ENV PYTHON_VERSION=3.12.13
# Thu, 11 Jun 2026 01:02:10 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Thu, 11 Jun 2026 01:11:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 01:11:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 01:11:27 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 02:40:47 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:40:47 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:40:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:40:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec7f4e699d76dee8107525bf275ad5506fc96ae25aeaf21fbd1633853ed49a2`  
		Last Modified: Thu, 11 Jun 2026 01:11:35 GMT  
		Size: 1.3 MB (1293270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6b2afbcb1ea17577af7be93b9dfd8431a3e3a1dc834ede13df40147db94d77`  
		Last Modified: Thu, 11 Jun 2026 01:11:35 GMT  
		Size: 12.1 MB (12112860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8148c4b61cf7dd8cff2c6146ffb5855f3d0cc2770312e6795a8fd68072e02`  
		Last Modified: Thu, 11 Jun 2026 01:11:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f65e5e83623239bb7e0f01f21abb37d8fa89b2e78fbd2436decaf7689e2074f`  
		Last Modified: Thu, 11 Jun 2026 02:40:54 GMT  
		Size: 5.4 MB (5397383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:a08a3718e5ab30f444efd930f21f2b2de6c7412bd75de9453b6c73f42a89705c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a20c397d71d06f5a97f6dafc90b0f56beb260d4a7ddf5f04841f695eb99c148`

```dockerfile
```

-	Layers:
	-	`sha256:f9ec6ba0f4cb2c5db1c4ccb31ffd6c4ba03227c106e493ce981658bb6a2c28bd`  
		Last Modified: Thu, 11 Jun 2026 02:40:54 GMT  
		Size: 2.2 MB (2155046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060e3d694436189c28a46c8e23c7f9ab94eb4564bff7cab9818bfce74fd4f214`  
		Last Modified: Thu, 11 Jun 2026 02:40:54 GMT  
		Size: 9.3 KB (9320 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-trixie` - linux; arm variant v5

```console
$ docker pull hylang@sha256:e3b2e1d6bbfdcd6e09fc6c0bd792ad2ac555da10b13bb400ed2e5715c928951d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46386499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429e49e2e5b36d52c61deb8a7977dde4d1bf5f25777686a2865e2a0766a388d7`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:45:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:45:23 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:45:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:45:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 11 Jun 2026 01:45:23 GMT
ENV PYTHON_VERSION=3.12.13
# Thu, 11 Jun 2026 01:45:23 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Thu, 11 Jun 2026 02:03:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 02:03:57 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 02:03:57 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 03:05:08 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 03:05:08 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 03:05:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 03:05:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21ad3fc3eb0bb64971b162a0741a8aa22f78c28a0352b8d9715145ca42d13a`  
		Last Modified: Thu, 11 Jun 2026 02:04:05 GMT  
		Size: 1.3 MB (1276372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f805677755633d2c27b486ca8c86c99035e6571544649942b4f1f15cf8fcbcb`  
		Last Modified: Thu, 11 Jun 2026 02:04:05 GMT  
		Size: 11.8 MB (11753161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267834b90c2de2f669c8bcb41b34e114ad1809ffe28e1f6976e2953732d2274c`  
		Last Modified: Thu, 11 Jun 2026 02:04:04 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16dc7fabe8c499577f9f718be43bb96f31a1670ca637f2f5bf691216b73c1a1`  
		Last Modified: Thu, 11 Jun 2026 03:05:15 GMT  
		Size: 5.4 MB (5397517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:a643ccf02f07cd2e9fa3742e4b72ccdb2a537a4178723a7a51b3595754e8fae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452065a2f345adce6d63178e24df33de10c53921d850e08e2ca87ff80e86d916`

```dockerfile
```

-	Layers:
	-	`sha256:625c7fc913e80b10684053ddebdbda38188b8bd6cf983444c387542b507d2927`  
		Last Modified: Thu, 11 Jun 2026 03:05:15 GMT  
		Size: 2.2 MB (2158047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c9ae486e6dec256f9e5f3344a5ffbc2cd009e812759ec06f0a6f995acef2f80`  
		Last Modified: Thu, 11 Jun 2026 03:05:15 GMT  
		Size: 9.4 KB (9431 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-trixie` - linux; arm variant v7

```console
$ docker pull hylang@sha256:bbbf119b7e268fe8f50ba1b8438efca074931afaeaa72735fb8ed357e397ab00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44343866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afef29b282ebeae7d0c1ae5d4eccbc8c55e3ab514dedec82924f06de0822e99`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:16:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:16:42 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:16:42 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 11 Jun 2026 02:16:42 GMT
ENV PYTHON_VERSION=3.12.13
# Thu, 11 Jun 2026 02:16:42 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Thu, 11 Jun 2026 02:33:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 02:33:57 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 02:33:57 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 03:24:38 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 03:24:38 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 03:24:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 03:24:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627872b205e505e6243676d392114700fdde2e76131f2ef9ab8a5014b715c6c6`  
		Last Modified: Thu, 11 Jun 2026 02:34:04 GMT  
		Size: 1.2 MB (1249143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f251cdc202702acf226a46e759cb39dd4a902c4614e3b0a373c104250587fc0`  
		Last Modified: Thu, 11 Jun 2026 02:34:04 GMT  
		Size: 11.5 MB (11485891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe0f7962a1cceb806e02497a9c607b64c24eec231efbe2b7b62bf239119c6ba`  
		Last Modified: Thu, 11 Jun 2026 02:34:04 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbfb1336ce4c785df6fa22e7d526c594e1ddcb78b8564344e27176b068060d3`  
		Last Modified: Thu, 11 Jun 2026 03:24:45 GMT  
		Size: 5.4 MB (5397579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:ad23a3e4011214566eeb45c22529e970b1bab3dac5d91540ce926257d8350fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3ebcc1e4078bba1a0779f1258adc5c832fd16197fe9f3ab85621497dba18cb`

```dockerfile
```

-	Layers:
	-	`sha256:8bfc506dfdce34c2f4a362cdaef7f61e0ea778f264743c54361e0b9a81455aa8`  
		Last Modified: Thu, 11 Jun 2026 03:24:45 GMT  
		Size: 2.2 MB (2156500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de2d6370b454ac59378ad8afff317757e6dc1b0c1c835b780ce444cd9d34b8f`  
		Last Modified: Thu, 11 Jun 2026 03:24:44 GMT  
		Size: 9.4 KB (9431 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:8e3c9c35f473b66d86cc7941ab4b5fcd83ee94077870d19b2950e88b02fa1a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48867824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb2759de3c43cdca0d2d70585acbed7c45bad0e50c47c79319f0f0e2e6d9388`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:04:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:04:29 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:04:29 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 11 Jun 2026 01:04:29 GMT
ENV PYTHON_VERSION=3.12.13
# Thu, 11 Jun 2026 01:04:29 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Thu, 11 Jun 2026 01:15:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 01:15:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 01:15:59 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 02:41:05 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:41:05 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:41:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:41:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1eddb5e68011a990749f44811f33fc197cbb6039bb4928c581e702cf3ef943`  
		Last Modified: Thu, 11 Jun 2026 01:16:07 GMT  
		Size: 1.3 MB (1274128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e02f73c7e903eb192894bbda489b3d715ac484432cdb437d5226ef43b599dae`  
		Last Modified: Thu, 11 Jun 2026 01:16:07 GMT  
		Size: 12.0 MB (12047260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985e4ae0ae203288aecbe2c69d34c26bb0eeda525706e27411041409f7b6485c`  
		Last Modified: Thu, 11 Jun 2026 01:16:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8ed1ee1933f06df2bfa2ecb0a63bd23c03a0d33816f28fe3204b891f3763e`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 5.4 MB (5397657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:e46211b5af1cbb16f2f84d2c45834166d9335aa9448c0696da42482c4f7c4341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59d4a094dfd8556a48bca263404e0bf0dbcc959a6e239c789cb64898444ad45`

```dockerfile
```

-	Layers:
	-	`sha256:fee0e89cfb4632d9a20cb1405bd93c7cf2ebcd8d230fb79db0429d5a80cc389a`  
		Last Modified: Thu, 11 Jun 2026 02:41:12 GMT  
		Size: 2.2 MB (2155352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee6d9a075c96bd1b5e8e0d71886ce0763502d950a3e02131aa64ec9db54494e7`  
		Last Modified: Thu, 11 Jun 2026 02:41:12 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-trixie` - linux; 386

```console
$ docker pull hylang@sha256:ed1f2b56451bb962530a22cd3d48ddb228119afb7b86cb3330b601a6b75642b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50164489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d072984ba27e090f71f6dce533c86a93a14c269df87b76b98f3769661ba58e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:58:17 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:58:17 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:58:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:58:17 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 11 Jun 2026 00:58:17 GMT
ENV PYTHON_VERSION=3.12.13
# Thu, 11 Jun 2026 00:58:17 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Thu, 11 Jun 2026 01:21:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 01:21:03 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 01:21:03 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 02:39:56 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:39:56 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:39:56 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:39:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4d8ae22526a29df67ea1ff98b0259e417a39fcca8d6e8c9133c9a20a4da964`  
		Last Modified: Thu, 11 Jun 2026 01:21:10 GMT  
		Size: 1.3 MB (1297759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6c36a32211223f04c8f754b4598162c0115600e56647dc63be493bc7626a0d`  
		Last Modified: Thu, 11 Jun 2026 01:21:10 GMT  
		Size: 12.2 MB (12167542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7abca0031593210e1962e82c289cb587f9bc3bf98155634a952e1c641f5b44`  
		Last Modified: Thu, 11 Jun 2026 01:21:10 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d51c1f8999aa7f7d017a617d0380db99f279eab238ff7f9fe6a40f542853b25`  
		Last Modified: Thu, 11 Jun 2026 02:40:02 GMT  
		Size: 5.4 MB (5397744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:ad80e732cb66d2963960a743dcd3c5039d92aaff2099c28e65ab6771cfc34034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0f19a9ac03524901b7f7be276578f1c9bdf0f1b138b652ab70c010f5b67e48`

```dockerfile
```

-	Layers:
	-	`sha256:d11a5291f7cb74d5d133b34c4cb41151b161ee4c1b6f18fda3abbe82c29d645a`  
		Last Modified: Thu, 11 Jun 2026 02:40:02 GMT  
		Size: 2.2 MB (2152207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6d51dc57d00208e02c0e15e674bee3a32402badca43fb1d58b4b54231d5c8cb`  
		Last Modified: Thu, 11 Jun 2026 02:40:02 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-trixie` - linux; ppc64le

```console
$ docker pull hylang@sha256:2e8154a3c9a3cf78d893e840a544cb70260f9cc8ad3522349aa1df03be30b45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52826030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583d3fd81cd63c859daa568a5d33392fa570252fc863bb9f9d3018d9b8379d98`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 07:45:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 07:45:04 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 07:45:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 07:45:04 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 11 Jun 2026 07:45:04 GMT
ENV PYTHON_VERSION=3.12.13
# Thu, 11 Jun 2026 07:45:04 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Thu, 11 Jun 2026 08:03:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 08:03:58 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 08:03:58 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 12:34:10 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 12:34:10 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 12:34:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 12:34:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57fbe4f0b9ceabf43c157fcab90b068b7953cc59c03767db856195a2a61e8a9`  
		Last Modified: Thu, 11 Jun 2026 08:04:12 GMT  
		Size: 1.3 MB (1321251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac566aede984a402e98d4c94998b5840507fb5c1f3bec3381a1fb19aa5031bd3`  
		Last Modified: Thu, 11 Jun 2026 08:04:13 GMT  
		Size: 12.5 MB (12500120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a78004da53bab72ee3afb141e3e91364b184a5a3cc0d7f6848fa78ef4f8b143`  
		Last Modified: Thu, 11 Jun 2026 08:04:12 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33100140713c6805dd8c2eaa20e1095f9c471c51a259177d532b5a5f86e46433`  
		Last Modified: Thu, 11 Jun 2026 12:34:26 GMT  
		Size: 5.4 MB (5398068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:7699670dd3d5d49cffee3bf609d22ec67461d85fe1cd64ad1e3f04d161535fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7a4e65965f4793d81704f91d47488f203f47ef4b4ed7b8c035033ab3566f77`

```dockerfile
```

-	Layers:
	-	`sha256:5984551d725c7773b3b325365c4d8fe0e9b1c3f382cfa5e214378948334eb3f9`  
		Last Modified: Thu, 11 Jun 2026 12:34:25 GMT  
		Size: 2.2 MB (2158637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b59639a4f49333fcf80951e3bf99dd6abeb8a3dcd6dc3aeb595d82fa997c3d8`  
		Last Modified: Thu, 11 Jun 2026 12:34:25 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-trixie` - linux; riscv64

```console
$ docker pull hylang@sha256:d65edd0b857c8aebb627fccf29d7637e3539cf8f3b8c5a3e784caeaee22ba67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46953039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542da3bf21a455d8b181b8956dea1c28c7404d7920f3caefe8afcb76d2773623`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Fri, 22 May 2026 03:40:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 May 2026 03:40:21 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 03:40:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 22 May 2026 03:40:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 22 May 2026 03:40:21 GMT
ENV PYTHON_VERSION=3.12.13
# Fri, 22 May 2026 03:40:21 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Fri, 22 May 2026 05:22:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 22 May 2026 05:22:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 22 May 2026 05:22:43 GMT
CMD ["python3"]
# Tue, 09 Jun 2026 09:03:47 GMT
ENV HY_VERSION=1.3.0
# Tue, 09 Jun 2026 09:03:47 GMT
ENV HYRULE_VERSION=1.1.0
# Tue, 09 Jun 2026 09:03:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 09 Jun 2026 09:03:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64887635710bb3720fe7560b7a4d5dad0dfb67a1d1866a9325f82ee51653a45b`  
		Last Modified: Fri, 22 May 2026 05:23:49 GMT  
		Size: 1.3 MB (1261219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e61e96326e564492a678327f7f9be2e3707c4b069d4f6c2597d69b30a6d014`  
		Last Modified: Fri, 22 May 2026 05:23:51 GMT  
		Size: 12.0 MB (12014890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06604e68d10b68994f3195b5b4375e9f69130db9a681de45e9e5a19df6ff0abd`  
		Last Modified: Fri, 22 May 2026 05:23:49 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2322627ccb8436d6ef88f69d8f87a0509f4b730d41be23277874fc68069a09`  
		Last Modified: Tue, 09 Jun 2026 09:04:47 GMT  
		Size: 5.4 MB (5399082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:10a4caf3951e885af9dd9e2e4d4ec67af305c462df3912871239e4eae8c8f439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f84bfc97a1257542059c12b33382d008cd7177b918a56fac3c8497b2ff94b4`

```dockerfile
```

-	Layers:
	-	`sha256:1096ad4102aef8d89b7dd0899cebc94b274cf152ea134aec7041bc48d2345567`  
		Last Modified: Tue, 09 Jun 2026 09:04:46 GMT  
		Size: 2.1 MB (2149008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dceb9b5c729f333052adb6d54beb0faf9d7ba8ff31a7a4ce02936d5610d2540`  
		Last Modified: Tue, 09 Jun 2026 09:04:46 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-trixie` - linux; s390x

```console
$ docker pull hylang@sha256:e7cba934f99b400ed1e0b6c8491c20b68cf990ec9ef77d56165d7981d924a029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48734389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2a3b517aba085ddae6e7256145d8bec0b8896cffb05a70608c6d81a90f3ef6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:35:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:35:51 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:35:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:35:51 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 11 Jun 2026 02:35:51 GMT
ENV PYTHON_VERSION=3.12.13
# Thu, 11 Jun 2026 02:35:51 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Thu, 11 Jun 2026 02:50:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 02:50:48 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 02:50:48 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 04:03:25 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 04:03:25 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 04:03:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 04:03:25 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e6ebe81c809d11446cb9d8ee1dc54cfcefcebce9a4bfd457553a7118acf502`  
		Last Modified: Thu, 11 Jun 2026 02:51:02 GMT  
		Size: 1.3 MB (1305780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e868db70d443038e408d4a35e551495bcb7469258a43b139ffcc4af80cb5ea2`  
		Last Modified: Thu, 11 Jun 2026 02:51:02 GMT  
		Size: 12.2 MB (12179475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f706c5b0ae1b8878bbd96de27bc23a356c45b49af20609b76c0935ffd3d08c`  
		Last Modified: Thu, 11 Jun 2026 02:51:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7940dac2049d221106d539e110921d0d65cd5a76b7e418f952f2f4da9c117c9f`  
		Last Modified: Thu, 11 Jun 2026 04:03:36 GMT  
		Size: 5.4 MB (5397532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:2af904fa12177aa371e8522f6cb579d2ed441a0a72b0a08b80616d989f2e1731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946992ec7ed1ef51bf98ad4d28c0b415141729cf89dd9937af83db701c0a030`

```dockerfile
```

-	Layers:
	-	`sha256:00b247d0de2dab870d9c8c495efb5375b63b15fd32ea6718e5ded8770a42afc6`  
		Last Modified: Thu, 11 Jun 2026 04:03:36 GMT  
		Size: 2.2 MB (2156485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3cef41ee1ceba2f73fa9f882425874a7744710ca97820417f09c7193ceb04fc`  
		Last Modified: Thu, 11 Jun 2026 04:03:36 GMT  
		Size: 9.3 KB (9320 bytes)  
		MIME: application/vnd.in-toto+json
