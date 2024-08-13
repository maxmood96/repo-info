## `hylang:python3.12`

```console
$ docker pull hylang@sha256:10062053fbdb8b3682e7893f246ad8e85f59125ef8925a3d1561050a04c9c105
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

### `hylang:python3.12` - linux; amd64

```console
$ docker pull hylang@sha256:efc6feb2779ded4473175675d7b5cb9094fab8294170bcfe968ad7e6b94feaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53339784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3303423ecbe5a292740a54aab77b015b858c7809ff22119afcad0c0b92cebe2`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3436ea9cd94528baf127b0fbf2da7be83a2d4ca52896281201483e7a1726b1a1`  
		Last Modified: Tue, 13 Aug 2024 01:33:34 GMT  
		Size: 3.5 MB (3509899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699e948b876a73dfab247efda41e01ed99235158d14d6a359f7cd4d45d11fe09`  
		Last Modified: Tue, 13 Aug 2024 01:33:35 GMT  
		Size: 11.7 MB (11725699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5fc93dff1232040d5e73bcd35fe92a68b5b35674ffd57eb91bc678a29b1b34`  
		Last Modified: Tue, 13 Aug 2024 01:33:34 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6b38c76ff31be6c1586a1f50ffbbcf5bcaf948828817c066f3d7c1f6525d67`  
		Last Modified: Tue, 13 Aug 2024 01:33:34 GMT  
		Size: 4.0 MB (3981617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613ee0986669f2e9e1c801e653adb13d984c5a597064459a59a9698126b77dea`  
		Last Modified: Tue, 13 Aug 2024 02:16:54 GMT  
		Size: 5.0 MB (4996105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:33ee1ff591fc912d52c63cb49406c36016bbe44bc56fd51f1228c654fbbb411a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8900b899e71ecf4ea43d25c6aafe95f86f5291eef279711969dfabeb99f9e2be`

```dockerfile
```

-	Layers:
	-	`sha256:77cedead09de7fcbbb50d8ef1b6d41dc6d2d985b5dca1cf5f67ca7d5fdd8b8ca`  
		Last Modified: Tue, 13 Aug 2024 02:16:54 GMT  
		Size: 2.5 MB (2500159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e90501dd8487bcd15a261fc958b569043c3662543082bbb84c0b912f8e91eef5`  
		Last Modified: Tue, 13 Aug 2024 02:16:54 GMT  
		Size: 12.1 KB (12131 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12` - linux; arm variant v5

```console
$ docker pull hylang@sha256:a445eba23a8ddd4de3812fbae307d6012d268065e38785a2b5b389af9fd719e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50149586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd5e970327192a4b2ccae60f1eaebf1eaaf8109300ac992e511423cbaa3586d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652c16af5bfa1219d86389da98bf2114b0fa0c2c34f86882d98783c006e6ce4a`  
		Last Modified: Tue, 23 Jul 2024 14:19:00 GMT  
		Size: 3.1 MB (3080511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536c2a2ca7ae9477a9b2afca5507467a03d2fbe78d9f38adbb8df33f60399c0`  
		Last Modified: Wed, 07 Aug 2024 19:58:15 GMT  
		Size: 11.2 MB (11204045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74192cf3ad69e5a2bb801393faeb4abf51197748f6338c3432e652828e7ce637`  
		Last Modified: Wed, 07 Aug 2024 19:58:15 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875d0ccbc07c8c510f328ea06628ba5d513e0033f5139a49d2d02f5f92e12012`  
		Last Modified: Wed, 07 Aug 2024 19:58:16 GMT  
		Size: 4.0 MB (3981425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf53117df4b5487aea32ce625de552a89dbbb282afcbd656fd78c106b760685`  
		Last Modified: Wed, 07 Aug 2024 20:51:52 GMT  
		Size: 5.0 MB (4996073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:8f72b9da7fe257a41a740c08789b641405badf0e402d54dffff4fb458f6537a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2515977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d8f161b3e0fb83d1b5faddff28eb76f7727369acfbc062217f97b65759ade4`

```dockerfile
```

-	Layers:
	-	`sha256:3daf1f40fe199f3abfc427b7cba2b00e2da11fa21f740e59e828db9dadbdd461`  
		Last Modified: Wed, 07 Aug 2024 20:51:52 GMT  
		Size: 2.5 MB (2503662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52af1542247ba09e48117b70db710ed86d2b70b8bee53122d8912a72a5556b56`  
		Last Modified: Wed, 07 Aug 2024 20:51:52 GMT  
		Size: 12.3 KB (12315 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12` - linux; arm variant v7

```console
$ docker pull hylang@sha256:83794fead1de99c448fdc760a54f9ae281585d408e087cad91f32c23a288e050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47397260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda2d84cdc1e0547832ecfcf3f1ab947244c7c242406037a796c81926980aff4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9e89a9a0ff00898681ed65fdf1b4314005b314abcdccf71af481df01c0b68`  
		Last Modified: Wed, 24 Jul 2024 08:52:42 GMT  
		Size: 2.9 MB (2912163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b239eedd77815595c68fdf4b1c1d2f91236916c4e6be9d684115bfd7053f622`  
		Last Modified: Wed, 07 Aug 2024 21:11:41 GMT  
		Size: 10.8 MB (10789507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b775408cec72c6fa891dd943635c7d4d184a162ab5ea409fab172ab48ebae4`  
		Last Modified: Wed, 07 Aug 2024 21:11:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc80f2ad81d308a8fd202c9c98b1c3606568d5c45a748ca832676be8fc5535e`  
		Last Modified: Wed, 07 Aug 2024 21:11:41 GMT  
		Size: 4.0 MB (3981062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891b25fe076c8a6092b9665926fd7f4a9835f5ca1b69a81e01e253c8ee5391d4`  
		Last Modified: Wed, 07 Aug 2024 22:28:46 GMT  
		Size: 5.0 MB (4996095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:e79d44e266a1398d74b69a1087714c4078ea2002db90d3d0e4cf86bb044f85a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2514844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08143cf2954331caddaa0aa3d730c38d61ac8c9c4fbeb571e81c62373190e49`

```dockerfile
```

-	Layers:
	-	`sha256:30768930539e7f52a83455d2581cfac8ffc5c4c1ae1fa647a7db6867207ed866`  
		Last Modified: Wed, 07 Aug 2024 22:28:45 GMT  
		Size: 2.5 MB (2502529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f117f64a731f4b5441e31684d4a6f05659e86a438ed4e11ddbbbaeace4cfb8de`  
		Last Modified: Wed, 07 Aug 2024 22:28:45 GMT  
		Size: 12.3 KB (12315 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b8e04336548c3141a3cbaafd3fab7a936a4ca62ef52e63ee285c5e2e496ab8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53162360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06876adb6711916c6d1da2dc61a02d6a0e9de623f9454fdca271a072bac50e7f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba32bf0f91fccf36472f9ad3da47b1bd3638fa0c80d026ea6a6a5571ce334a12`  
		Last Modified: Thu, 01 Aug 2024 21:16:03 GMT  
		Size: 3.3 MB (3329912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc5ee30d1f70e4ab51fbc78428594b7e45296e85eafe28a587f6f0ae1e82fca`  
		Last Modified: Wed, 07 Aug 2024 21:03:34 GMT  
		Size: 11.7 MB (11697708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4007f5a88cb8e72682b48b778d4aea4b402ba728aa85a7dc7c26bbef6695d`  
		Last Modified: Wed, 07 Aug 2024 21:03:33 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8d7ef7003af1045b584a5ca5e274078147b9767b7adcc46bbb82f0735177ef`  
		Last Modified: Wed, 07 Aug 2024 21:03:34 GMT  
		Size: 4.0 MB (3981813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c380caf3aad6d82109528f3db08ee112c5c28ede7a16f705281d740b6888012c`  
		Last Modified: Wed, 07 Aug 2024 22:02:50 GMT  
		Size: 5.0 MB (4996122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:507822e90174a1e6f755d601b7246e54ca5d899e7ef668498fe28955bc19b6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2d18fd561c47fa92575f28ecf0cc8b7848c9bda8175b9ea14b553300010731`

```dockerfile
```

-	Layers:
	-	`sha256:31d6200d4766568efa114b3facaa33cdceffb0d59002d23df3bd049b087aed35`  
		Last Modified: Wed, 07 Aug 2024 22:02:50 GMT  
		Size: 2.5 MB (2500577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2acac07c1080176851c78ee5acbd4ab94a4d2f7d4265ae7c9febdc241d06677f`  
		Last Modified: Wed, 07 Aug 2024 22:02:50 GMT  
		Size: 12.7 KB (12671 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12` - linux; 386

```console
$ docker pull hylang@sha256:e6b32b8f6757b516a93ae791868720b8af26ca79324648d2caf2fa75eb90a11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54602671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b2fe06b5533714727bb8ce466676ed357224a75f34fc372b0d9ac1e0c9e4d3`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a4753faa129ca00840745b3a9b8c5bf92a8946427c54b1b91a1bf5c3c50864`  
		Last Modified: Tue, 13 Aug 2024 01:25:20 GMT  
		Size: 3.5 MB (3507298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5be89c89972a85424fbd1312dbedfcf049c6a5987092f39f3fc0e39e462a3c`  
		Last Modified: Tue, 13 Aug 2024 01:25:21 GMT  
		Size: 12.0 MB (11973543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa26952404a49f2c94c8c6bcfdc68b2f0cdc0419ad11d364f4f5b5ca0ec95f63`  
		Last Modified: Tue, 13 Aug 2024 01:25:20 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e87a7607b0e1bfedfa8e43ad64fa6d0c2cc26d40d9ec5fee5da6e0dfcb70cfd`  
		Last Modified: Tue, 13 Aug 2024 01:25:21 GMT  
		Size: 4.0 MB (3981224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c4ab8d245b210718439fd89286f27f84909664e3ced01ebe5a0ec5624a2090`  
		Last Modified: Tue, 13 Aug 2024 02:17:44 GMT  
		Size: 5.0 MB (4996093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:d13bad64ec01b55e394b6d2a18391f66dd2ec8273b5fff9e8432fbae8baefeab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2509232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e567bf763ee78fdbc23ec7b3785c748f19e55216a459fd49abab2b15995cb648`

```dockerfile
```

-	Layers:
	-	`sha256:10f73d4f5da430b8e5db2ec7a9bca973eaacfded3d1277bda832b65ba08bd592`  
		Last Modified: Tue, 13 Aug 2024 02:17:44 GMT  
		Size: 2.5 MB (2497193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca676cc936883a8e5c9a96dac771ea514a7413d2c44b152e6b965fb9a8521b2b`  
		Last Modified: Tue, 13 Aug 2024 02:17:44 GMT  
		Size: 12.0 KB (12039 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12` - linux; ppc64le

```console
$ docker pull hylang@sha256:f2e1957652fc0a7b163d992706fa3f834518c7f624e9e81b24886c6a1a63057d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58146757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19cb1c00a7e4cd63a849e1e818713d8dce5a884b97051fb7737484e45c405270`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00727597bf5fb6407a0ed311ead2327da6f7ba9c8bfbef711680ea567fa867a`  
		Last Modified: Wed, 24 Jul 2024 05:26:08 GMT  
		Size: 3.7 MB (3708173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b851818e105fcf8d932b144e3fdab542b3c6f70bf6b5fb787a1d2ed7a431115b`  
		Last Modified: Wed, 07 Aug 2024 21:47:28 GMT  
		Size: 12.3 MB (12337880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db43efa6ebb0e27cdbb6013789881356cb11302ca57c97dba241387051f788e6`  
		Last Modified: Wed, 07 Aug 2024 21:47:28 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad950d2266f07f16f7f8f128d4b0660a021f72f7737d420ac44eb2b305144ba4`  
		Last Modified: Wed, 07 Aug 2024 21:47:29 GMT  
		Size: 4.0 MB (3982119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f663786fb3299714c9d449ae57f011207063ae044ba660b18db7567b1d60c5`  
		Last Modified: Wed, 07 Aug 2024 23:20:46 GMT  
		Size: 5.0 MB (4996077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:4fb5b37f725168fd1a3225e4817339af3a03901df07f32b17a50d938cd64d5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2516892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2782a4fc9dd13010146f0b365305cf7bb8933ec544317b9ff5665cdbc6be5e95`

```dockerfile
```

-	Layers:
	-	`sha256:1defdd0119c1d66ab92d27c0b71f29f31ad767b86f4f46eb9d8764895b696e4c`  
		Last Modified: Wed, 07 Aug 2024 23:20:45 GMT  
		Size: 2.5 MB (2504634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95b7a742f8bbaa50d27ef2778d6f224acbc929d43d8a4aadb9a052a2ff783d10`  
		Last Modified: Wed, 07 Aug 2024 23:20:45 GMT  
		Size: 12.3 KB (12258 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12` - linux; s390x

```console
$ docker pull hylang@sha256:ed3d869a31e4282052ce5fa809024de702aaf95a39d508853c3337a01fffe59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51292832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7745edddc00e97d34358b9865dcf64808508a6d4d31023a3ed6df5b12767e297`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:d8b037f30c0a2aeded43f72fe61531da3a0e449e034255bb0a7b2182e4e3ca8a in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:48319744c6dacda7d13413becf85a83639982e97ecf615295a1257ccc3082721`  
		Last Modified: Tue, 23 Jul 2024 02:32:44 GMT  
		Size: 27.5 MB (27490099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b51cfee76bcf61f72507ba36f6a5fe1af8c1828b22e9ca6a55b6d993f364cc`  
		Last Modified: Sun, 04 Aug 2024 13:12:39 GMT  
		Size: 3.2 MB (3170502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef175f8c0486bf0ccf5d300d43280be8bd6655d9439b0947e97718f91c03100`  
		Last Modified: Wed, 07 Aug 2024 21:22:02 GMT  
		Size: 11.7 MB (11654615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad69ef916fff0996c25218241b26e03b3ab26639417d0d219acbef1050380a31`  
		Last Modified: Wed, 07 Aug 2024 21:22:01 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc77c806964e7d791e8b36c3f0eb826677af6e163c122bd92ef8acb5782cf86`  
		Last Modified: Wed, 07 Aug 2024 21:22:01 GMT  
		Size: 4.0 MB (3981352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c85b3f7f9e0e6da54371678241a48c489f883e85cfc2b792bb5cb176d1e561`  
		Last Modified: Wed, 07 Aug 2024 22:42:54 GMT  
		Size: 5.0 MB (4996032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12` - unknown; unknown

```console
$ docker pull hylang@sha256:622ac9cb25e705d5bf0ddc742f59cb4e43ba74e7c87fe0f113dea90c0ddb3e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b5977180fb4a4d6f735644e90129754dbac5b061094258d85719ec728fb27d`

```dockerfile
```

-	Layers:
	-	`sha256:9e048c9e9db91cc8bca9673723ee8b7c7627f93277837b078168df5a23b62a70`  
		Last Modified: Wed, 07 Aug 2024 22:42:54 GMT  
		Size: 2.5 MB (2499972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c171ad01d95063c99a4bfeff1f8b2052866ed124be6d572b440ccec5f9f7f3af`  
		Last Modified: Wed, 07 Aug 2024 22:42:54 GMT  
		Size: 12.1 KB (12143 bytes)  
		MIME: application/vnd.in-toto+json
