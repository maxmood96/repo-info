## `hylang:0-python3.12-bullseye`

```console
$ docker pull hylang@sha256:872dece83b2cc81106d90354e4aed67b4aa3a4a29f5e21d32534cb65d0a59811
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

### `hylang:0-python3.12-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:b68bcb10c4c3902ee9b69d9c1a1a53c394a9b9afe5778ab997b76b22efc77511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52195873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d472798823498aeb790fa801b8eca9179f2e6cc9bc13ad8e2f7671a4393e7e`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["bash"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.12.4
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a19121168381ca3f160093c9e4f50db09fc1e885dd47610114d3a1edef8e96`  
		Last Modified: Wed, 03 Jul 2024 00:14:45 GMT  
		Size: 1.1 MB (1076291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddef92487c6484eab0a30299c96e321f9a9c71968c1de61404c8dbfc20ec1e50`  
		Last Modified: Wed, 03 Jul 2024 00:14:45 GMT  
		Size: 11.2 MB (11227812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b713bcb2cbf4f22b15027d5d930b2cc07de9f1258d7849b1ff803b6267b1339`  
		Last Modified: Wed, 03 Jul 2024 00:14:45 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca7c27cdde32a425476fa321e0bc46c4ba5c3067f171e5e3289f9c1e06e6f8e`  
		Last Modified: Wed, 03 Jul 2024 00:14:45 GMT  
		Size: 2.9 MB (2874078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c74cf3771cbe8a2222ca931c68eade1a952ea0b7f72c8846606404cd836dc5c`  
		Last Modified: Wed, 03 Jul 2024 01:00:43 GMT  
		Size: 5.6 MB (5595175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.12-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:0d2c1eae7b9a4f04858b02689c8c2306c07a3e6e16cf0552c9df99716f2339af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd3a6bc8cef548710f111dd4e051892fe1007841aba63f082c7bd715a9da4fc`

```dockerfile
```

-	Layers:
	-	`sha256:5ce7e6dc18d0b7237f6f8ab480dffd1202fef9974afad2d9d8fa68432f2ddbf7`  
		Last Modified: Wed, 03 Jul 2024 01:00:43 GMT  
		Size: 2.7 MB (2687335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cce3c07edea8efa012cb5ab5a037fc0011f7e790688aacd715160e18bee31f9`  
		Last Modified: Wed, 03 Jul 2024 01:00:42 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.12-bullseye` - linux; arm variant v5

```console
$ docker pull hylang@sha256:edc1e111346064bc3046fcb94d4d4196e014e9bc5b3402beaf03471afae96041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49371208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2875ca1349cd4855c09f77be0208095319ea571c2b278e273b675631ba1e2ba`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:7b150e5fe9a4f014196e0bfb8275f3406ad543dff58b049264b54e2e00f392b5 in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["bash"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.12.4
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:63678471745dce46512f823fc94716da7f08aa84c931dde61ae18c67b55c3085`  
		Last Modified: Tue, 02 Jul 2024 00:52:13 GMT  
		Size: 28.9 MB (28924714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56aa6fda52fd675c3296bcf24471cef5884c7268e1eed9e5d5a1f42f290c8dbf`  
		Last Modified: Tue, 02 Jul 2024 20:55:42 GMT  
		Size: 1.1 MB (1059710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282281315c79dcbf78b4b42ad91e2c46ebea9c02a1053b804d63390820e20340`  
		Last Modified: Tue, 02 Jul 2024 20:55:43 GMT  
		Size: 10.9 MB (10917734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c95a3d194898436fa45d098613a7487025e1c5a5e080bf45dec3656ef43f06`  
		Last Modified: Tue, 02 Jul 2024 20:55:42 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2075149d74c72a09a8f2039afeec82c0ef2a7ec9a88a81274a3beff417f20d9e`  
		Last Modified: Wed, 03 Jul 2024 02:31:34 GMT  
		Size: 2.9 MB (2873852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76a4f9312a3485e2d863ee333f51c30ee09f3e012f962b2e8f63b7edaf7f9cc`  
		Last Modified: Wed, 03 Jul 2024 04:01:42 GMT  
		Size: 5.6 MB (5594966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.12-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:983494de5abc7b22ffb2ead4853fa48223a2d11d00cbe98d1d5b906ab6d109cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fcd507c0bc8ad11c7dabef1449f85ea05cabf90a9d0be1429332e50c53f4e7`

```dockerfile
```

-	Layers:
	-	`sha256:ba9a01c3a85783f1d219a516b3210433717394035e3aaedbe36fbe30a342bb9e`  
		Last Modified: Wed, 03 Jul 2024 04:01:42 GMT  
		Size: 2.7 MB (2687609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb4cee3907e4028a099875c5cc60c8f7b600c4f6addf414a63beb5a34272941a`  
		Last Modified: Wed, 03 Jul 2024 04:01:42 GMT  
		Size: 9.8 KB (9821 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.12-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:2d4e9af02b4541a5a78d07f8a30bf8939ecb3d5976cba0027767a77815c52517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46573009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3945b6e64308dfd7c932200a06df44daa5060fdbdb53ae88593b8b9e5442b650`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["bash"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.12.4
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d1b8374477deda088db2b2784d203ec3d046360becceaedc483315dda4ef49`  
		Last Modified: Tue, 02 Jul 2024 22:21:03 GMT  
		Size: 1.0 MB (1041728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c8191d4d6f73a35e14bb2cb519459d4b9a599ae028eb56aea8557c8dfa189f`  
		Last Modified: Tue, 02 Jul 2024 22:21:03 GMT  
		Size: 10.5 MB (10479217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e974718122d43ee35ee10acbc383f8ec43fa37ec0527ba13c671e2c0912723d`  
		Last Modified: Tue, 02 Jul 2024 22:21:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c932a02060e7c76710a4638b3d63efa371f285acf4d78bad866d5afab63e4d38`  
		Last Modified: Wed, 03 Jul 2024 06:48:39 GMT  
		Size: 2.9 MB (2873857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f6b74053e79c100e697a34ab63e394e01167414f6c38aab860b07bbe4b2945`  
		Last Modified: Wed, 03 Jul 2024 11:20:28 GMT  
		Size: 5.6 MB (5595268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.12-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:ddfe258c3530cf768d28182b687ab8b33722d52dc4004c2c9f4c88986c88f3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df9840e5d7fa38dadff02a1b19b37e2cd425a7a69ab334cbc4f5d0777c6fd78`

```dockerfile
```

-	Layers:
	-	`sha256:cd8506ddc98e817426c69a6be73232b360e93243a3104a732a6a56073bcd3c0f`  
		Last Modified: Wed, 03 Jul 2024 11:20:28 GMT  
		Size: 2.7 MB (2689617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb80771d51abb89141d0bdd9536deabfa29c63301da7aaa843d1eeeba0c3add`  
		Last Modified: Wed, 03 Jul 2024 11:20:27 GMT  
		Size: 9.8 KB (9821 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.12-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:1eefa89b0e8c9e99b1a363252cc66aeefdd9d505d41181ef130a1b0e5d283b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50897875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee2431f2e4466e4a780ce71cadadaa7a6e537bf81ea814ab5ce5c3d902ee9bb`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["bash"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.12.4
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2197229b63cd075b53e5db849039a3900a119a8b056fbc92b7c606dbf3ecc530`  
		Last Modified: Tue, 02 Jul 2024 21:20:28 GMT  
		Size: 1.1 MB (1064130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95308c8804cad9fdf83d34811f850e032b4b36b2df9b53869b4f5a864e2219ab`  
		Last Modified: Tue, 02 Jul 2024 21:20:28 GMT  
		Size: 11.3 MB (11294613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90092edca53bb728d1d06f3d69125fc61fc5ea000d537a582a50391757705a45`  
		Last Modified: Wed, 03 Jul 2024 05:23:12 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59068fb80142a919ead538d997164cf8ac4ec160f3743f0d56790972561da363`  
		Last Modified: Wed, 03 Jul 2024 05:23:13 GMT  
		Size: 2.9 MB (2873973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a826cdfedbf5de3a58115b8addf0904ed672804bc332bd63cadd9e6842e854c4`  
		Last Modified: Wed, 03 Jul 2024 10:10:54 GMT  
		Size: 5.6 MB (5595312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.12-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:534cef1a82a85dce036b150b036fe7ed7b339b1dbf1a8ad81d3f8c4c5cc09c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269773b704b51429c5b021c8d0d2771e85a0316f50a7a136d21be044105e8153`

```dockerfile
```

-	Layers:
	-	`sha256:2f784a8e58f5ceb79b0a82aa50f112ce4ca0401cd5defec0e2d5c2150ec8d75c`  
		Last Modified: Wed, 03 Jul 2024 10:10:54 GMT  
		Size: 2.7 MB (2687643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00442d550a5c174a20be79901005fe34e5162bef0ec475c76b834d7727e9dda0`  
		Last Modified: Wed, 03 Jul 2024 10:10:54 GMT  
		Size: 10.1 KB (10146 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.12-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:5f99413cdd8ef7b255103a4bae10d3c324592884532a3783ac35799c43cc9f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53293655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd6b954b4a89d95106096f29cb45a4bf86989cf5b3206d2c09080f98ac291b4`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["bash"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.12.4
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f6b3a4bb814914beb65e8c591972879ce1121505d0011055afc8a097fc82fd`  
		Last Modified: Wed, 03 Jul 2024 00:20:48 GMT  
		Size: 1.1 MB (1088834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091473d1595664e04c7360e756ced214fdd6f00d1bc209fb2ad0e7d77995a74f`  
		Last Modified: Wed, 03 Jul 2024 00:20:48 GMT  
		Size: 11.3 MB (11327132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbae7b1dcd6aa9ae3d08e211f66a0e7ef94cfa906ac6df092ece98830f715410`  
		Last Modified: Wed, 03 Jul 2024 00:20:47 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44983f4ff7319ef6b77dc3634d4f4ce1263d866e952f13e9b35117401b3defda`  
		Last Modified: Wed, 03 Jul 2024 00:20:48 GMT  
		Size: 2.9 MB (2873711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48467db71af2d008722331cb4c3d7a1dbc04b560d2001785087007bc438ebd7`  
		Last Modified: Wed, 03 Jul 2024 01:00:48 GMT  
		Size: 5.6 MB (5595295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.12-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:e78518490eca22ababad46eb1d4bd94074b3b76c850cd4c3fe67d8dd13e97dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf067f81cf1faa14d85527fd2e245462f2b478834487ce43b0915d757b8bdf4e`

```dockerfile
```

-	Layers:
	-	`sha256:a07469f90a9e2ae889676a8425fff804608f366bacac246dd9a4d1ba3924303d`  
		Last Modified: Wed, 03 Jul 2024 01:00:48 GMT  
		Size: 2.7 MB (2684421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c372b97717a10cf37c4d51d4b56cdccf9636166de998372ef2a9ebe36257fb1a`  
		Last Modified: Wed, 03 Jul 2024 01:00:47 GMT  
		Size: 9.6 KB (9649 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.12-bullseye` - linux; ppc64le

```console
$ docker pull hylang@sha256:4f26856fa018dfd8fb75ec90653e130e89dfef0411d446fd0d7762fc306919f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56136068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e8d41554734d5b5dfe5045f5e0284b39433d4d95e8a4686ad29ffaceb25eeb`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["bash"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.12.4
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:64741f366161eb41a5c86810e08ceabb9f4e4b69ac16c725aa2d48f19486e1be`  
		Last Modified: Thu, 13 Jun 2024 01:22:19 GMT  
		Size: 35.3 MB (35311302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e719c077e3046e1b649b1b984dc04759c8b233d3a42d27bc96eb5df0da64b7`  
		Last Modified: Thu, 27 Jun 2024 02:53:39 GMT  
		Size: 890.9 KB (890889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9cb25da3fad6f8e7549b0daa8a097d7407dd5340d9ba0e67235b79adef1f65`  
		Last Modified: Thu, 27 Jun 2024 02:53:39 GMT  
		Size: 11.5 MB (11538743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6937da7b52a3c118ddc56f2bedaee24216d5733968ae05989d02b612b35f6461`  
		Last Modified: Thu, 27 Jun 2024 02:53:39 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf1d0490a18523ac0dd98fd01b923eb6d378c616f85973986377e974057997f`  
		Last Modified: Thu, 27 Jun 2024 02:53:39 GMT  
		Size: 2.8 MB (2834078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5fb249827e7cb2ef1757cd5e9fd96e96028fa4cd51a0aa5805aee8be2665fe`  
		Last Modified: Thu, 27 Jun 2024 07:06:03 GMT  
		Size: 5.6 MB (5560824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.12-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:1598c90964b64b7bffd0ff10f4157ee4c12a258452a36f1fee94c522abbe985b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2701513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd47b24cb7da28c8cec7b19d9bd8ef054b25cd717c8409bd32f739dd448c170`

```dockerfile
```

-	Layers:
	-	`sha256:f059332886b847e551c6984d5c9326d4bc62ec80bffe1553a61409ad11a240e0`  
		Last Modified: Thu, 27 Jun 2024 07:06:02 GMT  
		Size: 2.7 MB (2691734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b67a56dcb8fd70c6161886e920fcee4a3020534f9e2667760e4f74af9ce0c3d4`  
		Last Modified: Thu, 27 Jun 2024 07:06:02 GMT  
		Size: 9.8 KB (9779 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.12-bullseye` - linux; s390x

```console
$ docker pull hylang@sha256:188927078d354dafab717d79e74efa281d0021237db1e161c1feb3018d88438e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50382396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228b5dbf0a3c4761a2ee3746ab2435ce3f84aefa6e948dbb8ccee2b344e6d77c`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["bash"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.12.4
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14220572a7603ca678630a49daa33ea1fc9e1570b0be8aa0f934f8d0d7c8553`  
		Last Modified: Tue, 02 Jul 2024 09:22:07 GMT  
		Size: 1.1 MB (1075919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22461a621e39cfec29db38130aca775a4e452467aca25591a1dae7b408074b4`  
		Last Modified: Tue, 02 Jul 2024 09:22:07 GMT  
		Size: 11.2 MB (11174497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11d743401868383ae96456d2cda0ae9daa69275372850f50778d62fd879dd57`  
		Last Modified: Wed, 03 Jul 2024 04:55:43 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9e9e5acc69baa0638afb30bffd8d6d35822fdf3d98e28a58880cee2ce6359a`  
		Last Modified: Wed, 03 Jul 2024 04:55:43 GMT  
		Size: 2.9 MB (2873859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c828e0f2869ec47353020687cb91fd22e95597d2493d1ddbb43c5267a55e3a`  
		Last Modified: Wed, 03 Jul 2024 10:14:24 GMT  
		Size: 5.6 MB (5595535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.12-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:7f693a77cd7557ff4d489957edcc3feaba4859ae56b28f6b42c90c7a298f0f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2472fe50e23cefb43648f0991031d8b39f177c4563143b19a8f551f0a67926e7`

```dockerfile
```

-	Layers:
	-	`sha256:40b8aaa35d21f9ed45c373ee892cc4526cadb32bdcba36a5fe487c7d4c266c60`  
		Last Modified: Wed, 03 Jul 2024 10:14:24 GMT  
		Size: 2.7 MB (2687531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad3a773b5da01c01fdc3be1125eb46413493bc6864377ff18ab676f31287b3e`  
		Last Modified: Wed, 03 Jul 2024 10:14:23 GMT  
		Size: 9.7 KB (9713 bytes)  
		MIME: application/vnd.in-toto+json
