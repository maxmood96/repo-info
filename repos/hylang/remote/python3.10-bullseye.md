## `hylang:python3.10-bullseye`

```console
$ docker pull hylang@sha256:a07cd3c8a2440bc504fe68ac5bcd55af8d89374dbbc7844382f43032b943fbb4
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

### `hylang:python3.10-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:d1f34d75d74c0ebdfbd6c93415419ac2c3484e6cdaaf151a9fc9a86675ba192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51369835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658da83f4cc8134c7f33461251dc29c776b2c5b3db99373911745b5f0cb26ee6`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80d9280082bdfedadb129e7c704495ff2ca50167c6a3f47f91348f4962746f4`  
		Last Modified: Wed, 10 Jul 2024 19:06:47 GMT  
		Size: 1.1 MB (1076285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773171ea0025c5c0bf49a06d9e852ad74e4dcd93e7719cde485513196972c17`  
		Last Modified: Wed, 10 Jul 2024 19:06:48 GMT  
		Size: 11.5 MB (11539431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696497820dab4dc3481908b491822fd2c319724d97ed3091fd029604ccaabac5`  
		Last Modified: Wed, 10 Jul 2024 19:06:47 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9588dc194b6c1d3949bf1a84dc90e32e2f4cc0fa8c01848d7636ec54fb870cad`  
		Last Modified: Wed, 10 Jul 2024 19:06:48 GMT  
		Size: 3.2 MB (3158101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a10c68a1068f7615f2cf41783bed121b607eb3f12ec7889ab291e47831b124`  
		Last Modified: Thu, 11 Jul 2024 16:58:10 GMT  
		Size: 4.2 MB (4173501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:5a16dfd34ebc2f9a06abf116dac4b95aa277659ee166d47e08a6626605851a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9730636684a523480aa80f009ae6f5a35a91319f6076401fa8b9fca3ee347404`

```dockerfile
```

-	Layers:
	-	`sha256:b7f0f447a714f93b2133d4cb674e4b36648f6883a3a6cf46ccc9ac2d7dfa765f`  
		Last Modified: Thu, 11 Jul 2024 16:58:10 GMT  
		Size: 2.7 MB (2686187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60bacb2ce1ace6777e40653c36fe3cbb83d768c742bc65a3924a6881e81fa0bc`  
		Last Modified: Thu, 11 Jul 2024 16:58:09 GMT  
		Size: 8.5 KB (8503 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bullseye` - linux; arm variant v5

```console
$ docker pull hylang@sha256:0e3bf6973ce14459f4aa4ad623fe7d26f9cb50f6994e27fdaa2baf51a1dd1e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48618983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c642ab23dd24be4a72d7601238259920129d2a6c4bb1185f0607822d7b29e7`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:43 GMT
ADD file:7b150e5fe9a4f014196e0bfb8275f3406ad543dff58b049264b54e2e00f392b5 in / 
# Tue, 02 Jul 2024 00:48:44 GMT
CMD ["bash"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:18cee74f213a3301147afdb9cf830a5bc400858ea881a037e9afb0a56d95281f`  
		Last Modified: Wed, 10 Jul 2024 19:15:46 GMT  
		Size: 3.2 MB (3157786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffefea50b685a715987406319b107f38078b5bcde37ca94187920915184ce2fe`  
		Last Modified: Wed, 10 Jul 2024 19:59:08 GMT  
		Size: 4.2 MB (4173707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:53888ff4aa43e94ec064f8a1bd893e27beae11827254deea2f3d8a148d418468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883b614da4364ead4c0cd951efb44b0dbe1e3e83f9973fa6113dbcdfdca9777f`

```dockerfile
```

-	Layers:
	-	`sha256:62a59f8a52fa21b99078be7636fd62178d0bddabbba886cf136cb5379f8f5cb9`  
		Last Modified: Thu, 11 Jul 2024 16:59:39 GMT  
		Size: 2.7 MB (2686429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d939d15f88edb6a891eaa7021d1ba9b3700839f0d99b408fff67d9c3b4b09601`  
		Last Modified: Thu, 11 Jul 2024 16:59:38 GMT  
		Size: 8.6 KB (8591 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:52a87728b8375c812563f726f0e23d7f0c96a30633cf8a6bbad60733c5e4f72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45837685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409cb1bbc81752808dcacfadac240a891ae1df589e810fba0ed4411633127957`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:21 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Tue, 02 Jul 2024 01:00:22 GMT
CMD ["bash"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:7f837164375122a4485b3a798df77e2028e6325aadf6fde4b368e6f0d9f42347`  
		Last Modified: Wed, 10 Jul 2024 19:18:28 GMT  
		Size: 3.2 MB (3157879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288a646022f73d0262b6461004e9ce6397c6e70e65f47740c5a097aa85d1d1c9`  
		Last Modified: Wed, 10 Jul 2024 20:10:48 GMT  
		Size: 4.2 MB (4173695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:6e087b85f9f6bd24d4b9795d980601a2c357fa56e89a2f1fb56c48c8b59de419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1e039cf98cd42019fe5a45f47b19046bca00156325697db85f3350ef128e56`

```dockerfile
```

-	Layers:
	-	`sha256:926118813916ddbadf9b0dc9e429abbc85583af2e50fa2cbce61928ab07a9b7d`  
		Last Modified: Thu, 11 Jul 2024 17:00:49 GMT  
		Size: 2.7 MB (2688437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a5e98914192592cb8a880ce2b506b8c3fb855006c4d70f9d19f24c892d421e0`  
		Last Modified: Thu, 11 Jul 2024 17:00:49 GMT  
		Size: 8.6 KB (8591 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:fb87399fc1ab56d2c71baa0efc628ac36efc80a92403867771c4584a2945476b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50083542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21b706bf9d174a7b27e28cc4961fd2cec9d7c6349681ce90a0a9751a9cbe155`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:720ff8aad1f88a8dff154dd2554798aacb1fce59f545e5584f19fa92d47916c6`  
		Last Modified: Wed, 10 Jul 2024 19:13:57 GMT  
		Size: 3.2 MB (3158044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37a116d2d3645d94e20498742550e6c42fe7cf0a6f9ea130a629466e0925a43`  
		Last Modified: Wed, 10 Jul 2024 20:04:33 GMT  
		Size: 4.2 MB (4173443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:ddadb4ce2388030d2026e90f3674768e52c9d840a82ff66d235b6d2811aee991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993749972606c5e3e0b3b3436bf80bff6b74e5692f86d6ad492528198ee00932`

```dockerfile
```

-	Layers:
	-	`sha256:c584815ef73d677b1265a3a502c2c0a961c259358b1b8c9f92a809a7ef2839bc`  
		Last Modified: Thu, 11 Jul 2024 17:00:44 GMT  
		Size: 2.7 MB (2686447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e850808891cc79c814404dbb15e5ebc3fb595eabd01263a8fb23981d66a7ab0d`  
		Last Modified: Thu, 11 Jul 2024 17:00:44 GMT  
		Size: 8.9 KB (8900 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:27b0b909fdacd024e5b2734a7f2380c891e58d3911ea8dfec157574812f29e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52497463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa59f1f631f13df694f118f2318816ba6888bfcc746ff7abc1a8ecd782e01ac9`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:16 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Tue, 02 Jul 2024 00:39:17 GMT
CMD ["bash"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a7b158c6a075e09f2ba66b9517f6cbf6d2993f1cb8c0082a6c479dcc5e02cb`  
		Last Modified: Wed, 10 Jul 2024 19:09:57 GMT  
		Size: 1.1 MB (1088889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42e3fb0a58b3b91e65c00464341713d3d97074ceed9b1a9c61b08e9e49e04ed`  
		Last Modified: Wed, 10 Jul 2024 19:09:57 GMT  
		Size: 11.7 MB (11669014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e0117a0f1c496047f948bc6657c7f934a042836ab711cf2ce3b5694b4abebc`  
		Last Modified: Wed, 10 Jul 2024 19:09:56 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39a03587a6933799a24309b19a9c4a8c6ac0f84ec254a52744fd860c17e2b4a`  
		Last Modified: Wed, 10 Jul 2024 19:09:57 GMT  
		Size: 3.2 MB (3157788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799db2b59f013927650bcfce1350a88223c7a8602ad1a0f21234f6abf087f751`  
		Last Modified: Thu, 11 Jul 2024 16:58:06 GMT  
		Size: 4.2 MB (4173087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:1774dce7a8b105c0c6d43b6b5078ddeb6a2e4f0feebdd7e312d6f438af4dc9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f5f7074f22e8a4f376a2d88c4d653361eaffd7dd773048928e6ef26f2de929`

```dockerfile
```

-	Layers:
	-	`sha256:8dae76bd57161bfbae67b0a5ebced0bc92356acf39bd46d6162ba2718afaa202`  
		Last Modified: Thu, 11 Jul 2024 16:58:06 GMT  
		Size: 2.7 MB (2683293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3cb6c111b63f81afb0d01c0920cd5559fb9f4cb2bdcaaa44e16a425de0e246a`  
		Last Modified: Thu, 11 Jul 2024 16:58:05 GMT  
		Size: 8.5 KB (8470 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bullseye` - linux; ppc64le

```console
$ docker pull hylang@sha256:7671516a5503fb5b3361eda3e8c2f2f60b5128dc2676d1712a19ad593943104a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55610944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1628d7810af059188b6a46a908624ba872fb8688e3a8162b1f2761ad28af301`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:03 GMT
ADD file:8fcbfde241e9377ada40ad73089516c86d20e018c99a8192ba63a50f0168b8b9 in / 
# Tue, 02 Jul 2024 01:18:05 GMT
CMD ["bash"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:687d52b24394339ceb9470debd0e5f0d6b612ceb063cc228cbef23d23fb7f6a2`  
		Last Modified: Tue, 02 Jul 2024 01:22:46 GMT  
		Size: 35.3 MB (35299189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bb4d7d6f5ea93020aee1c796b84ffdc8197c451898058312c2fe823ccd4b1f`  
		Last Modified: Wed, 03 Jul 2024 12:58:01 GMT  
		Size: 1.1 MB (1094935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a42ea863703d1440319da63476809d1840c83c3808b019de91799f3fc747385`  
		Last Modified: Wed, 03 Jul 2024 15:49:09 GMT  
		Size: 11.9 MB (11884444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b27ae410610da1603700fac07e05ada17d620d0694655e85a77b351fb978e3c`  
		Last Modified: Wed, 03 Jul 2024 15:49:08 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd680d61e9794b84c77429b6d8decf2679ab9332a876da67fe5341ed1b4334`  
		Last Modified: Wed, 10 Jul 2024 22:24:16 GMT  
		Size: 3.2 MB (3158538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c29e44da3db4d3c4b22bf595ccda8dcecab7835787b7e2c09bd704079c0bff2`  
		Last Modified: Wed, 10 Jul 2024 23:20:58 GMT  
		Size: 4.2 MB (4173608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:567b31c5a4c0138693084cf12d374227311e2880df9aed2b30d6a70c3c956da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acf498eaabc758029a1bd6fe227bdff09e47cdcd8816facf309ec21d7ae364b`

```dockerfile
```

-	Layers:
	-	`sha256:fada1a2ad7fa2ccfe15f914ce9394de2d9e038e810ad8b40c5d0e94d13c0d1cd`  
		Last Modified: Thu, 11 Jul 2024 17:04:07 GMT  
		Size: 2.7 MB (2690564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c970defc2e081badbae887cd8c2d915ec0e54218b2ed7ea556a0b85f76c80e83`  
		Last Modified: Thu, 11 Jul 2024 17:04:06 GMT  
		Size: 8.6 KB (8558 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bullseye` - linux; s390x

```console
$ docker pull hylang@sha256:e4892eff66748cc5d69fdfd61cb7bf3afa0817e2c5663603b4a08ebf9d8b2a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49536822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d3538555b055205fad53d800dc267a7be408dc744e48dc195c0953d9b72e54`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 02 Jul 2024 00:44:15 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Tue, 02 Jul 2024 00:44:16 GMT
CMD ["bash"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:87689254f0689daf8f62b6a853b509226c7b3b41067047ebcc829f4b347e7fc0`  
		Last Modified: Wed, 10 Jul 2024 19:19:14 GMT  
		Size: 3.2 MB (3157907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d505395ef8650eda9f1027f310957e7dac0881fe1ad83b5f220a4fbcf574c6d3`  
		Last Modified: Wed, 10 Jul 2024 20:11:13 GMT  
		Size: 4.2 MB (4173461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:4a65568ea5c5cbf9628c51702f661a6fb498f0c766ea2a492d43bca6ece36e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccb965f54df87993c6010fd61071a408f26b87ae6320876fc33b2c76eacca1e`

```dockerfile
```

-	Layers:
	-	`sha256:01453899758b2e3a0d4d030e22bf456e189a67bba635e6bac06d8a5e90b08c97`  
		Last Modified: Thu, 11 Jul 2024 17:03:08 GMT  
		Size: 2.7 MB (2686383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f7cc5a24c24a5cd78e244181713c6c164f6f3a52a930c315363b1294a145586`  
		Last Modified: Thu, 11 Jul 2024 17:03:08 GMT  
		Size: 8.5 KB (8515 bytes)  
		MIME: application/vnd.in-toto+json
