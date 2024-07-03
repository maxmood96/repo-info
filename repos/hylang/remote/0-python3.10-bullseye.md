## `hylang:0-python3.10-bullseye`

```console
$ docker pull hylang@sha256:779cdfe3f5cb6014cb9378b1cbe48501f4a4b75eb54ebe1e0f4c2dc2d231bcb8
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

### `hylang:0-python3.10-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:9e12f3c044792db034f7558142b7262ead49f00b9cf92c69759d0b151af18165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51369396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c8f29800567509c17af62b8d4966127ffe65841813427b2bcb9a9dc8af5a44`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.10.14
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:f75f1b8a40515466474d554c1d28ffb2cb5a22fe3078de5e87d9c688f2aba24d`  
		Last Modified: Wed, 03 Jul 2024 00:11:35 GMT  
		Size: 1.1 MB (1076292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9adc358e0b8d172c9d9c0d9381b0a84671a264c1a8111adf1ffe4ae6f4ef0a7`  
		Last Modified: Wed, 03 Jul 2024 00:11:35 GMT  
		Size: 11.5 MB (11539359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66e101ef41f6ed207369987658bdcc47cd1840e62b06786feeb7190bb1575aa`  
		Last Modified: Wed, 03 Jul 2024 00:11:35 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b913137adf9e03d733d0bbba7be920d260e2ec2beab25af56fe150ef920a466a`  
		Last Modified: Wed, 03 Jul 2024 00:11:35 GMT  
		Size: 3.2 MB (3158011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee849e13a8d1f0f60a2fcfe2d9976c7303db6ff5c8694b320332af884d439f8`  
		Last Modified: Wed, 03 Jul 2024 01:01:25 GMT  
		Size: 4.2 MB (4173218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:eebdb6b579a1c5108d1442c9a342fafa0a9378d9ebea941f3631046586568e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32344ac7aca3b6d34f587b5dec51c5b3082080a3ab23ff6b1755a05fcc66645d`

```dockerfile
```

-	Layers:
	-	`sha256:acc83c7ea0634a5ddf0db6f44a5a356f3041b0bda852cf30484a0cfab5d7259d`  
		Last Modified: Wed, 03 Jul 2024 01:01:24 GMT  
		Size: 2.7 MB (2686187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0353e632bc260b32637fc9e5d5ac80f1669dfdf095da278c0434d06c9e0b507`  
		Last Modified: Wed, 03 Jul 2024 01:01:24 GMT  
		Size: 8.5 KB (8503 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; arm variant v5

```console
$ docker pull hylang@sha256:dea19ef326f6cea38142278a0c8d4802dd01bc61ae57bc513c9c5d56835904f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48618818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed78ff63bdd15114fc151b11a80caae4117c52b3f05f169261003db57640c495`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.10.14
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:b3c3939a48fa29ce705d0bbb04b8580b10790f1f96ddaae221e58660ee74638b`  
		Last Modified: Tue, 02 Jul 2024 22:49:06 GMT  
		Size: 11.3 MB (11302835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0b1b0fed42927ae849541ac7cdb459e21bf3da2bfc4915a96092a5f734ee77`  
		Last Modified: Tue, 02 Jul 2024 22:49:05 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4493255168d49997352acc9890389616d6b684765049b5623182cb5c2c0f9d04`  
		Last Modified: Wed, 03 Jul 2024 02:38:57 GMT  
		Size: 3.2 MB (3157811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432c083e13c1c7f2b26bfdc1c7ef243b86fbf23659c434336f5e837c811f544`  
		Last Modified: Wed, 03 Jul 2024 04:04:57 GMT  
		Size: 4.2 MB (4173517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:84a1c92315cb0cd6c6226c3c969c607a62ef879c6fc9b9d648c47e90d560142a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2da99f77b812db11d22b51c542f4a58b8ff80ae49ab98ef47a1ccc0a46e235`

```dockerfile
```

-	Layers:
	-	`sha256:27944dcc328bda2e02886d054e45c0fff5d6c2451543df369dc421e3f2315590`  
		Last Modified: Wed, 03 Jul 2024 04:04:57 GMT  
		Size: 2.7 MB (2686429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2eeffcb2f70324e623b2a0f8f4b7a2d3b4411d2768c9272f28cf8a6f1609a80`  
		Last Modified: Wed, 03 Jul 2024 04:04:56 GMT  
		Size: 8.6 KB (8590 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:412b282cd6267962c8c82186ac77159ed3a16e35a0c27488fa51961f0fb9af50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45837298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e50ceab4bd2c9a8977a1f92ee9072b73aa966656d9234033ccf661eb1f3175`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.10.14
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:8f6b86f51340a3604fb76e50f0a570cfda3f798be2eac4fec840ba7c19d55d2e`  
		Last Modified: Tue, 02 Jul 2024 23:58:18 GMT  
		Size: 10.9 MB (10881445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c1cca4d3c9335f3a908adf7d238469ec1bc6a93e29c2e88e1cd0e417fd70c3`  
		Last Modified: Tue, 02 Jul 2024 23:58:18 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeba881f0a427aa76e6014aac83695e7de25af8cf5b034249069146731a811a`  
		Last Modified: Wed, 03 Jul 2024 08:05:50 GMT  
		Size: 3.2 MB (3157755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3204c759e4b629e65a9e8665a7bfbd64f163f7671475d2e9e7877a4156cb95`  
		Last Modified: Wed, 03 Jul 2024 11:25:31 GMT  
		Size: 4.2 MB (4173432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:8e222ccd9bef5a021da45b1d9eeddc7faab972859017b94da2f760b4fd776902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb1775f438f1f155284182d6500f8dc07abc8e4655854291c7c1e0cb8233d55`

```dockerfile
```

-	Layers:
	-	`sha256:bf96eea9a450af7ec1ee688677692efa56d1a35607b571e0b61c683fc624bac2`  
		Last Modified: Wed, 03 Jul 2024 11:25:31 GMT  
		Size: 2.7 MB (2688437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e0e59e1d2e59411de311c7787bc5d1cd8ed4db02c8993cd9a0161aa4811a56`  
		Last Modified: Wed, 03 Jul 2024 11:25:30 GMT  
		Size: 8.6 KB (8591 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:54a0490442c809cb09e1368c4edd92b08143c1b8b6fc7fc368a6f765aa63f0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50083126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e93c09459e2e0709202c42c00f851bc26324ac6d27aa13ee0953e999f21bfd`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.10.14
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:c244351a11da00b5327a6f927c807a69b1e1b9b67beae46eb0be0b234636e61c`  
		Last Modified: Tue, 02 Jul 2024 22:25:25 GMT  
		Size: 11.6 MB (11618078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2f245e8946dad98b8ab27ac4dc646e46a50e28a5de02c03c984e69c07be086`  
		Last Modified: Wed, 03 Jul 2024 06:30:21 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24952c8d5fcc3dc4c7163bac572e7f7ca5ef43dfd046abfeb2852f26ad756537`  
		Last Modified: Wed, 03 Jul 2024 06:30:22 GMT  
		Size: 3.2 MB (3158016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c5d3840cc5e6a7f607be5b22e2960f1086fee40ccb20a97f3b2b2c4219fab9`  
		Last Modified: Wed, 03 Jul 2024 10:15:06 GMT  
		Size: 4.2 MB (4173055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:77bbf758b4fca07b5e4d1a54537ea0e037c0ea069b468fca1b61ed4b71545489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1251f8a83791d9d3653b46a2b2c78cbea0ef7382d2aa1ad10121d0cc9402edca`

```dockerfile
```

-	Layers:
	-	`sha256:fe487ff877e4acc5700198d3851243ed6f7734069bbbb93469338b94cfb6f83d`  
		Last Modified: Wed, 03 Jul 2024 10:15:05 GMT  
		Size: 2.7 MB (2686447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45bd8be86417f0945f01b1ee3d40abbe4b974a08d627a9828cbbf041a2b50ffd`  
		Last Modified: Wed, 03 Jul 2024 10:15:04 GMT  
		Size: 8.9 KB (8900 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:3c7fcf63dfaa9f9759711776499f3d67ec9c6dabed3f30a6a3fcf75bb1516fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52497373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaed894537ae6347de49cee5045b6b633029e15891ebcb945ddf714e9e6d9db`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.10.14
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:d8f862b3459a5f3daa985e0ad568b261b5866d6dc04dfb6aed23ee2e008cd64a`  
		Last Modified: Wed, 03 Jul 2024 00:15:43 GMT  
		Size: 1.1 MB (1088844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d96db2eeb90450d6b8ae69e75a605cc70df4bbdbe018edee78e5e04944fd5c`  
		Last Modified: Wed, 03 Jul 2024 00:15:43 GMT  
		Size: 11.7 MB (11668986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676aa2528e568a92fab4808e7de653f24fba0d6b3df36cd8840f9715e1f70d64`  
		Last Modified: Wed, 03 Jul 2024 00:15:43 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd719d7e1aedd3e473430ec1f6471f7e207fa9b2b349c6a5501fd0245150bb2`  
		Last Modified: Wed, 03 Jul 2024 00:15:43 GMT  
		Size: 3.2 MB (3157696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a73eb8817c0d2d36c023e2868185d63ac59cbaffc164327501223fc3757fbcd`  
		Last Modified: Wed, 03 Jul 2024 01:00:48 GMT  
		Size: 4.2 MB (4173164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:3ae19ff73eedb47b1e7303259529854541311894b94106335b8b0800cc3eeb3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a0c8482a0b8053e3b046b3ce7868b4cf7454d0311439b0d82df66f76eee1e6`

```dockerfile
```

-	Layers:
	-	`sha256:f570133e2e43a0a1d4aafc7f6bd2ded3d6095b713895d755a31f808a740e4d97`  
		Last Modified: Wed, 03 Jul 2024 01:00:48 GMT  
		Size: 2.7 MB (2683293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be3ff7ec5dd454a67846d2aa4b3b3bd7bbff74bab1d7f4fd91d6351b813b5af9`  
		Last Modified: Wed, 03 Jul 2024 01:00:48 GMT  
		Size: 8.5 KB (8471 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; ppc64le

```console
$ docker pull hylang@sha256:f50b5e58caba2de8e794c24476b8ff78232f44d7e7c6478770fdcd5599cc05ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55420300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4924331cdb139f640559ecd26e60e76cc4940a218aaeb3c940e6f6dd83c9b21c`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 21 Mar 2024 23:32:08 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
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
	-	`sha256:fb10825c9d0995282ce2c7de2dd2ac72f275fb560a516183f7a78f84502c3238`  
		Last Modified: Thu, 27 Jun 2024 05:40:55 GMT  
		Size: 11.9 MB (11886218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dbafa8a29fad53ef8f33d20031233bafc7a1155d02c73ccd9fe09295661e03`  
		Last Modified: Thu, 27 Jun 2024 05:40:54 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c12db81627f20fc0274947dee01c57e43ae6ccaa177621dba537b6f3b8919db`  
		Last Modified: Thu, 27 Jun 2024 05:40:54 GMT  
		Size: 3.2 MB (3158571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b7d2097b36678decbae48c5947e24f19062cfcec2c69c3870bac2688e0ae28`  
		Last Modified: Thu, 27 Jun 2024 07:12:02 GMT  
		Size: 4.2 MB (4173089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:4a768dd4351e26840f39fc9726617733e1c3843ebd48b7d93592d1f8ba9b30fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84be75e56960715c14db692db0716244436839876074923e4c4dd95d3c6606c6`

```dockerfile
```

-	Layers:
	-	`sha256:63826fc14d42934c2ef2137c662af14118fbd2839aac90b6ebfdf76e77ad0a6a`  
		Last Modified: Thu, 27 Jun 2024 07:12:02 GMT  
		Size: 2.7 MB (2690562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e1e7c432196e2f7213f2946f10480aa49e7abdd85c72184f484964447799eb7`  
		Last Modified: Thu, 27 Jun 2024 07:12:01 GMT  
		Size: 8.6 KB (8557 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; s390x

```console
$ docker pull hylang@sha256:536179411afe6ed6c63876757478d77a58eb75218ff2c3ff39eb075441f62acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49536944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fcf786af8c71859fcbac3ff838c531595816e8bebebb69b4fc8a0d2b999281b`
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
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.10.14
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:bce4d1c89e0115b616c86c88c1bfc0363cdaea7ab3197a75819b1f8c35b484b7`  
		Last Modified: Tue, 02 Jul 2024 09:54:15 GMT  
		Size: 11.5 MB (11466950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb618a138690dae332d10b9161c8693fcbc9b202e0cd06b84da65fd0cad886f`  
		Last Modified: Wed, 03 Jul 2024 06:02:33 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c476dab9f0c6552aa2d64f64584714e2098fd9e46a448921dfeafe9ef67976`  
		Last Modified: Wed, 03 Jul 2024 06:02:33 GMT  
		Size: 3.2 MB (3157934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769f0e5e0adb65f8e0f6647cc5ddcf2f72fc1044986e0c14ef408368553f5b07`  
		Last Modified: Wed, 03 Jul 2024 10:21:05 GMT  
		Size: 4.2 MB (4173556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:73aa8f571d193bcb02a29044d102bb97c056dec34675ad6cddf514a0184bceff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccfd18715b276d34855ff577d55ac15e313b64a3a88b5d4bd21d7baff67c593`

```dockerfile
```

-	Layers:
	-	`sha256:2484fbaf4728dc3d625790bd8a827ebc17e88588e17393bb8ffc9e61a5060c2a`  
		Last Modified: Wed, 03 Jul 2024 10:21:05 GMT  
		Size: 2.7 MB (2686383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1049fc9b604287b52bd0e1849e832ca24205fd959aa1ada6d8aa42da7faf7447`  
		Last Modified: Wed, 03 Jul 2024 10:21:05 GMT  
		Size: 8.5 KB (8515 bytes)  
		MIME: application/vnd.in-toto+json
