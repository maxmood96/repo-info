## `hylang:1-python3.10-bookworm`

```console
$ docker pull hylang@sha256:77fc5f8bd031c0b935310abcf9f9b8d5ad31b294a49cf65da8e17b10f9ab1c65
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

### `hylang:1-python3.10-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:ad9aecd331710de24570197c08631f556e92553b2fcbd79cff7907fc9a940e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52284964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c442ab89746e8bd59d5caf78968ea781ca67958b982b42ba49ddbf3965ed06cb`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:47:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:47:49 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:47:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:47:49 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 19 May 2026 23:47:49 GMT
ENV PYTHON_VERSION=3.10.20
# Tue, 19 May 2026 23:47:49 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Tue, 19 May 2026 23:54:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:54:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:54:07 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:12:05 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:12:05 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:12:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:12:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5eacb2bb814dea504626f971132e96d20cdc3721bd2e1b63a41cd0c152c095`  
		Last Modified: Tue, 19 May 2026 23:54:16 GMT  
		Size: 3.5 MB (3519929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2b8aa2b7e86f4393dd07f42230666f2fcfd3e180ccae3ac14119d5d0c9acc`  
		Last Modified: Tue, 19 May 2026 23:54:16 GMT  
		Size: 15.4 MB (15377429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a160da2020445bafab042b7b1a33e174db04f20055c2dfc8b0e0887fa6be8`  
		Last Modified: Tue, 19 May 2026 23:54:16 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ed8ec630775f7730696f50d0031259a15356b9d3cca9d8b0f06399e60e439`  
		Last Modified: Wed, 27 May 2026 00:12:13 GMT  
		Size: 5.2 MB (5153813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:2b6f38a7ee5a9c76ff615f9dcc24359e6c47e03825f4bc97e712301a78e35ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b00dbe834226765c1c6581dac59c9e30fb95ca90844daa19cfdfc352f2d28c`

```dockerfile
```

-	Layers:
	-	`sha256:97f2b152dbedb287992c7cf6e16cefd041a4be8443b81c923739522d7ad24b79`  
		Last Modified: Wed, 27 May 2026 00:12:12 GMT  
		Size: 2.6 MB (2623052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f3fd358e9015fa9997c22274f792ec2785a43eff29a11a08619116e5d41ee4`  
		Last Modified: Wed, 27 May 2026 00:12:12 GMT  
		Size: 8.1 KB (8094 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:0b74a4bd466f7cdadbaa6f1753ecff6a6bee02756bc6c31b58ce49b3b56937ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48847219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6b1a760f93f1a3d7ae43d0c4003b6c2a1163424b2f0618ec64061159aead87`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:34:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:34:59 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:34:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 May 2026 00:34:59 GMT
ENV PYTHON_VERSION=3.10.20
# Wed, 20 May 2026 00:34:59 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Wed, 20 May 2026 00:46:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 20 May 2026 00:46:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 00:46:05 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:10 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:10 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3e5afa2eeb01167c187727ebcf5bb90554d4e6dd21fe61f1f694b128ceb15ac1`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 25.8 MB (25768291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707bad11ec37199ee53f63412620e016ac341b3a7ffb75bf4cfee6957bb0127`  
		Last Modified: Wed, 20 May 2026 00:46:14 GMT  
		Size: 3.1 MB (3093150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d49ecd1e278d3e2c9137c22c046cdef588a22e63f723ecdff9bb38211ea09af`  
		Last Modified: Wed, 20 May 2026 00:46:14 GMT  
		Size: 14.8 MB (14831665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ed33f50456606a74ef8572ecc385f822840d45f0458eb0f5285341a916f448`  
		Last Modified: Wed, 20 May 2026 00:46:13 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e043e53e233a851447cf01ae9ae5b02312de5c66e44012708919b77b79b4958`  
		Last Modified: Wed, 27 May 2026 00:11:18 GMT  
		Size: 5.2 MB (5153862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:a7fea3294cae9d3f87917c7beb6d5d425247c633b3dee628e4580011f9dc3b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf299c2749406bbd8031be0e256d699170474e9cfd1cbf03a974d9ff227e402`

```dockerfile
```

-	Layers:
	-	`sha256:d84eb1e358606e287563708193279552309b35c75ee21214b8d048c316d8b582`  
		Last Modified: Wed, 27 May 2026 00:11:18 GMT  
		Size: 2.6 MB (2626872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883649132894a940f599ae285dae650d6c82d56ae7630c2fc235bf8353f5fc24`  
		Last Modified: Wed, 27 May 2026 00:11:18 GMT  
		Size: 8.2 KB (8174 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:5bb87cba0c75b0edea2e44c5af7773886bd5347fd8b8291d1ec7ff270655610b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46438834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bff92a3fb658d5dd8edac1fb3473bd7666286deb9aee72c80e5c1cde84f81c`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:00:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:00:13 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:00:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:00:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 May 2026 01:00:13 GMT
ENV PYTHON_VERSION=3.10.20
# Wed, 20 May 2026 01:00:13 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Wed, 20 May 2026 01:10:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:10:58 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:10:58 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:12:04 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:12:04 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:12:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:12:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69453f811718caf87296925fa72c7ae29ab06e2d2d55d6c0876a464b59706d32`  
		Last Modified: Wed, 20 May 2026 01:11:06 GMT  
		Size: 2.9 MB (2928570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba2cd7fc16e94a82b55dbd5fd9532fa672a80b6e35802d71b627bf092801dd3`  
		Last Modified: Wed, 20 May 2026 01:11:06 GMT  
		Size: 14.4 MB (14414590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61be48308a9c85a09aa61c3487b07632948dacd562d075d698157ecf1bc8c5bc`  
		Last Modified: Wed, 20 May 2026 01:11:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333e976faff6ebb568d1e27df3380eefca57887aa5ee534d672f71cc097d65a5`  
		Last Modified: Wed, 27 May 2026 00:12:12 GMT  
		Size: 5.2 MB (5153782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:8cae30cb0e177cec689608b2dd4a0f5594104dcde704e7bcc4d2a4c8cf2fd712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b760c41ca8f235e8d02fad74afd6c9e44b3b6760c8fb7fae91b574ce25092457`

```dockerfile
```

-	Layers:
	-	`sha256:ada48a20604648bd6cf30d1897804b7fb681f73fccc6cead12ab07ca3ed4c851`  
		Last Modified: Wed, 27 May 2026 00:12:11 GMT  
		Size: 2.6 MB (2625321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7736ccd6afc9f0671c16e15e570da9c2f6659d7a0eb1d816b3f60e21d185106b`  
		Last Modified: Wed, 27 May 2026 00:12:11 GMT  
		Size: 8.2 KB (8174 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:a48a6569b897872f5653432a6e8da44f3b80785effc78bd8f24dc16ab3ae3e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51931570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015c1e6e64a17eb5b8534225159cf0e77f060903b15f452ca437bb91206be250`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:52:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:52:12 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:52:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 19 May 2026 23:52:12 GMT
ENV PYTHON_VERSION=3.10.20
# Tue, 19 May 2026 23:52:12 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Tue, 19 May 2026 23:59:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:59:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:59:47 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:12:02 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:12:02 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:12:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:12:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850cdd686c6534c1e6410260c9e99b5874ede04a9e995882bd5d58ab3f9b453a`  
		Last Modified: Tue, 19 May 2026 23:59:56 GMT  
		Size: 3.4 MB (3351801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbea6b852aab1b0a3e249c7b0f112eb21ed3409bf60acbf98de41ab58561716`  
		Last Modified: Tue, 19 May 2026 23:59:57 GMT  
		Size: 15.3 MB (15310693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7f270e4cf27bd271cde398411295b9b1752512c6a47fb55385da91fc14ab3`  
		Last Modified: Tue, 19 May 2026 23:59:56 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de0c42165c7ff55957b870cd87b1aeaf8aae3456e47f3aafa277729ccdf47c7`  
		Last Modified: Wed, 27 May 2026 00:12:09 GMT  
		Size: 5.2 MB (5153783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:4348af9467df722c7786fe81345349d85275b93c640eea525949b2ee331cad13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1be3d770dc0f24645ce884ae77c455601f8dbd0cbc67fc39bb082e0e61807ad`

```dockerfile
```

-	Layers:
	-	`sha256:bb3b8fc09de0ff669e294569654f069c51e0d5ce41e45f85868e6b76663cc9a6`  
		Last Modified: Wed, 27 May 2026 00:12:09 GMT  
		Size: 2.6 MB (2623325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cfb70951b90b08c554b5fb27f509e625dfa9c4ae3ab493c31d18b3e9636546c`  
		Last Modified: Wed, 27 May 2026 00:12:09 GMT  
		Size: 8.2 KB (8196 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:95547d2ad8b5fe92245f904fad8e7cdec01b157fd7e30cf19c1e90e102b81129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53514863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900800df165293d6ee5342d64836ab85857a372433e840bc750f3372085ae2db`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:48:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:48:31 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:48:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:48:31 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 19 May 2026 23:48:31 GMT
ENV PYTHON_VERSION=3.10.20
# Tue, 19 May 2026 23:48:31 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Tue, 19 May 2026 23:55:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:55:36 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:55:36 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:58 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:58 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c223f0114af4eac70bec94b0054ddde207caffeb53960af4c0204f2d731ff6`  
		Last Modified: Tue, 19 May 2026 23:55:43 GMT  
		Size: 3.5 MB (3520874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225e12692954276aa86f02d1173d9fe5e6d5d01ca1e4b24485f8daa0d36af7d8`  
		Last Modified: Tue, 19 May 2026 23:55:44 GMT  
		Size: 15.6 MB (15621370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f9fcd2ff28a1c20f5a64f3ba8dd8f596bccc65ee16855a8078b1db881ab2b1`  
		Last Modified: Tue, 19 May 2026 23:55:43 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b9c3fbe7c5ab773a62a2c29006c623710282a396a9590f55fa06e05c1b662b`  
		Last Modified: Wed, 27 May 2026 00:11:05 GMT  
		Size: 5.2 MB (5153769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:862737b9b24ef721ca97d3ac0ff4e9b645e32727997a91b54cb19cc8f9814d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d55792116cb915c91805f700c3fb6801ef4aca2de935effe8287bd9cfbc28e9`

```dockerfile
```

-	Layers:
	-	`sha256:b7c28da8c3b556b17431dd130acd77702be05af5bc7df8789fb119b06d49ec2c`  
		Last Modified: Wed, 27 May 2026 00:11:05 GMT  
		Size: 2.6 MB (2620203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01e0a80eff69c8b843f963cfccd4b34e639068021c50cb3bd6f08e6cbc6b6e7e`  
		Last Modified: Wed, 27 May 2026 00:11:05 GMT  
		Size: 8.1 KB (8062 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:41f0080094d4e3449767763f1b29e7a63a38823ed4eedbe665c74cd2a2709b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56951217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644420f1562759f88e1aed33877d4d8b9a986e41d94261e4d2a8e1e5eefd09a2`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 04:33:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 04:33:44 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 04:33:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 04:33:44 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 May 2026 04:33:44 GMT
ENV PYTHON_VERSION=3.10.20
# Wed, 20 May 2026 04:33:44 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Wed, 20 May 2026 05:26:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 20 May 2026 05:26:08 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 05:26:08 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:26:16 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:26:16 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:26:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:26:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9992109105b99d139cd44d383159fc226ead8096c0467c99111f3a441a0537e2`  
		Last Modified: Wed, 20 May 2026 04:53:37 GMT  
		Size: 3.7 MB (3725057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdeea5a58af93bbb30c92809a92ac819875e9015e48aa9f8a0fe92a336276e0`  
		Last Modified: Wed, 20 May 2026 05:26:24 GMT  
		Size: 16.0 MB (15995795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8be941f748792785f84166e8a976eb0dc2787418593f24dbe197b58ed1400d6`  
		Last Modified: Wed, 20 May 2026 05:26:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0197e5b00c6879ac04783e0e3fbf28d3ce56e557896b6b2524bee0da58fa7793`  
		Last Modified: Wed, 27 May 2026 00:26:32 GMT  
		Size: 5.2 MB (5154375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:ea2d22bea3a232e62f6ca1ffa987bab642a0156ee75a6e4c79504c1dae16e4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10100b667d84571a09fd8b07d47910caa5560990bbdb1babde04a9d6c809bfd`

```dockerfile
```

-	Layers:
	-	`sha256:433d4236e317e5bdfdcda8a7c41a20ad6db5ba60670f4b535e00c40db3a130a0`  
		Last Modified: Wed, 27 May 2026 00:26:31 GMT  
		Size: 2.6 MB (2627558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f682ff17dcb3efda049d06c4f686b329c21ed243cbd08b9d61ff3d7d7fd632d7`  
		Last Modified: Wed, 27 May 2026 00:26:31 GMT  
		Size: 8.1 KB (8138 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:7ba10f8edde2efac745a933d8005578acd092b6a0f22730a642367ed88b1755c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50397552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe14553ef4b5484e6580d6df3a186330b2c606598cf4b4cce5b12c66d5b4741`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:15:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:15:32 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:15:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:32 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 May 2026 01:15:32 GMT
ENV PYTHON_VERSION=3.10.20
# Wed, 20 May 2026 01:15:32 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Wed, 20 May 2026 01:38:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:38:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:38:06 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:19:24 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:19:24 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:19:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:19:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d95ecc58e29f001750d357eea736423e2548d14ad0d284c6c148dd3071050`  
		Last Modified: Wed, 20 May 2026 01:29:03 GMT  
		Size: 3.2 MB (3184031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39842e3390b4fe57293cca69372c473d0eb06f1c8b33de72720ba842bd1923c1`  
		Last Modified: Wed, 20 May 2026 01:38:20 GMT  
		Size: 15.2 MB (15170739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b90779841aa3d99f974daee894a6ac6429100f48b8e63be26de5b7f50182dd5`  
		Last Modified: Wed, 20 May 2026 01:38:19 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c9d7325df71ae9e0bd8a0c8251e69187563dd957a156373f31d3c2623c31c6`  
		Last Modified: Wed, 27 May 2026 00:19:36 GMT  
		Size: 5.2 MB (5153935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d955929944783565e1e64c3d7e75e58cbe7662b96e77172b8c5b821f867f7b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41956240ec365ccb721e5fcd4f99b235b1547cf44e0199bfaa97b093269eb38c`

```dockerfile
```

-	Layers:
	-	`sha256:eb9483570aa62582fc495bd5202fc889dc693bbe3addfd348a19768e4bf7b1fd`  
		Last Modified: Wed, 27 May 2026 00:19:36 GMT  
		Size: 2.6 MB (2619868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d09cdd07dbb4aac0984cf696e8aa7410a70398461cfa47899a7c3d92e57b4fd1`  
		Last Modified: Wed, 27 May 2026 00:19:36 GMT  
		Size: 8.1 KB (8094 bytes)  
		MIME: application/vnd.in-toto+json
