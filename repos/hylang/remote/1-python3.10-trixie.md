## `hylang:1-python3.10-trixie`

```console
$ docker pull hylang@sha256:923e24f08e32d7c7b94d25d0ce5c08acfa1bc72bea4c8834900ca3b9aadcd76f
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

### `hylang:1-python3.10-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:4d5327b459d0c7d97bc8293d0c4966c8746999dee3961bbefacd922df1202b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48745349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362a3b6851c39d7bcddb6b5512d62dbccf06367b7147a341b3a90a1458a09e69`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:23:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:23:16 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:23:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:23:16 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 04:23:16 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 04 Nov 2025 04:23:16 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 04 Nov 2025 04:29:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 04:29:12 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 04:29:12 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 07:55:38 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 07:55:38 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 07:55:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 07:55:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b7f5f69b041b1abff4207e69de41cedf65789880545196c035eaf5811d5659`  
		Last Modified: Tue, 04 Nov 2025 04:29:26 GMT  
		Size: 1.3 MB (1292959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfba6d6670ccbd07cb56beb604a62b8845b258b6681c2e48550494be8cdd04f5`  
		Last Modified: Tue, 04 Nov 2025 04:29:27 GMT  
		Size: 13.8 MB (13820541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09dc670095e3274f5c5b53f13f7809b550ebdbdb2d9fb9e32e1b18889d13fe5`  
		Last Modified: Tue, 04 Nov 2025 04:29:26 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379e4fe0eedbb868feca77cf8ffcd360150e1550d6852f91549746912e137f39`  
		Last Modified: Tue, 04 Nov 2025 07:55:51 GMT  
		Size: 3.9 MB (3853497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:df258f36c95e9f7287fafa415614af57f2ab18d7579560be98d4ea4fe5b120d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d03c92f28c5f2921f4d7540e9a6bbe81f0e860659f99549f0b6af2456c0d6b4`

```dockerfile
```

-	Layers:
	-	`sha256:c5c2de6cbdb227b05399d5f6f18267062ce26dbde24978554eae24c19c4ef01f`  
		Last Modified: Tue, 04 Nov 2025 09:18:11 GMT  
		Size: 2.2 MB (2199955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7fa7fb5aa1b84ea226c8a0b533f61d889d70e7dfc1c4822cff8c09bf55978c`  
		Last Modified: Tue, 04 Nov 2025 09:18:12 GMT  
		Size: 9.3 KB (9319 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; arm variant v5

```console
$ docker pull hylang@sha256:9fae1a447f1f2297f33eefbe20f018b524778c6335ef3e20324faa570fbc3857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46554554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85b34755f1d9cafed8e2430989c8b76719758afdd1ed9e352fff2d1497d6dc7`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:06:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:06:11 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:06:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:06:11 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 18 Nov 2025 04:06:11 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 18 Nov 2025 04:06:11 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 18 Nov 2025 04:17:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 04:17:35 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 04:17:35 GMT
CMD ["python3"]
# Tue, 18 Nov 2025 05:33:25 GMT
ENV HY_VERSION=1.1.0
# Tue, 18 Nov 2025 05:33:25 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 18 Nov 2025 05:33:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 18 Nov 2025 05:33:25 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674a2e16f191aa62c46fb7d536f53d2458129bd51fb47bee767049e1a5fc4090`  
		Last Modified: Tue, 18 Nov 2025 04:17:48 GMT  
		Size: 1.3 MB (1275883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b04dc225f08429f7d40b62c025dcfcd703c4b69be2b3a6fbd70e08d57ed963`  
		Last Modified: Tue, 18 Nov 2025 04:17:48 GMT  
		Size: 13.5 MB (13480432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481df48b2562dbb2a57a9ec639901666fb433c1e9eed562cc09c1276b3d77c68`  
		Last Modified: Tue, 18 Nov 2025 04:17:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b93ead97cd4f6657be415cd02337384abdef0edabb74ab9263de56bd4a2d046`  
		Last Modified: Tue, 18 Nov 2025 05:33:39 GMT  
		Size: 3.9 MB (3853842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:c92e8b52fedeb0adb654def8ac994b1454cf6ad07b2736a380ef3b0abf4a0cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f2824a9eead40648dd6425ff1079022815b1c5c8912b028fc55c24e562412c`

```dockerfile
```

-	Layers:
	-	`sha256:0e936d4cdd3aa0a815a3efe8b4424c5381026e3658af792d6cc7e158c174aaa2`  
		Last Modified: Tue, 18 Nov 2025 06:19:16 GMT  
		Size: 2.2 MB (2202950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a490887c5e82f9025948fcc56e20afa663b654d19e0c29e78bdc06a44458743`  
		Last Modified: Tue, 18 Nov 2025 06:19:17 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; arm variant v7

```console
$ docker pull hylang@sha256:33b9f04b1f9b15154b38d70c9209b2fd8f0805f0d9f84cfad2589c25607b337d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44530529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098335aa686a27d748e9c58caafd3e112bf2f8367f762f0879fac24f6e8bf8af`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:33:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:33:29 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 02:33:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:33:29 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 02:33:29 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 04 Nov 2025 02:33:29 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 04 Nov 2025 02:44:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 02:44:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 02:44:21 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 03:42:06 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 03:42:06 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 03:42:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 03:42:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fdafbb6fd9ccb5e22e626d83b3074310a07ae20e8bf322f08b2d5ed234ea2`  
		Last Modified: Tue, 04 Nov 2025 02:44:34 GMT  
		Size: 1.2 MB (1248440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d5d7bbf48b908e2511d2b00a581b492ff63966e57507bc8364cf67a6a6b32e`  
		Last Modified: Tue, 04 Nov 2025 02:44:37 GMT  
		Size: 13.2 MB (13215315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50445c64f570a830315d24d7a16aa94b3829a5e9f591f4ae8c65aa9fd6a35b85`  
		Last Modified: Tue, 04 Nov 2025 02:44:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e3ad2b1e02ef6d7a20e41a686b3d00066046f0aa54a17e635a0ea19785d565`  
		Last Modified: Tue, 04 Nov 2025 03:42:19 GMT  
		Size: 3.9 MB (3853487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:1fae07e3832f08fac04590f26d2785b36d1ecd78c2a8bde9765a8281b42b12ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e85d918b5249ff28ce73353c89209962dd1b1e632736b6288e1b691fbbba02`

```dockerfile
```

-	Layers:
	-	`sha256:e7ac509573c5cc37dd001dca20f99a93db7c491d2fc0c78ebe18948a546f7666`  
		Last Modified: Tue, 04 Nov 2025 12:18:11 GMT  
		Size: 2.2 MB (2201409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a988428f6ee9d757c3546dd3b46f18c5e85662a3ad034d13cb5036e530cede3`  
		Last Modified: Tue, 04 Nov 2025 12:18:12 GMT  
		Size: 9.4 KB (9431 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b0c7409c4d25647fa21f8aa361fd766ca6180519f38225b6cf4307ca620326e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49045346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf78494ffdcec44104500b0db968b91b0bce399d2e00cccb4a57da2ff52f06f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:39:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:39:11 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:39:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:39:11 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 01:39:11 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 04 Nov 2025 01:39:11 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 04 Nov 2025 01:46:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 01:46:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 01:46:53 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 02:35:27 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 02:35:27 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 02:35:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 02:35:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0e64e707cff4aa8e5a06c7e15f2c4055c1379890d173ac3b646578d402675c`  
		Last Modified: Tue, 04 Nov 2025 01:47:06 GMT  
		Size: 1.3 MB (1273601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5451a8c78bf7efc1b69f1709d740070c48d78751c38aa4e6d0e1499ac234562a`  
		Last Modified: Tue, 04 Nov 2025 01:47:07 GMT  
		Size: 13.8 MB (13775627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d675b6cf90017651ef0bc36c4835cec1ea1b5f70d9b3ed7360633ddd24f784`  
		Last Modified: Tue, 04 Nov 2025 01:47:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30658924f60e4ca491679df16188bd90f67d4f56ac2b07c14abc919b3cc4bc1b`  
		Last Modified: Tue, 04 Nov 2025 02:35:39 GMT  
		Size: 3.9 MB (3853573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:416e2a3a1c6bddbcdda62ec31506f3bd253b34a680802fc06449de1b9d8052f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd73c886a5be79af5393e049123afd2cf4fcd836c4a6add548de14621045000b`

```dockerfile
```

-	Layers:
	-	`sha256:fd55b57219bffcbef97901da699474712eb1790f8a461d7f169ce19d87219bfb`  
		Last Modified: Tue, 04 Nov 2025 12:18:15 GMT  
		Size: 2.2 MB (2200269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:272221a0de8f692e3091944ecdcfcc43ec6f9bfc6b55e95198aa7a4e0fd7b726`  
		Last Modified: Tue, 04 Nov 2025 12:18:16 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; 386

```console
$ docker pull hylang@sha256:8ce4cb721ccca913745f0e90c6ddf9084032d9f82c798ea7e97fe5c3658d5158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50296460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb0f9627958af8e93e07a550e33436581182d4615b85e0b507e98d7ecac4690`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:44:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:44:01 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:44:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:44:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 01:44:01 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 04 Nov 2025 01:44:01 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 04 Nov 2025 01:50:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 01:50:58 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 01:50:58 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 02:30:40 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 02:30:40 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 02:30:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 02:30:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93be10a18dda632411bcc889924f4df7d8616dc36349376746530944871fa4a`  
		Last Modified: Tue, 04 Nov 2025 01:51:12 GMT  
		Size: 1.3 MB (1297148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bd98a4531c696e8cedcdb9fc4009e42edd12256e3743443eca349d3089db68`  
		Last Modified: Tue, 04 Nov 2025 01:51:13 GMT  
		Size: 13.9 MB (13850746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139267af71f182efc94f10d9102ba369dc2015d00620fee6f159c85ea827fda5`  
		Last Modified: Tue, 04 Nov 2025 01:51:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3d8e5f005f6bd10535dec3d536d618ca8ac5b5511aa2a34b62c9b169d7923c`  
		Last Modified: Tue, 04 Nov 2025 02:30:52 GMT  
		Size: 3.9 MB (3853536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:dec9c34447e9f414175fa4862f575ab070aaeb1c383f8942f66c4c17d3c05527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149f298929588d0cba54de7c3d67b6313901904e662eda25f0d0496b44770bf5`

```dockerfile
```

-	Layers:
	-	`sha256:ea3ae54eb02e7a2967c0d68d7e3760106f247d9f921ab7370b07a8d4c50266d3`  
		Last Modified: Tue, 04 Nov 2025 09:21:19 GMT  
		Size: 2.2 MB (2197116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e617ab65e0385268c12f4a6f1fa92d3a4537b0486642e14d62ef29f42e691e`  
		Last Modified: Tue, 04 Nov 2025 09:21:20 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; ppc64le

```console
$ docker pull hylang@sha256:7c182710da8e5de0dbc6cbde9c89019038fc73ddf99f7cbd90b44af4ff57f622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52922020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86db0c73de80fa15666547bb955b5963398f2f819492ecf9416cbdf31f41c979`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 10:33:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 10:33:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 10:33:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 10:33:31 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 10:33:31 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 04 Nov 2025 10:33:31 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 04 Nov 2025 12:01:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 12:01:56 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 12:01:56 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 20:07:59 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 20:07:59 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 20:07:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 20:07:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38798fa0998cac5d52717f1c476b8942b4e6351f3b73edb03379b155af9b0c53`  
		Last Modified: Tue, 04 Nov 2025 10:51:46 GMT  
		Size: 1.3 MB (1321333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f42d4e20c422061d148d0225bf42edac1afd23a3e9428e5f4522b83064a29b`  
		Last Modified: Tue, 04 Nov 2025 12:02:39 GMT  
		Size: 14.1 MB (14147900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada21d04cab2688c96c84da109461060433b7f9b8ceded019333e99a46c4cb13`  
		Last Modified: Tue, 04 Nov 2025 12:02:39 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4a47a4a8ce300ab71ddd092fce4c6736cf3602068787e53c0c54925fbc1f75`  
		Last Modified: Tue, 04 Nov 2025 20:08:26 GMT  
		Size: 3.9 MB (3853890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:a948c8dc678c829be7c516e410120490e41e0c13166c09747878563618417020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c5415e20144b20141b9459d41290e133d7ab75356da8a20d3b19d77f22295f`

```dockerfile
```

-	Layers:
	-	`sha256:fca008432b54557295c94802444559506ea32b04b946e2244f7edbf32bbdd486`  
		Last Modified: Tue, 04 Nov 2025 21:18:09 GMT  
		Size: 2.2 MB (2203546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f97f4e54d4c2e505b1d985639a19aded47a6a6b250ebf60c0f8c7a1f37902612`  
		Last Modified: Tue, 04 Nov 2025 21:18:10 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; riscv64

```console
$ docker pull hylang@sha256:da15e9b4c63283833707d95b5f0fc4a49ecee841372ae23604225eab20d0f239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47120085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68f5c18fa97462ae7a198f25da90b0597199e74b5b527df9a076b1bb695ceb4`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Thu, 06 Nov 2025 22:15:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 22:15:20 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:15:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 06 Nov 2025 22:15:20 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 06 Nov 2025 22:15:20 GMT
ENV PYTHON_VERSION=3.10.19
# Thu, 06 Nov 2025 22:15:20 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Fri, 07 Nov 2025 01:25:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 07 Nov 2025 01:25:04 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 07 Nov 2025 01:25:04 GMT
CMD ["python3"]
# Sat, 08 Nov 2025 08:03:18 GMT
ENV HY_VERSION=1.1.0
# Sat, 08 Nov 2025 08:03:18 GMT
ENV HYRULE_VERSION=1.0.0
# Sat, 08 Nov 2025 08:03:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 08 Nov 2025 08:03:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4321fa2fab4685cf3a08032cd46bc0aeb0781651614ec91351b4aab4487fc6ef`  
		Last Modified: Thu, 06 Nov 2025 23:56:47 GMT  
		Size: 1.3 MB (1260095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e55755199e835690b97db9d63b4dca47b22cbcc714a46f29eee601524678df`  
		Last Modified: Fri, 07 Nov 2025 01:26:22 GMT  
		Size: 13.7 MB (13729489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac29fe52b8889b598216b4996ef2bbf805b091d7c6f10fb56bba9fd34b8e22`  
		Last Modified: Fri, 07 Nov 2025 01:26:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adba2cfd127e7fe90ddb8c0f29364b25da2d9031c8b9e51044adbfd5d3dbf5c5`  
		Last Modified: Sat, 08 Nov 2025 08:04:24 GMT  
		Size: 3.9 MB (3854466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:bc457524849bf3d06adabfc7e29c3c749873dbc8b6fad23303b5e4086d9bbf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb547ca7f5da8cf3813c53a9198320605acc21a91d0bf591e494d7d059a42f99`

```dockerfile
```

-	Layers:
	-	`sha256:a00ece00e6cc771e941fa7c635781ede91dd90a47c21a38aaa421784dcf639fb`  
		Last Modified: Sat, 08 Nov 2025 09:17:53 GMT  
		Size: 2.2 MB (2193917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e547289671c922a7e53c11a4b67317dad4cda1c6eccea6cedd9a1295a0292043`  
		Last Modified: Sat, 08 Nov 2025 09:17:54 GMT  
		Size: 9.4 KB (9387 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; s390x

```console
$ docker pull hylang@sha256:e2311ea4041b530e9dc93df04e9a0c322c4b728c3f81a61b4b08e09a7ce8b065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48751489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a3faf97b07eafcb6115690e84cc1d8eb5bcb4b330ceac73c2aa8a20d40515c`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:05:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:05:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:05:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:05:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 12:05:55 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 04 Nov 2025 12:05:55 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 04 Nov 2025 12:38:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 12:38:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 12:38:24 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 16:57:47 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 16:57:47 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 16:57:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 16:57:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625ac5bda657e609a86d5ae749bde4b1ce2e45b9d6e043c5149653e38c49f76`  
		Last Modified: Tue, 04 Nov 2025 12:18:36 GMT  
		Size: 1.3 MB (1305470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a446af97a48baa4014aa21f073c57f3451b82f695e890ac0675681b772308309`  
		Last Modified: Tue, 04 Nov 2025 12:38:57 GMT  
		Size: 13.8 MB (13754662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561657a4db01d95035cc8d60227f52a832b57bbe2bdb23989aafd4c9b323df9b`  
		Last Modified: Tue, 04 Nov 2025 12:38:56 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a00e274678d4cd44099c9d67395a92b9f08b10a11dd89bf02aaea9af99963f`  
		Last Modified: Tue, 04 Nov 2025 16:58:05 GMT  
		Size: 3.9 MB (3853717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:b3ca46eb6394563bae56e8ab4a834c426af19b5f79e85c9bb0b0441e2fedcbcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc4a48891e24fb9625bd40894f3f61043da5c052a8b443c7cf0330346842f0b`

```dockerfile
```

-	Layers:
	-	`sha256:bf39b8053c6fd26bbdbbf493f2237ca6da9186dedeb7c91dfd669ada757a60a6`  
		Last Modified: Tue, 04 Nov 2025 18:18:08 GMT  
		Size: 2.2 MB (2201394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7845b7023f553505382cb5a389121c4261c0378fd5f616a75cb1cefa37f925`  
		Last Modified: Tue, 04 Nov 2025 18:18:09 GMT  
		Size: 9.3 KB (9320 bytes)  
		MIME: application/vnd.in-toto+json
