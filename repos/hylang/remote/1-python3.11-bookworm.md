## `hylang:1-python3.11-bookworm`

```console
$ docker pull hylang@sha256:4a5fe405d9aab8f48946fd264e24f16c5c0b2bee008d79676136d0f763c51cc8
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

### `hylang:1-python3.11-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:d1f3e82230020adbd720799ea015ba5a615799329ba685596083bb0c32ffab3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53338656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1f3e19b324ec60226d6a6a3fab1e16b3eadf10e478c8957f0e1286a508aa8d`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:44:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:44:29 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:44:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:44:29 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 00:44:29 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 04 Nov 2025 00:44:29 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 04 Nov 2025 00:52:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 00:52:57 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 00:52:57 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 04:34:13 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 04:34:13 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 04:34:13 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 04:34:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93300bbaa9a608654264bc3b927e30b7a83fea02177f2e9b329363552420a8ad`  
		Last Modified: Tue, 04 Nov 2025 00:53:12 GMT  
		Size: 3.5 MB (3515896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5c0390855fa5cc721b77436b5d5fb444021875fbb3590d0046d93e289e4259`  
		Last Modified: Tue, 04 Nov 2025 00:53:12 GMT  
		Size: 15.9 MB (15924890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f590d3d1259b9e8452aa4f67a6713138c1c81a4ac191be89113eda5d7bd98a`  
		Last Modified: Tue, 04 Nov 2025 00:53:11 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79903c2255dd00d9eec52b447d2824067594bcc5d031fe6356865bc1de2ea306`  
		Last Modified: Tue, 04 Nov 2025 04:34:27 GMT  
		Size: 5.7 MB (5669055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:4d6306d836d257fa8595eab80447b62fafbe76f06fd813ea471023a912e4c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c3c6fc2f1e8cb43a924a5c7f0eed14bbd7acceb6f59b8950abc4c814617698`

```dockerfile
```

-	Layers:
	-	`sha256:693a65f6a35f21c034cfd08c161f114162c8165403da1a452b0055a3c74e1169`  
		Last Modified: Tue, 04 Nov 2025 09:18:50 GMT  
		Size: 2.6 MB (2622984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ee425576f132e95d47bb3c9636223539d83285b4ac05ec21e724bd3f634b4b0`  
		Last Modified: Tue, 04 Nov 2025 09:18:51 GMT  
		Size: 8.1 KB (8094 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:0ce05167f37995e642b7235f525bfc8a0923a5bd5504df9899b0d44b2275c4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49860173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde6e403a93aae111fa2c66c674d43cb900928aa97ca017eb42fe8951d12a562`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:46:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:46:43 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:46:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 01:46:43 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 04 Nov 2025 01:46:43 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 04 Nov 2025 02:03:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 02:03:04 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 02:03:04 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 03:03:31 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 03:03:31 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 03:03:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 03:03:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:def4b77141116a067c72a4f39eb9fa70634fe918be6e3df3cf0bc46323be22c7`  
		Last Modified: Tue, 04 Nov 2025 00:12:34 GMT  
		Size: 25.8 MB (25757661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5201ca5b28e4d29e6f3d0e349c32b35bdacb2abdeeac6cf7861eb7ef7ac3d07b`  
		Last Modified: Tue, 04 Nov 2025 02:03:26 GMT  
		Size: 3.1 MB (3090747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c002ef355bb9ecf9099060431d0f238185e6c4a09fa3f926007359b06d744e0`  
		Last Modified: Tue, 04 Nov 2025 02:03:29 GMT  
		Size: 15.3 MB (15342044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0d4b16a554cb694bee32c3d65fcfe98cfbd25887aa0e32d7558e7d09a16a38`  
		Last Modified: Tue, 04 Nov 2025 02:03:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1b9b02453cf938176ea6a0b8d041bfabe1e64180aeec5fe1475d8519cedab0`  
		Last Modified: Tue, 04 Nov 2025 03:03:48 GMT  
		Size: 5.7 MB (5669474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:35c4d3645e52c2767b1717e47e6b4aa04a6573f252f7977cb1e901274f148999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22b1327fdeaf3f6bb1b59ce0da5689383cb62af06e14af9198f9508677579f2`

```dockerfile
```

-	Layers:
	-	`sha256:470227deb26a56cd5928d952a43974b0332d51fedca78c9a044e3b22066490b3`  
		Last Modified: Tue, 04 Nov 2025 09:18:54 GMT  
		Size: 2.6 MB (2626804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:982bf380594d4831502ebb7af71a09780e25ce2fae4043991da5f268b5305e3f`  
		Last Modified: Tue, 04 Nov 2025 09:18:55 GMT  
		Size: 8.2 KB (8174 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:ef7c0783a0697df893141edeaee75a4b42746e2c61d425bc63248e71c03b3428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47449876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bfb2358d8f1dcadb3397ee6fb1ddba8b591f4437d731e1c173c0889a10d0f2`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:05:35 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:05:35 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:05:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:05:35 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 01:05:35 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 04 Nov 2025 01:05:35 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 04 Nov 2025 01:22:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 01:22:17 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 01:22:17 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 03:05:40 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 03:05:40 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 03:05:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 03:05:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99495ddaefc77f94e485d9e161c9ea774fc0d959795525976ee6d64591b1a06`  
		Last Modified: Tue, 04 Nov 2025 01:22:31 GMT  
		Size: 2.9 MB (2925464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8def9eb95b8efed55504a092bd5d328d24f33ba74d6dad9021b00c1d9ce8f4`  
		Last Modified: Tue, 04 Nov 2025 01:22:32 GMT  
		Size: 14.9 MB (14920999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559e33cd72edc18871d4057a75a90aef54719afd549cffe30c44f0c6ec95bc72`  
		Last Modified: Tue, 04 Nov 2025 01:22:31 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cdde97c9bf505f5ab825098288d66f6da5c44245de4b658c011ea63aa17439`  
		Last Modified: Tue, 04 Nov 2025 03:05:54 GMT  
		Size: 5.7 MB (5669039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:243eb3535d7414ca8be85b99d0a65752e057f9dd59635abd1e2e7009b5ffc8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c17053a0c5a17b5ea5a10815054df97ba576b5a218c4ae135b0d5227d8ce39`

```dockerfile
```

-	Layers:
	-	`sha256:fe69189ba250d0a800b9959f7f4d6a7b961f82a5bc0a845c80eb5a1dd4c19e50`  
		Last Modified: Tue, 04 Nov 2025 12:18:48 GMT  
		Size: 2.6 MB (2625253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9acf976cb01798523998cd88b4bb91fd7187a2301be6c62f38b3af6d31d9ffb`  
		Last Modified: Tue, 04 Nov 2025 12:18:49 GMT  
		Size: 8.2 KB (8174 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:33fc470c73f79ad9d5e265733bca5573813a8d2a4d0357498c4b5d9edab337cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52985865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b2aaebc2f905d86fe23196ce0ce0e1f925205e137a89d7e9d2fbc3f4a30d80`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:45:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:45:43 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:45:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:45:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 00:45:43 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 04 Nov 2025 00:45:43 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 04 Nov 2025 00:56:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 00:56:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 00:56:34 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 01:49:13 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 01:49:13 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 01:49:13 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 01:49:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a55acfaeea192f4fc92f806c4e0c6166344af12761d9066ea67c3ae5a9370e`  
		Last Modified: Tue, 04 Nov 2025 00:56:50 GMT  
		Size: 3.3 MB (3349175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c2416e54fe6c8b413e93afc29060948cd59f744ea44d3d5ddbd0907788d81c`  
		Last Modified: Tue, 04 Nov 2025 00:56:51 GMT  
		Size: 15.9 MB (15864813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6047e63ff5f92b72a0bdb7d4928374485fc72a3f1c695f2fad4ab39556d52ec8`  
		Last Modified: Tue, 04 Nov 2025 00:56:48 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1945c1dd395daef56fd8679bf7cd9f5cd183d94c8d6c0bd921987de1fc53e4`  
		Last Modified: Tue, 04 Nov 2025 01:49:26 GMT  
		Size: 5.7 MB (5669254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:5b30d6bcfbba408d216488dd67ad92b24de6cb9bf072df683e5100922035887d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fd71d590f42b2ff6c5ef75d8eca663d64840cbe5b97f32aa18066f64a9335e`

```dockerfile
```

-	Layers:
	-	`sha256:1536df02fff33fecf8c3ae59e10b5d84017f063726775993ff8a3d83f683bb80`  
		Last Modified: Tue, 04 Nov 2025 12:18:53 GMT  
		Size: 2.6 MB (2623257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f53c204dc37e2016db613604feadc504861e1bb145d7b0e45a3aa7484c14ad85`  
		Last Modified: Tue, 04 Nov 2025 12:18:53 GMT  
		Size: 8.2 KB (8197 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:8870f7a9b43c0643a0b49b185aa4b3ffa774170ae8e0dda160ea04299f12e610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54561516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486611b79305fe30d02eeedfb1b1f32f962d94d1a1723935565105d4d8a968a4`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:35:56 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:35:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:35:56 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 00:35:56 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 04 Nov 2025 00:35:56 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 04 Nov 2025 00:45:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 00:45:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 00:45:01 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 01:50:12 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 01:50:12 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 01:50:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 01:50:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f45b1830c6e874fb84538aab2dd209d6e2c3fc3ad6988daca5a1110be018f`  
		Last Modified: Tue, 04 Nov 2025 00:45:17 GMT  
		Size: 3.5 MB (3516544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32481f710350b51bb2d4f7e332b23d0f8310a11b6273bc5a4b29af46c450d05`  
		Last Modified: Tue, 04 Nov 2025 00:45:18 GMT  
		Size: 16.2 MB (16165814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff80051e0778e26c663893c78a01990dc371751c8d801df0825fd184850108f`  
		Last Modified: Tue, 04 Nov 2025 00:45:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b6ba66530d1c38f68b585ef9a97151bcd69f0b4794601c767cc81430f9493d`  
		Last Modified: Tue, 04 Nov 2025 01:50:34 GMT  
		Size: 5.7 MB (5669064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:4c980cfaa44212a458a6bad1980c95dbb188c904a10b3a234810a3621254bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945d6606001ab89b9a685b3271b9976ce61ebb72d431d79d5a50734c7c0f8946`

```dockerfile
```

-	Layers:
	-	`sha256:6ef1d2d186e5260091a254b26d9ffab25cbab63b208cfabcf156f960065dee53`  
		Last Modified: Tue, 04 Nov 2025 09:21:33 GMT  
		Size: 2.6 MB (2620135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:937705fadd42fb9da2d776caefd783ad8f4d36d41ddaa7d2d4fae39240afb120`  
		Last Modified: Tue, 04 Nov 2025 09:21:33 GMT  
		Size: 8.1 KB (8062 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:b656d1957c425eab30a2116410f4d33902e6e9f5ecfaebde1205705a0345edb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (58026251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e5cfeec0222507287f62c009bf9deefca6ae1299b154dd3e446ba082492971`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 10:52:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 10:52:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 10:52:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 10:52:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 10:52:14 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 04 Nov 2025 10:52:14 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 04 Nov 2025 11:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 11:49:42 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 11:49:42 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 20:06:54 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 20:06:54 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 20:06:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 20:06:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1624bff9c7835fe916701479dd582305a8fdfd055e9e01e7a71e11540110bb`  
		Last Modified: Tue, 04 Nov 2025 11:13:39 GMT  
		Size: 3.7 MB (3721120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1f118df130468482a3ceb13e848c9ccaea696dbb996aba3552440aecfff4de`  
		Last Modified: Tue, 04 Nov 2025 11:50:23 GMT  
		Size: 16.6 MB (16566273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ac4f447251692077aafbbb7e604689ee14d60418da9975a63f3d4e456c3d05`  
		Last Modified: Tue, 04 Nov 2025 11:50:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fd6e0c556875f437f0808e8600a57569e554da3dc2676afd495f655f3324eb`  
		Last Modified: Tue, 04 Nov 2025 20:07:15 GMT  
		Size: 5.7 MB (5669704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:fd7fde8c126e69736ea91646ef4fc7ddff75cb25acd246ff1380617ff5f0df70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40af539468fa236818954dfa4cde49666eb39872cb611b432bfa6fdb41d2374`

```dockerfile
```

-	Layers:
	-	`sha256:84faf28b76ed870caee0ca3ff729ee2272ea094d40823e0055e82dd18ff6d9a9`  
		Last Modified: Tue, 04 Nov 2025 21:18:46 GMT  
		Size: 2.6 MB (2627490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b0ab8fb6f4da7b9342cb438119722d4bd6ccda6299e344c7e0774a035dc12f`  
		Last Modified: Tue, 04 Nov 2025 21:18:47 GMT  
		Size: 8.1 KB (8138 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:f1fbd0331b56e1861856ebdd26950e2ebdcf28ce135c7093805059f30365c3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51499758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f9f0c565e198639b71ddec7fcd0978210d368d94b0cea6037dca034893090`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 05:28:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 05:28:42 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 05:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 05:28:42 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 05:28:42 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 04 Nov 2025 05:28:42 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 04 Nov 2025 05:52:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 05:52:51 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 05:52:51 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 13:41:32 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 13:41:32 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 13:41:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 13:41:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f30c665d3e8773547abe33ad871b3bc816ee85876f7308da9a2b467a93cbe87`  
		Last Modified: Tue, 04 Nov 2025 05:41:38 GMT  
		Size: 3.2 MB (3181831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa743db87e45ee38785f83eb592499e3535e8897a8602e101e6424487ec8d96`  
		Last Modified: Tue, 04 Nov 2025 05:53:15 GMT  
		Size: 15.8 MB (15763780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc2e361780d1296f6c0f9affd90705023cf66d682c36ae1d8110107c6307eeb`  
		Last Modified: Tue, 04 Nov 2025 05:53:14 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df119515aa9d4c35d94e68f9cb9caef094e710d043d06c49192cfa8c88454462`  
		Last Modified: Tue, 04 Nov 2025 13:41:53 GMT  
		Size: 5.7 MB (5669348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:e6cbd0663feb9f749f4cf7fe2ff2f0a990786426e41cb048b6790fc451beaafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1361d5e5de9e0933774e2c6d52ed4590a54092d2b0d51ccb62bc5e58bfe2df23`

```dockerfile
```

-	Layers:
	-	`sha256:1a5f9d337bd2eff04fb4c3af3fc21600ab43a29f93bf34e4bc4f59cba29ca58b`  
		Last Modified: Tue, 04 Nov 2025 15:18:11 GMT  
		Size: 2.6 MB (2619800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d838719778c33f5b285fc66fb0055514a3dc13698459d367931e3ec0311ab850`  
		Last Modified: Tue, 04 Nov 2025 15:18:11 GMT  
		Size: 8.1 KB (8093 bytes)  
		MIME: application/vnd.in-toto+json
