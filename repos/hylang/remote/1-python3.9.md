## `hylang:1-python3.9`

```console
$ docker pull hylang@sha256:760a9b0ab2611fe5f1824c4fcba798b4094180b3e04cb0e5cbc086291692e560
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

### `hylang:1-python3.9` - linux; amd64

```console
$ docker pull hylang@sha256:a1e745b339da21f7242540d8c1c69cd0658599914e4037958f029450fb1dc70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48672546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133115b2072f367811106a37055db922c11957395a2da99f7dc04ca52434a88`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 31 Oct 2025 23:14:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:14:26 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:14:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 31 Oct 2025 23:14:26 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:14:26 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:14:26 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:17:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:17:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:17:23 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:56:24 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:56:24 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:56:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:56:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ec39b36ae8c03a3e09854de4ec4aa08381dfed84a9daa075048c2e3df3881d`  
		Last Modified: Fri, 31 Oct 2025 23:17:36 GMT  
		Size: 1.3 MB (1292953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74430849022d13b0d44b8969a953f842f59c6e9d1a0c2c83d710affa286c08`  
		Last Modified: Fri, 31 Oct 2025 23:17:45 GMT  
		Size: 13.9 MB (13884816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea56f685404adf81680322f152d2cfec62115b30dda481c2c450078315beb508`  
		Last Modified: Fri, 31 Oct 2025 23:17:36 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784123c0e266175a789b806eba22f1f485837135f2340680702188c29b4b00fa`  
		Last Modified: Fri, 31 Oct 2025 23:56:37 GMT  
		Size: 3.7 MB (3716602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:946d83a73331d6fd29c15f41150a0a27002d12904dab50dd8773fe218acf3c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f0b966c88f0ec595202d63e9906aebe537fa32d22d7354e5aac80af8373441`

```dockerfile
```

-	Layers:
	-	`sha256:f8ff8b671cf9d044cbcec6e3195998489de28453bfb5a6b316a9e78f9623682c`  
		Last Modified: Sat, 01 Nov 2025 02:18:40 GMT  
		Size: 2.2 MB (2199877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343c043a072645a9ed6e0b46606001cb7d67a1c414b67e1bd3083ea77542f07f`  
		Last Modified: Sat, 01 Nov 2025 02:18:41 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; arm variant v5

```console
$ docker pull hylang@sha256:7c009bcee9083b6a043a2a7a5b1ae5024ce37b5b34413b69efa48de701d2888d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46466029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57cc662b536ffe1936aa235fec79cafef31c9bd9cff96a61f0e61b08e54e8ca6`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Fri, 31 Oct 2025 23:14:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:14:38 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:14:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 31 Oct 2025 23:14:38 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:14:38 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:14:38 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:20:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:20:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:20:34 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:56:17 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:56:17 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:56:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:56:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92e4a34f3d13410d79a22c357d921e05e1a3af304e544e352e07d6caf5ddee6`  
		Last Modified: Fri, 31 Oct 2025 23:20:48 GMT  
		Size: 1.3 MB (1275850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac16be0136378454d5c3ff4ddbb3d003fd5a7088dcb1a0300476d9b9e93aa42`  
		Last Modified: Fri, 31 Oct 2025 23:20:50 GMT  
		Size: 13.5 MB (13526947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd274c0de9e8b15842dccbd1945c5dc7498a3870aa7d13f7eb9abdba4265346`  
		Last Modified: Fri, 31 Oct 2025 23:20:48 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a5d58aea386e0f439fde25bb3c014fd0279fb8fc2c06a50883886f1c5af64`  
		Last Modified: Fri, 31 Oct 2025 23:56:33 GMT  
		Size: 3.7 MB (3716698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:2e75815e520159bcc1bf250e5eb1eacd2b17591f228d9edd934db79b41ebf371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfe56cd271f7571d4a81b15d30406d05c1f695d0dcb1dd14740a95e0b32f315`

```dockerfile
```

-	Layers:
	-	`sha256:85b913cbfc456311aa668a914714bbc32bd01882f07db087cbb444935f04903a`  
		Last Modified: Sat, 01 Nov 2025 02:18:45 GMT  
		Size: 2.2 MB (2202878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e939b6deaceb6626e6c5254739888a34f317afec1db077b9c254a24552897377`  
		Last Modified: Sat, 01 Nov 2025 02:18:45 GMT  
		Size: 9.4 KB (9408 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; arm variant v7

```console
$ docker pull hylang@sha256:a979dddb0a97cfd6f83dd93417efaaf35a303da1328b7f9fcfda0160ab8d4a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44452569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174b0ea4303cc6cec95753cec9e5af2248d40c6f86f83a23658efd449d2c3538`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Fri, 31 Oct 2025 23:14:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:14:32 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:14:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 31 Oct 2025 23:14:32 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:14:32 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:14:32 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:19:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:19:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:19:49 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:56:06 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:56:06 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:56:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:56:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e32008df04b762f42ee979daf452716caba37d02948d35e388fe9f9bb54269`  
		Last Modified: Fri, 31 Oct 2025 23:20:05 GMT  
		Size: 1.2 MB (1248428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38767de1a42d7c1f5a6a8e14f3ce4413a9d1069b7fad01cc2c5824c9653dcc99`  
		Last Modified: Fri, 31 Oct 2025 23:20:06 GMT  
		Size: 13.3 MB (13274307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68aaccb6b319afe57a72d045952121e0ad0284bebfd39041920890fa26ef417b`  
		Last Modified: Fri, 31 Oct 2025 23:20:05 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a74d40c95807e8e7b5d620e3cb05e4df1fd91324330ffbe6e9cd93239120723`  
		Last Modified: Fri, 31 Oct 2025 23:56:22 GMT  
		Size: 3.7 MB (3716689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:eeada379d5a21e10a3eb2849125279dfc590d3b841193b9ccea698c801d2bd39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa812f138d4d90016c25c9855e8407f29231c33f16a7655fc25ee144124f104`

```dockerfile
```

-	Layers:
	-	`sha256:2d4f1d90a3633805b15b0bdc78cd6e368d09382919d192bc66e390a6d16268d6`  
		Last Modified: Sat, 01 Nov 2025 02:18:49 GMT  
		Size: 2.2 MB (2201331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c93e3bdee39ff652807fc2e33af5c391fa97229a9a7cd0dff37bd0d485317f21`  
		Last Modified: Sat, 01 Nov 2025 02:18:50 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:1d23f86bf9b48d7dea2b6e6c28590f5422a1584dc5002b9b3ab3404418ec4df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48961476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2eb2147347d02dc283a95c5662eb7fb865cd76c488018f804f86d0e973bf29`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 31 Oct 2025 23:14:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:14:03 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:14:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 31 Oct 2025 23:14:03 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:14:03 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:14:03 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:17:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:17:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:17:37 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:54:51 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:54:51 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:54:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:54:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479b8ad8bcc3edbeba82d4959dfbdc65226d5b55df3f36914c68455762bf924c`  
		Last Modified: Fri, 31 Oct 2025 23:17:50 GMT  
		Size: 1.3 MB (1273584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfe7d4fa0c501a81a5ba6d1e1e2958e4b005d3ce3827b0adb869d47b8c51229`  
		Last Modified: Fri, 31 Oct 2025 23:17:51 GMT  
		Size: 13.8 MB (13828984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f4b50347300e01a1a1da6dd0266adcf8e44671002ad28c2386cb6557943d6`  
		Last Modified: Fri, 31 Oct 2025 23:17:50 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc41b990764bee32a53bf5bbe5beea40b2483acf264a4104ba12cd894195938`  
		Last Modified: Fri, 31 Oct 2025 23:55:05 GMT  
		Size: 3.7 MB (3716530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:a411cac11f75734482155f6ca42f4c8201f4d955bc4de542d69a9eb1bac409cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff34ffaf2e609dd8aa41347d0f755e68635291cf0d6b1a70a739333a51f2b65c`

```dockerfile
```

-	Layers:
	-	`sha256:0089ce753963a9df1205085e94ab96c510b0ebeb536428e99f6b0b79de4c2eb0`  
		Last Modified: Sat, 01 Nov 2025 02:18:53 GMT  
		Size: 2.2 MB (2200191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f5567f7ca52973dcbe1a61b756853e78da4560e511d638fb49df5d9b8bcd4d6`  
		Last Modified: Sat, 01 Nov 2025 02:18:54 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; 386

```console
$ docker pull hylang@sha256:1ca6008c03eeba6ec128db4b22e751b30a26eefaadf8b9d28e13a90e62494517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50237551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfda2e35f7d3273012caddfba3a7d67c02c91f3d0bd7403c633b1177c644c2d`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Fri, 31 Oct 2025 23:24:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:24:36 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 31 Oct 2025 23:24:36 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:24:36 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:24:36 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:28:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:28:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:28:47 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:56:04 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:56:04 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:56:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:56:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcd73ce769ac866dc7902fc45045ce24f9d59911499d9575fe914e9bf5d25da`  
		Last Modified: Fri, 31 Oct 2025 23:29:01 GMT  
		Size: 1.3 MB (1297120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16768d22e6a0373d35b5d2d70262056ca97ce3d526d74c1b2385b0b2f0a914c1`  
		Last Modified: Fri, 31 Oct 2025 23:29:02 GMT  
		Size: 13.9 MB (13928975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c69f3d2d2e68fd4633af3b23323fd3ed970a1bb225f7056ca57bc416014cb48`  
		Last Modified: Fri, 31 Oct 2025 23:29:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0722df40605ba7063a0d9417dc0342c06ec8ef684b3fbc7b4db3995ca5db5b56`  
		Last Modified: Fri, 31 Oct 2025 23:56:23 GMT  
		Size: 3.7 MB (3716577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:3c56d917d459756be50ccf254f6d15ed06a70e1553ec37edbc18184c3c23059a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229858cb763f926c0d8d484ba954cf48403799aa2135319607767d6d3915dca9`

```dockerfile
```

-	Layers:
	-	`sha256:02a9b69375d2a26b545ffb5a7e647693325fe1efbed5e68e130ecbe3af95ee8f`  
		Last Modified: Sat, 01 Nov 2025 02:18:59 GMT  
		Size: 2.2 MB (2197038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25e10179ddc123ce8c6de5def178e097c34bc28a4bbb5d4f39c6144fbd535a58`  
		Last Modified: Sat, 01 Nov 2025 02:18:59 GMT  
		Size: 9.2 KB (9244 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; ppc64le

```console
$ docker pull hylang@sha256:1af70546ed57a5fa30050ea6a14a0153b0d55967f5f805424418e84944b5eb49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52859229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf723a62748fa5cfdd68c730e2e41f859e33e46243c7e2d6f93d3020deaf76f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Tue, 21 Oct 2025 12:26:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 12:26:01 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 12:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 21 Oct 2025 12:26:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 21 Oct 2025 12:26:01 GMT
ENV PYTHON_VERSION=3.9.25
# Tue, 21 Oct 2025 12:26:01 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:26:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:26:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:26:13 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:55:14 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:55:14 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:55:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:55:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb558dffcc860262e2beb67e32665bd21619cba0fcdc6a241d92e98e82bc66c3`  
		Last Modified: Tue, 21 Oct 2025 12:43:45 GMT  
		Size: 1.3 MB (1320968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fba89b5bb517a8eadc6556059a2aca4358d3c571241512b633842a856b2ee33`  
		Last Modified: Fri, 31 Oct 2025 23:26:39 GMT  
		Size: 14.2 MB (14222649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a97a8ce8fef8d902a4c81f6940e663f72d4c314ffcdaabf0811af4e202f16d`  
		Last Modified: Fri, 31 Oct 2025 23:26:38 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41355c0a7d83abe5665d507ec470f4a217885a81b1b1031f491662e7efe2521d`  
		Last Modified: Fri, 31 Oct 2025 23:55:45 GMT  
		Size: 3.7 MB (3716843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:465d9a54edc20c84229072e55369aeee962c87cc603e35839586bf0d1dc8ce70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f962f2e5970a5a54755bb2057dd1de86ffa69c5991dd72c8c71fd04968e64f`

```dockerfile
```

-	Layers:
	-	`sha256:1dc97ec20fcab2d9f67993cb2fc97f3efd163786ca6e131a53d4de6c5cea1898`  
		Last Modified: Sat, 01 Nov 2025 02:19:03 GMT  
		Size: 2.2 MB (2203468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b02cde9121f8d750a97a2cefea238e6f7298f731d6e745ef736e8a0f926a546`  
		Last Modified: Sat, 01 Nov 2025 02:19:04 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; riscv64

```console
$ docker pull hylang@sha256:1f9d8ebd9890e142762acf8ef81a62a052d44fef28dcdfd9a6d89613236ff1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47032779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30515dbc411fad2b0c4b94302c3e43a006b4f68bc85b34c21a46d291924b90d4`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Thu, 30 Oct 2025 04:33:31 GMT
ENV HY_VERSION=1.1.0
# Thu, 30 Oct 2025 04:33:31 GMT
ENV HYRULE_VERSION=1.0.0
# Thu, 30 Oct 2025 04:33:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 30 Oct 2025 04:33:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a3f1451d93ce350365e520b97eb9b8a07657581de0c11399fbe6f5092d90b`  
		Last Modified: Thu, 23 Oct 2025 11:04:25 GMT  
		Size: 1.3 MB (1260102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f06ce9695e4be7bf0426bdb4090b77f655bf8ffe9100002673d9c6d67a4e9b`  
		Last Modified: Thu, 23 Oct 2025 15:04:44 GMT  
		Size: 13.8 MB (13779208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72357e4ca1fd363a888a2bf92b245fac5651c93775f0e056b2a8bd5551c4bad1`  
		Last Modified: Thu, 23 Oct 2025 15:04:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b2e9a3e709f7efa4304db03328f92d3fb7b58a04818444aaf85560d801553`  
		Last Modified: Thu, 30 Oct 2025 04:34:42 GMT  
		Size: 3.7 MB (3717569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:d0eb3a809c9cebded949b2bbfb5156bf6c3f78e3d9dbaf146a7ee1743f0ef09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0e093a46e075615c8801e0720f6063a9bb715e5b574eea3fa89ecbe4eae0ee`

```dockerfile
```

-	Layers:
	-	`sha256:73604742ea2dfb2a1757e20f3a176f2f74448cf054e3b8856d97f6acd6c03a48`  
		Last Modified: Thu, 30 Oct 2025 05:20:15 GMT  
		Size: 2.2 MB (2193839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b406977f2b2ace729989df0f9b8e7c34a8f79d02a01b9db2a45ef246e71d43`  
		Last Modified: Thu, 30 Oct 2025 05:20:16 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; s390x

```console
$ docker pull hylang@sha256:07c63fe0dd272d085a67d8170ddb3f469c39f2a454c014d7ea7453314a82aaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48694872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17d88c457e2a21ce77186e054c9bcf17ca126c8e7116b37740d104e72a2cab4`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Tue, 21 Oct 2025 19:30:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Oct 2025 19:30:43 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 19:30:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 21 Oct 2025 19:30:43 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 21 Oct 2025 19:30:43 GMT
ENV PYTHON_VERSION=3.9.25
# Tue, 21 Oct 2025 19:30:43 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:21:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:21:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:21:49 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:55:06 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:55:06 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:55:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:55:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e414015a43e56e4b06133185cabf480df8d52b2f49fb047b4d68df5892c90435`  
		Last Modified: Tue, 21 Oct 2025 19:46:14 GMT  
		Size: 1.3 MB (1305251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0435056ca9e61c25c468371ac087c4332407526e9af1b21b805fb7d723ba8a4c`  
		Last Modified: Fri, 31 Oct 2025 23:22:09 GMT  
		Size: 13.8 MB (13835488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78521935a1237991092d52e8b0f19bd2bcbeece5e3547687509829a62679dad3`  
		Last Modified: Fri, 31 Oct 2025 23:22:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e949e0b16106afcb49bf93c8105f250799cd1dfe767f2e3e134c7c82018c8`  
		Last Modified: Fri, 31 Oct 2025 23:55:30 GMT  
		Size: 3.7 MB (3716628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:3255ef5110c6bbcec88b2174fd3242a99be3200ac278c35b77cc561db57dd158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d34c78c3754e709692618b4c9ad0c599ca3db41bc71b6b2413fec0f8d7df7bf`

```dockerfile
```

-	Layers:
	-	`sha256:b7724ceee90844467a92403b1d6c151e8aaee6f005f703690c35bb22852ea1c8`  
		Last Modified: Sat, 01 Nov 2025 02:19:12 GMT  
		Size: 2.2 MB (2201316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49be7a6e529c3ef31324dcf30d6e4fbb08e100efde414f0acfda44ce4c14a947`  
		Last Modified: Sat, 01 Nov 2025 02:19:13 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.in-toto+json
