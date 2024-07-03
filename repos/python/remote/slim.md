## `python:slim`

```console
$ docker pull python@sha256:d5f16749562233aa4bd26538771d76bf0dfd0a0ea7ea8771985e267451397ae4
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

### `python:slim` - linux; amd64

```console
$ docker pull python@sha256:5eb1d9eb9ef435d2e4aa6bd5cc38bb26b391cb831124e3682c4d191632858b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47515797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d84f5948d07f0d0b1cb5c9cbbfba92669c5f25278fbe25d448611185940cb3`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64cae28bf14ee9ca8961693d783fe7591aed311a7c2aad9b9898e1c3610444a`  
		Last Modified: Wed, 03 Jul 2024 00:17:01 GMT  
		Size: 3.5 MB (3509900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e903b6a67b033750931cd30420776ef569371f51670235efd435667633e5d4d`  
		Last Modified: Wed, 03 Jul 2024 00:17:01 GMT  
		Size: 12.0 MB (12004305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808ac08b160778f5c927a9fc705c113dd3f2772b70c3f7bcce63ae0c38daf707`  
		Last Modified: Wed, 03 Jul 2024 00:17:00 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e9078483aaf4f1c9afe105fb5659021d6422dd240b1550d19c4d859a5e3594`  
		Last Modified: Wed, 03 Jul 2024 00:17:01 GMT  
		Size: 2.9 MB (2875084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim` - unknown; unknown

```console
$ docker pull python@sha256:e29cfb2ac524d0e4ff7fa3bc35b6daa6d9572ca52363a2cd804ecb06c547380b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87f452b367e0c62b6a6621063d4f4d758e5afa686206d188262c97af959e1d7`

```dockerfile
```

-	Layers:
	-	`sha256:522386167d8e596f212989032f0853c9898f956f4a91f79a416d90959d94a32e`  
		Last Modified: Wed, 03 Jul 2024 00:17:01 GMT  
		Size: 2.4 MB (2427823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868f9d440f9303f38bee45e7fac19103ee1576971263f88a2046c64fb427f6ed`  
		Last Modified: Wed, 03 Jul 2024 00:17:00 GMT  
		Size: 27.1 KB (27130 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim` - linux; arm variant v5

```console
$ docker pull python@sha256:c1b74bdacbd4903bcfbf73f5b8683478c83435cfa8e293068efaa102ecc56ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44327609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d17067381fcd4b21677d367a5ac3a7d7c3e5a9fb7173dc7e65a351529abfe23`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3083af8d5b0504ae8578ba893e917c0644e422873b872c9e1bd561b95c73e5`  
		Last Modified: Tue, 02 Jul 2024 20:16:24 GMT  
		Size: 3.1 MB (3080513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a148320800f1565c82dd28b29aba63b286f7ad2437b0a5766fef71c3edcf5d`  
		Last Modified: Tue, 02 Jul 2024 20:16:24 GMT  
		Size: 11.5 MB (11484662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc23bfd8e3d77f7c43847edbbf860a01343de65ac8a524f1fcc1bd1ba59648a`  
		Last Modified: Tue, 02 Jul 2024 20:16:23 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f14ede318c92a3f8b1324e045e9fc4da2a1b65954150f1a220c8fa435c61ce8`  
		Last Modified: Wed, 03 Jul 2024 02:29:20 GMT  
		Size: 2.9 MB (2874917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim` - unknown; unknown

```console
$ docker pull python@sha256:6ec7f5ec2f9a05bcd2668e81165a54863ad6941a3640f35992c97ac7623ab40d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a19cd21d5240536779dc1221ca5631ac10b6aaf1f9afe06dca9b1e97b01f61d`

```dockerfile
```

-	Layers:
	-	`sha256:b37aa504611775335019b46f94c512abee3cf0961beb04793f86dadf2de59f0f`  
		Last Modified: Wed, 03 Jul 2024 02:29:20 GMT  
		Size: 2.4 MB (2431119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:118a8673d274c334b4394f4f32034356b6a5da9915e3adc551ebd5ff7e461c85`  
		Last Modified: Wed, 03 Jul 2024 02:29:19 GMT  
		Size: 27.3 KB (27271 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim` - linux; arm variant v7

```console
$ docker pull python@sha256:136d7ad1e02aad88152919f84bb4c4d88df6ee30c917d314f8bf2bed44b35441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41577766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d6c063a55591d36da283e128bcf6a68079f9eb3ed3435aa3f2f3601b9b9968`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671707060f2688f3172d9033e2b417b06398c09cd5244f4da254ec539f72863d`  
		Last Modified: Tue, 02 Jul 2024 21:39:06 GMT  
		Size: 2.9 MB (2912235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85126a491c40d3ce8b5f4286220353763228887cb5d24f3ced4c391b526c6f94`  
		Last Modified: Tue, 02 Jul 2024 21:39:06 GMT  
		Size: 11.1 MB (11072376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d56c9c35d5e562a3436f6d52735a8b4dc3d2fa39425efed77dbb4a02135e9f1`  
		Last Modified: Tue, 02 Jul 2024 21:39:06 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79de08d6294a29a55a226efcad407baedf8ea6319a899d720b3ae30c9a1aad05`  
		Last Modified: Wed, 03 Jul 2024 06:46:56 GMT  
		Size: 2.9 MB (2874754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim` - unknown; unknown

```console
$ docker pull python@sha256:70b29866089339700dff7c9f8bb6dc889de958702c079d149ed238251f21a791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c960b2f992e6cb6778578ea285186ac21f9a7b1998d144e3064bac376d128c27`

```dockerfile
```

-	Layers:
	-	`sha256:511b94c3d9f9c7ac191b6f4dbf905da0445089c351cf68e4c4b04e827dbb934f`  
		Last Modified: Wed, 03 Jul 2024 06:46:56 GMT  
		Size: 2.4 MB (2430129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:948c9446f107352ad7eab06f39639113472d4ce5ede43a6a2407502d99c37707`  
		Last Modified: Wed, 03 Jul 2024 06:46:56 GMT  
		Size: 27.3 KB (27271 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim` - linux; arm64 variant v8

```console
$ docker pull python@sha256:279fcdf3e7ed5a37b61b205a11bcdea9668fce519694f2bd377a99a2315f7f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47339409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2e08ebc5534e1bc95dcd08bf4604258b4aeb0c9c5910b847d99e6818da1b87`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f13e32d8cd0dd6045ae8e76baa59b01457fb37cef4627f2e033eba1d883a6f`  
		Last Modified: Tue, 02 Jul 2024 21:00:39 GMT  
		Size: 3.3 MB (3329912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee30644a5dcc1af1caabea58d40e7757b2b5e1a7a798ff4ee9569b04b4b8f11`  
		Last Modified: Tue, 02 Jul 2024 21:00:39 GMT  
		Size: 12.0 MB (11977351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c7fa2607b2097467f2c1af3017121be58be80cdee4c1e9fbbe578b5308db04`  
		Last Modified: Wed, 03 Jul 2024 05:22:03 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92b04d5608525910ef7af0f47431e992e62953684e9472a17ebc865e2aec2e9`  
		Last Modified: Wed, 03 Jul 2024 05:22:04 GMT  
		Size: 2.9 MB (2875352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim` - unknown; unknown

```console
$ docker pull python@sha256:254eb083365eb5017ac4f8ba6051eceddd0b1ce6a61b801cf3a5c11de5837a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd5bf6f0a30d528b78215e6624a0dfdbcb6d8e5d73d5ecaa58a438f99cb753d`

```dockerfile
```

-	Layers:
	-	`sha256:41c0656caf4ac4fe7cd4493c4841c59477dbc382db59e3826f01808b8b3d24f1`  
		Last Modified: Wed, 03 Jul 2024 05:22:04 GMT  
		Size: 2.4 MB (2428145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776cf7b03eab0be898efbc565369081981a8fd044bf56f457dce7ad2b77dc051`  
		Last Modified: Wed, 03 Jul 2024 05:22:03 GMT  
		Size: 27.5 KB (27487 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim` - linux; 386

```console
$ docker pull python@sha256:047e058758b05ad9393bd1e9bc617e6bd8d42c20f593c69b0d3c50c12d41daff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48779091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d089c7d82cc4d7bcfa3eaee1aa317c25eee35345c0a006a73a22381a0e9393`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c968d725e9468e1e891f58ccd08740d7f4f528e5e9ee9b3c98bb1136763e1c76`  
		Last Modified: Wed, 03 Jul 2024 00:18:24 GMT  
		Size: 3.5 MB (3507335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8886089e85ddc41e8ef103a8bd3759cedf593e2c08f923fad5fd2b82ce7679c5`  
		Last Modified: Wed, 03 Jul 2024 00:18:25 GMT  
		Size: 12.3 MB (12252543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cec5a9a97c3a738c181c396647c395c5b5a4aa14d21f63e12693ae7e0544b3`  
		Last Modified: Wed, 03 Jul 2024 00:18:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bd64363428b0a3cd042e4b22b6e15231386e524c5570870c012d042f4aa329`  
		Last Modified: Wed, 03 Jul 2024 00:18:25 GMT  
		Size: 2.9 MB (2874708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim` - unknown; unknown

```console
$ docker pull python@sha256:faf8603320af01738a7e08b38d03c21fabc1a10a34b7d1781206f6740e1fc430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2451972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cc532562d4037c10c1cc89b0c5d0e196f459f54e89836c3bbae837a04eb6c7`

```dockerfile
```

-	Layers:
	-	`sha256:62aa606f62205d8fb0030d01a15086f87b3b063f22d5b08ec3e6e0a0a8edb010`  
		Last Modified: Wed, 03 Jul 2024 00:18:24 GMT  
		Size: 2.4 MB (2424897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0016c2550bbfa941e38e9173f5a43c10896a3a61beac73b44a4ff7affbd57a82`  
		Last Modified: Wed, 03 Jul 2024 00:18:24 GMT  
		Size: 27.1 KB (27075 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim` - linux; ppc64le

```console
$ docker pull python@sha256:a6c5f4ffe6c7b78509081321f6339a4f099a1695540b4bff4a7117ed84cfbe64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52322978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ee2e2197b57d14936194cf317d136efab5f88ac7f15fd39761de5b91a2aeba`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127f6c403ccc850ef15c20429df36acc7fe9ed45bf9d7766b1396d833c57a4df`  
		Last Modified: Wed, 03 Jul 2024 12:23:24 GMT  
		Size: 3.7 MB (3708161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722378d30b8652f344ea6bdac3e8eedb5d49a49051815d53db6206c360116047`  
		Last Modified: Wed, 03 Jul 2024 12:23:24 GMT  
		Size: 12.6 MB (12616759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dca1fa3a5217c87ef57898b9cacd4e282ea56ae77ffbfc92c25809394b57cf`  
		Last Modified: Wed, 03 Jul 2024 12:23:23 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6b4f60ce3c93981150d71f4db19dd8ccee2edfcec7b82f09a705f725c4b169`  
		Last Modified: Wed, 03 Jul 2024 12:23:24 GMT  
		Size: 2.9 MB (2875549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim` - unknown; unknown

```console
$ docker pull python@sha256:9b0e718ef0571124f8a7c40c6decfe7f0f4f6040a1d9a60d6cc5def8801cd689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4934ee7b73016024550325eef387ef2c11a26d1bcc823f68cf6f9e95f06b934f`

```dockerfile
```

-	Layers:
	-	`sha256:abbba901ef807c5d1063831c5f7bf72c6c6b93ced2c6dd709bd839ff15d1a340`  
		Last Modified: Wed, 03 Jul 2024 12:23:23 GMT  
		Size: 2.4 MB (2432250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb7f65db6fa5e3ceaf9a2e77eaca611491b648bc9d0ef5780363fe366551d3d`  
		Last Modified: Wed, 03 Jul 2024 12:23:23 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim` - linux; s390x

```console
$ docker pull python@sha256:5c4b90b061a6a5ead4e8d4884e41edae388ea82f09f9a5e4c480ed87f80cd1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45470959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a755acfc67046c528529fe511fe1c4476f75e0b38efdfef85c1103f6ff7dd2a`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 26 Jun 2024 21:58:20 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 21:58:20 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_VERSION=3.12.4
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_PIP_VERSION=24.0
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ac00c61f60b2df101b7cdf90ed319b625ac93b42/public/get-pip.py
# Wed, 26 Jun 2024 21:58:20 GMT
ENV PYTHON_GET_PIP_SHA256=0f8bb2652c0b0965f268312f49ec21e772d421d381af4324beea66b8acf2635c
# Wed, 26 Jun 2024 21:58:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 26 Jun 2024 21:58:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9bf27c1e85db88a8895753d07df07ce2736432c228a810e199a590621a5aa3`  
		Last Modified: Tue, 02 Jul 2024 09:12:22 GMT  
		Size: 3.2 MB (3170396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f8a2f462ee86d0ca25278896a3b5aa11dc88c15c463b635fe620e878556ca1`  
		Last Modified: Tue, 02 Jul 2024 09:12:23 GMT  
		Size: 11.9 MB (11935323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e40fff8d4f170cd21eb083b833e1740f9372fee24f7fb65b3ca553637ffc8a`  
		Last Modified: Tue, 02 Jul 2024 09:12:22 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee269ef3e2463de9e32cd2cb46eb095f7dfb4bca1ca155dffcb5b1c519e094a6`  
		Last Modified: Wed, 03 Jul 2024 04:54:05 GMT  
		Size: 2.9 MB (2874920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim` - unknown; unknown

```console
$ docker pull python@sha256:d5e76d52c4d4c8554856dd2878ceb70f42dd1af9a7fdbf6b96ff9db09e2f4d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f1ad11aab77ae2c1ff3550e106c1eb83bd2b7e2a8f389f9e83e5f2ffdab8b0`

```dockerfile
```

-	Layers:
	-	`sha256:97c3023492ec9a5113414c32d546a1be9654012ffe29490e2da3a686f57a0d87`  
		Last Modified: Wed, 03 Jul 2024 04:54:05 GMT  
		Size: 2.4 MB (2427636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4e71abc4481c632c7ee852dfcb5119181e157017f4eb036de5547967c00d971`  
		Last Modified: Wed, 03 Jul 2024 04:54:05 GMT  
		Size: 27.1 KB (27130 bytes)  
		MIME: application/vnd.in-toto+json
