## `hylang:python3.10-bullseye`

```console
$ docker pull hylang@sha256:b56886d58bb90dd94125ee3661379043797146cb026525a4f76335c87d5a3a23
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

### `hylang:python3.10-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:874f32dcbb387fb7768c0dc62d08069f3343a55484394d69e9aedd69f2e09d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56999792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719a7272eb385026c467c263e431d405f71e34437576acc08c6d062544a4632d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 21:49:13 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_VERSION=3.10.18
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
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
	-	`sha256:023041bc400d838f7b27950e5e44ebea508a1b93fcacdd659dd0ecd7f7091692`  
		Last Modified: Wed, 04 Jun 2025 18:03:24 GMT  
		Size: 1.1 MB (1077888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b6e24646ef0de0f78ccf72b5cb693e2c26e729f5303561765ed4177f833aa9`  
		Last Modified: Wed, 04 Jun 2025 18:03:25 GMT  
		Size: 21.5 MB (21478422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8c448fc85b717400728a712a0d711117cb3e8491c620084d3f9058cd03098b`  
		Last Modified: Wed, 04 Jun 2025 18:03:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb60dc42278850cd710d65c3220c00c44ed006c79c7a6a1e662014438a6e440e`  
		Last Modified: Wed, 04 Jun 2025 21:22:52 GMT  
		Size: 4.2 MB (4187293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:214c28f163c2ff8661a389f5490ba2ed85a0266e1820c6f2c600fe6fe68f223b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864dfbc41643fc4f3ea0abf1fb6e0d39bd20407cc315f3f3ed8576820fa17fcf`

```dockerfile
```

-	Layers:
	-	`sha256:78780fdc63c1d5233f27d29f1da0b9e6d2eb9973cf698d83f8cd233e4cd07244`  
		Last Modified: Wed, 04 Jun 2025 23:26:41 GMT  
		Size: 2.7 MB (2739039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1672d643ff6e69b16d3bb4efc0863f1c7132f822b78ab265aa733f50ba470938`  
		Last Modified: Wed, 04 Jun 2025 23:26:42 GMT  
		Size: 8.0 KB (8028 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:394ba7f5e9e3efab0d9ad4721dc73ef6d0069da952335e1dcb9a5c2f9fead166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49966379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f586b10d2cce25857cee687615cdd6c8cc2baa8e636f3dc435b7764072aeda`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 21:49:13 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_VERSION=3.10.18
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
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
	-	`sha256:19d77e6172c26b4080a501eca67ca27311fbd0dabd85e4ad4d0387ce4631519c`  
		Last Modified: Tue, 03 Jun 2025 13:50:35 GMT  
		Size: 1.0 MB (1042868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e559ec1c5dad2a9832b2446ad181a8870d938fe83da319e767c4c7be191c65`  
		Last Modified: Wed, 04 Jun 2025 22:33:12 GMT  
		Size: 19.2 MB (19192217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044118dc95a8ffdd966c4f6121cb71ae17f6a07430c9f50a9e2a8fe6f2af32b9`  
		Last Modified: Wed, 04 Jun 2025 22:33:10 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0df559c00f966c5d34c5a920687ecfaa798cb27a5df5399c11ba99ef403de3c`  
		Last Modified: Wed, 04 Jun 2025 23:24:50 GMT  
		Size: 4.2 MB (4187143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:34b1aede4176f6b14c87e65b02e6e4a1ac07e7a5ee07eb4960cc26f0497f622c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e0638a98fb98dab0c95020412222878c0c267fa911b4976dd8a47a737b4210`

```dockerfile
```

-	Layers:
	-	`sha256:3987c362d5ddbc9a7767973987996a3b858d7226fde96da7bdc046d533a6c3d9`  
		Last Modified: Thu, 05 Jun 2025 02:18:18 GMT  
		Size: 2.7 MB (2742880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ce4f995690d6e051a183d7afcd927aeb13436cca7be48f9641d072f3abc980c`  
		Last Modified: Thu, 05 Jun 2025 02:18:18 GMT  
		Size: 8.1 KB (8104 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e4da61a68d3c13e018446b2623ce0250fc3ee21eaf20c3f406cdd5d89fc35cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54597011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8118326a5a99242cc46240c3d5dde8d08acf8795e452b6d37d535d2636f7437b`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 21:49:13 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_VERSION=3.10.18
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
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
	-	`sha256:9f68d4647786cc15bd979e88aef7c4edf03f28557e1b55612599156bdb92f7f9`  
		Last Modified: Wed, 04 Jun 2025 19:02:33 GMT  
		Size: 1.1 MB (1065725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05eb6bd745bd635c057b7504b53e049ae0b34aa44fd74484d99e65562dde1f6d`  
		Last Modified: Wed, 04 Jun 2025 20:48:05 GMT  
		Size: 20.6 MB (20597627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a5287be3ff59b5d3d4587aba5baaf37511274dd2247dd7cf257ed0f9dc1838`  
		Last Modified: Wed, 04 Jun 2025 20:50:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da844d14bff27a970f8e5d4deb3c3e6a89ad6af268c3c916d170042ca689c1ba`  
		Last Modified: Wed, 04 Jun 2025 22:01:09 GMT  
		Size: 4.2 MB (4187153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:6d03405788cc0818e30ca832d191922423c128cb4850a9b8cba10e737c8e18ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dd87ee8e8bede003aa3bf6d203476799351f1fd1147698ede5e00b816f72ee`

```dockerfile
```

-	Layers:
	-	`sha256:eb3fe882aa29babe078f7cdc30e11869f1b5107f6114d214559d38d8fb309679`  
		Last Modified: Wed, 04 Jun 2025 23:26:48 GMT  
		Size: 2.7 MB (2739298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bbe8e7e99b2749c61ca8c4e5f73d895d98294cd975e66ebe96f60f1a19f6304`  
		Last Modified: Wed, 04 Jun 2025 23:26:49 GMT  
		Size: 8.1 KB (8133 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:6177d2d1e2338bcc5f9507541349a052ba72fa487e3fdfe552c7fe9f333a6c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57634462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319b6fa38ef55fa72e58e282c56c40a4e600d1653d051faf06740fd502053079`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 21:49:13 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_VERSION=3.10.18
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
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
	-	`sha256:3c9567100ccfc880b8ceeff912bf33e903fd9f0594496de3bdda6fcc7af65636`  
		Last Modified: Wed, 04 Jun 2025 17:19:48 GMT  
		Size: 1.1 MB (1090551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2790cd2a053b54acaaf4ca116b2cbbc38d200ffe743c2ee5f7974d34bc3da388`  
		Last Modified: Wed, 04 Jun 2025 17:19:35 GMT  
		Size: 21.2 MB (21167276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cfb7731dedeb2b17c62f50c7caf7be3a421c9325f50f068e342f101707f5a8`  
		Last Modified: Wed, 04 Jun 2025 17:19:34 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ed8bcdd1e4ba526033b253af7dcafd700f347f4cbd34adee7e8c664ee0d5ca`  
		Last Modified: Thu, 05 Jun 2025 02:16:18 GMT  
		Size: 4.2 MB (4187184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:34e3e805b474c2ba59ab5b114934900f308d991b515c421345b6a454d3c9bdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2744199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3089ea8c14c678e4e009d577d071c493b7220d910628a71070437cee6dbc1bbe`

```dockerfile
```

-	Layers:
	-	`sha256:1010736d0bcf9c0fe97704a934633c8ff6fa5af4b306da22b9e01bbc179a6621`  
		Last Modified: Wed, 04 Jun 2025 23:26:53 GMT  
		Size: 2.7 MB (2736202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecae7772ed5ad90733b025030acf415705e7bd827961c6b02dcf29181cd13b45`  
		Last Modified: Wed, 04 Jun 2025 23:26:54 GMT  
		Size: 8.0 KB (7997 bytes)  
		MIME: application/vnd.in-toto+json
