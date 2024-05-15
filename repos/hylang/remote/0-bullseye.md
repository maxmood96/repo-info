## `hylang:0-bullseye`

```console
$ docker pull hylang@sha256:18744cb67b1b31f5d6e1d3462e1713bb18045c7d742acc3925767ab213482d72
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

### `hylang:0-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:89d4f72e3c5dfc546fdc6cfc6279bf7524e5f1e13d6ed504217dfd8c02ecf47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52366239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dddc6e5051751100878cf6e8b28da3313127406eecc5ceb76cb8176c08e26d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.12.3
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1ca9b4dc3e3a61667ce56aa8973a0f79300a0d2bc1c677608fca5a20a6e71c`  
		Last Modified: Tue, 14 May 2024 09:20:53 GMT  
		Size: 1.1 MB (1078202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff314948cd748157816b418ffb8d5a834c58552d2f147552adeda9ffbaacf9c6`  
		Last Modified: Tue, 14 May 2024 09:20:54 GMT  
		Size: 11.2 MB (11218985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775eb0fca1f366c27e2eda6e40d178cd366d34d92171c3ca2fd10ec0b06c010e`  
		Last Modified: Tue, 14 May 2024 09:20:53 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cb43d7355fa62d470ac0cb430951fb68529f463c217aa6911419c20286b436`  
		Last Modified: Tue, 14 May 2024 09:20:53 GMT  
		Size: 3.1 MB (3063186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa55134126bdf6464f54fcb593bd67190f16201b160fa03f379375da54279011`  
		Last Modified: Tue, 14 May 2024 09:57:36 GMT  
		Size: 5.6 MB (5571691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:c51f64a5d356ff8dcee8c9e3ccaa355b96e852c4f7093dca7f2a1cc9fd9ef003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c95ca786f4dbebde9b3cc89d9b741a85d22eaafc896c678cb96b5a30c87253`

```dockerfile
```

-	Layers:
	-	`sha256:e35f633062c6022385fc55972f2ffc0d7a0173946e38fa918d5005bd7f98038c`  
		Last Modified: Tue, 14 May 2024 09:57:36 GMT  
		Size: 2.7 MB (2684253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b170646abbb0d7b23ea8966978304bedca4a02a88fe47692dbf7ded3158b83a2`  
		Last Modified: Tue, 14 May 2024 09:57:36 GMT  
		Size: 10.4 KB (10351 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-bullseye` - linux; arm variant v5

```console
$ docker pull hylang@sha256:aca08ea91467966b67d823f225f01286d276ef3d1bb4fe865888dfb7302c6126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49543832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3826dd66d18428982ba77256223a7ef82ebd71ff2ac00454430857ba2f089f9`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:7a63cf2b5d16adf102fbd2452be219224667c4ea55981247f398a4a867ef96c4 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.12.3
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b6ea79e472ea80a508a2732ddeb0e19de51d3f0aaf8f0fd18c1cdd1c939d49de`  
		Last Modified: Tue, 14 May 2024 00:52:17 GMT  
		Size: 28.9 MB (28936721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f0f3c3040a85d02b480f9db8c19a0aaf1facff8dcda11fe342738e98f422e7`  
		Last Modified: Tue, 14 May 2024 06:13:55 GMT  
		Size: 1.1 MB (1061248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa42fc5cf1aab8073e72dac8323b3b74dc1db66984fae1fe2da27b34232489f`  
		Last Modified: Tue, 14 May 2024 06:13:57 GMT  
		Size: 10.9 MB (10911016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efaa03ad6f4f5ee6d714345d101b4d5db0924b1df148f54871fbb6d14398819c`  
		Last Modified: Tue, 14 May 2024 06:13:55 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2454f54f1573c049f660d2c008f38415eed906dc1bb57b4ca53db492edfaa61`  
		Last Modified: Tue, 14 May 2024 06:13:56 GMT  
		Size: 3.1 MB (3062736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e24b60984732deb5c1fae2b050a3a67ff64b8b74002f940557b4ecd018fb5f6`  
		Last Modified: Tue, 14 May 2024 22:32:17 GMT  
		Size: 5.6 MB (5571869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:4220a30c3710006402e89aacbb6c7e3627f957e7f69d06574e254ab99311f5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac361028438e8c8c73ad9849eceed556aedd80e465dee3aebb9aafd702972db8`

```dockerfile
```

-	Layers:
	-	`sha256:7c10f389d98ca7489502f51ca26605cc4491f33bc770df2b1df3c51d5e2e56f6`  
		Last Modified: Tue, 14 May 2024 22:32:16 GMT  
		Size: 2.7 MB (2684527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b257047cde821f479d1ef2e1f5badcac5d8a7e7b7e980b5d45bfb3a80f25f241`  
		Last Modified: Tue, 14 May 2024 22:32:15 GMT  
		Size: 10.5 KB (10453 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:8bed3a0c10e5fe2e5b1886587380907c4b47b004ecd07b86bffd75893f28b921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46745257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34737ee154a6b1e4079bc1ac40d436a286ae37adda6cd8bbeb2a0c2cd188c15d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.12.3
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266e3b43e28b4a4eb703026ed4e0c556ccd74d0464a7c2f4972661be125d2b30`  
		Last Modified: Tue, 14 May 2024 09:24:38 GMT  
		Size: 1.0 MB (1043219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805c69b6677a6c92568f9793343c04855449c1eafc12f6e85835074f73c59806`  
		Last Modified: Tue, 14 May 2024 09:24:40 GMT  
		Size: 10.5 MB (10472846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b76f23e23b85a9e272185999b7dc2cc9bcc3ca1451dd7ded072358aef349427`  
		Last Modified: Tue, 14 May 2024 09:24:38 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6994115c076694cf3454ffdf9e51cb18aa9d7bc94cac882d5d5506764eef793`  
		Last Modified: Tue, 14 May 2024 09:24:38 GMT  
		Size: 3.1 MB (3062722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd5f856f22376010d9f5dad6f5cb422fa69d1803c27fdd77134e7887fd1e2a5`  
		Last Modified: Wed, 15 May 2024 08:24:57 GMT  
		Size: 5.6 MB (5571734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:e9774b3513af83bf5da4f2b2b3fbb73c885c66c860b107b725e714bfd3e3fbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed891fa5a2e48976f9f8553fe75d3f6ffd4c5d5d2ac13c633a15a425fccc7f8e`

```dockerfile
```

-	Layers:
	-	`sha256:6b3ad2447522a960ef892697c2b71b0fcbea94601f4cd34f39a9d82005623b87`  
		Last Modified: Wed, 15 May 2024 08:24:56 GMT  
		Size: 2.7 MB (2686535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c2251e9c57659fd32b1cf731163b7b43adbc041ee02b9959d3244e6e29681e8`  
		Last Modified: Wed, 15 May 2024 08:24:55 GMT  
		Size: 10.5 KB (10452 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:69f430ceb7cbab6e6e088797ddb358618a650efe03f9bb6baaefe98de5fdc390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51074344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64076adc14004ccfee90dbed196c61bcbe691c2376c62d432d61b744eb59712`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.12.3
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677786c8fd4e2bcbd58e895f7759126964177be319e2bfdc6a2d56fb732e6d59`  
		Last Modified: Tue, 14 May 2024 07:27:03 GMT  
		Size: 1.1 MB (1066080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186d528dacd9bc40a6c16294490a8b5386557406a01e998659d125b38bf310fd`  
		Last Modified: Tue, 14 May 2024 07:27:04 GMT  
		Size: 11.3 MB (11286493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0568d02bd638d0430fb1650275fab22912d1b351c0dcbb3c4927b6421675c5cd`  
		Last Modified: Tue, 14 May 2024 07:27:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b71081d104be277a0f63becefd7b6f65948c49d30967a3e8b9a3b85a7264e9c`  
		Last Modified: Tue, 14 May 2024 07:27:04 GMT  
		Size: 3.1 MB (3062983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3199fc3db520c8c1a9a8d6f92106c1a8e2b985bd17953a995a1fbd5db9ee32b`  
		Last Modified: Wed, 15 May 2024 16:30:49 GMT  
		Size: 5.6 MB (5571637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:d4bfe52478fb83f57730edf5099d261414de2242e9de4bc39aaf14fc3b22e59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b76d1906fd0f30c306f3bd0d067cacc5c68312521fc715f30cf0f97f8ac8e20`

```dockerfile
```

-	Layers:
	-	`sha256:4846587a9359c1f098b8a3298d796dec003045f8da40aac615e7d4490b34693b`  
		Last Modified: Wed, 15 May 2024 16:30:48 GMT  
		Size: 2.7 MB (2684476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b180cb0c91ea0fe843da4c1c4de5a9e1b2b327b3fbb6ce4bc7a1f6da550831cc`  
		Last Modified: Wed, 15 May 2024 16:30:47 GMT  
		Size: 10.4 KB (10369 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:e096305b3106e65d7fd8cb52e945dd865187a4eca6f0be37be83a743338586a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53465089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e236713df534f1054d6a9ba3be4986be178b6eff48fcc8a66be9d417f0df064`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.12.3
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cd7886b26acdcde7f6b2314b2d4c75c4c09201287ff2c45311bc8f404cd6dd`  
		Last Modified: Tue, 14 May 2024 08:29:53 GMT  
		Size: 1.1 MB (1090943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f13969ea23cff2ed7f056fd896b551d6579f0ddb9ff216d8df1dbcc2120217`  
		Last Modified: Tue, 14 May 2024 08:29:55 GMT  
		Size: 11.3 MB (11315382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c06479515e8387f03721b1260778b1f40edfc9476d27aa105edc46890fb716a`  
		Last Modified: Tue, 14 May 2024 08:29:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04104e8070c73ee8fd7b3c18549982e9d46afdea14750e4b604833720eea91d`  
		Last Modified: Tue, 14 May 2024 08:29:53 GMT  
		Size: 3.1 MB (3062850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf91c42675ebf3c3c5538c3a083b34fc4470d4004837370e4bd592630cc9d037`  
		Last Modified: Tue, 14 May 2024 08:56:26 GMT  
		Size: 5.6 MB (5571627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:78f2c8689966b0c752bca1eee366032f9601e9f76a43c4b79fe395aac009ab41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d99c8f7ff7bf442f8f42891d169ac4771f178389a2831aaff354f7c7912025`

```dockerfile
```

-	Layers:
	-	`sha256:6fdc267d51228cfd5427ccaccb9234999da051c02360adb7991ea1e27296ab7f`  
		Last Modified: Tue, 14 May 2024 08:56:25 GMT  
		Size: 2.7 MB (2681339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806a56cee60198fa5cf51839594cf663d0b63ff7e3db6dc217cee73a88bafbcf`  
		Last Modified: Tue, 14 May 2024 08:56:25 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-bullseye` - linux; ppc64le

```console
$ docker pull hylang@sha256:8bd5b534c9bccdeeeb491c62bd65726ea847217815e74301cf5d7dc48d422406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56575474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0baedd1f1314e30af29c83d8664841f7a1861fface4638ff2d046bcbbb664171`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.12.3
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e09fcd9c4184dfa956e22dfad7a592e9ea5e95df5d38d5e05eff8ba6c02a38`  
		Last Modified: Tue, 14 May 2024 04:48:15 GMT  
		Size: 1.1 MB (1096847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b369cfa55d637a820c4ff4c23164857aef0a116597ae884f855ecce91df9ce25`  
		Last Modified: Tue, 14 May 2024 04:48:17 GMT  
		Size: 11.5 MB (11531854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa30d077d93e872d81abb88beaa4080302f282df1d59943ab6115a67af91c08`  
		Last Modified: Tue, 14 May 2024 04:48:15 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67f56711e10c5e94a59148a666209bdc9ae484aa068d9571c4902a742d90eec`  
		Last Modified: Tue, 14 May 2024 04:48:16 GMT  
		Size: 3.1 MB (3063516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dfd4aa5b0232719f26cdde5885447c53b500ff9bca6c6cf0771ad6e2a1729e`  
		Last Modified: Wed, 15 May 2024 04:32:39 GMT  
		Size: 5.6 MB (5571854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:7abfaf2d87d49548f87a414f64e03aba4d4af11fde612ddddf493a1e9d49ee96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d2ff788a60c4f5b7d98ba9a277decaa711e46fc14b24d297cb53faf1c9bcf8`

```dockerfile
```

-	Layers:
	-	`sha256:a6132ffc153033551dbe9280db07e08485063b868555709fd4a87341d619cdc7`  
		Last Modified: Wed, 15 May 2024 04:32:37 GMT  
		Size: 2.7 MB (2688654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03d898f0830f9fe12fd8d4a46ac5cfe39f9236c99fe953d3d1583d48a3ab4fbb`  
		Last Modified: Wed, 15 May 2024 04:32:37 GMT  
		Size: 10.4 KB (10413 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-bullseye` - linux; s390x

```console
$ docker pull hylang@sha256:c51d14d21389ff9da7969caae5db92bf0860c69aceaeb9460d785b31f023830e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50550624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbae49882cf19ece1918a9aa3c8ea8ec8f901b5f4d9e3e2ed1d2f20ed8fd7dfc`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.12.3
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ef64954ab5f27b054e5193a752fcac96a4a5f22e6b97b453de70c43772a3f5`  
		Last Modified: Tue, 14 May 2024 05:24:50 GMT  
		Size: 1.1 MB (1077688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02587f3bb4952e68baac1d69b783a93ec65cec0db80d9c0774d834f069a7e398`  
		Last Modified: Tue, 14 May 2024 05:24:51 GMT  
		Size: 11.2 MB (11164352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d34ccd83e7fa01207e1d611ee04197267c0610942b08c5a0684d2b57dd215cb`  
		Last Modified: Tue, 14 May 2024 05:24:49 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccd326f0c80245f346ac4f68c984c196b1d281a6079ae05bdb2b0b2cf2cfda8`  
		Last Modified: Tue, 14 May 2024 05:24:50 GMT  
		Size: 3.1 MB (3062902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2410e5a62c723c371798f67b7738b3191211e371ff8ab2f3386a1a9aec930e`  
		Last Modified: Wed, 15 May 2024 03:32:57 GMT  
		Size: 5.6 MB (5571782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:f9699dbb2a0bf5fff1a9159a013c386896dcb293a011b74f7fc9135f60e64abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3142129d707c8d6baf14c7b48ce487365ec56b939ace0965969ed865e86028ff`

```dockerfile
```

-	Layers:
	-	`sha256:f1c09dc2a1ed3341877927046719cfcc70b9043efc47c47224b92f9e09cb129c`  
		Last Modified: Wed, 15 May 2024 03:32:56 GMT  
		Size: 2.7 MB (2684449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5c761b0a15509d6dd687f1b754173e02caa301d90b42a412ccf3ebf26e24a52`  
		Last Modified: Wed, 15 May 2024 03:32:56 GMT  
		Size: 10.4 KB (10351 bytes)  
		MIME: application/vnd.in-toto+json
