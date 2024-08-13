## `hylang:0-python3.9-bullseye`

```console
$ docker pull hylang@sha256:235eaf40507ed597f5c2fef212b0ad829b75be9629385f169d501f6acc1ca107
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:0-python3.9-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:83899fc1cf710fbd91197b87e3f54b8d6178e25d57c1237b3b64022600f50324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49974902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c21663821da3465867692be67deba271242bc5faaf1af81800fbb1b26faf97`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1c8976519d9b16187156b76ee3051c0cc94a5f7be68aa751684d6c8fd34a68`  
		Last Modified: Tue, 13 Aug 2024 01:15:44 GMT  
		Size: 1.1 MB (1076288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea85b71d103fc78de736df30cca2fb8385946ed7433989a782859997ad1b96e`  
		Last Modified: Tue, 13 Aug 2024 01:15:45 GMT  
		Size: 11.0 MB (11049657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672e4cffd2e83dcd9d2ae9bb2ddda7502a24b9f6fe4b2c6f6a358c941e5f31b9`  
		Last Modified: Tue, 13 Aug 2024 01:15:44 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1df16d1d788375971c6ea9141229399eabfbe82bf8f811d9c0244f630c9b8de`  
		Last Modified: Tue, 13 Aug 2024 01:15:45 GMT  
		Size: 2.8 MB (2772587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd9c8c1d4847420730a96c76bcf1bc5b91f56e77eaf00ffce29983a74bd53f9`  
		Last Modified: Tue, 13 Aug 2024 02:17:31 GMT  
		Size: 3.6 MB (3647851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:a9b33706a651fa2e7a078dd442ff146c371b83be7bea5701f8b4cd6a90260327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c442be8bfcf2c8218053e8346d11baf45e3af50f76a2759bedd1e58a7bfd27e7`

```dockerfile
```

-	Layers:
	-	`sha256:62b9b15ec02b432c45c857ee24c0a0f0822e7f2967093d6bae4702d8bb3726f6`  
		Last Modified: Tue, 13 Aug 2024 02:17:31 GMT  
		Size: 2.7 MB (2709694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e744fc3f8c77bb11db8ae678f67ee7f5b83e02a4be0e5c38489b2454ec2dfadc`  
		Last Modified: Tue, 13 Aug 2024 02:17:30 GMT  
		Size: 8.5 KB (8490 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9-bullseye` - linux; arm variant v5

```console
$ docker pull hylang@sha256:3763e4c2c32467e4cf2a7a2d32730496e4f35dc02d686b26960ecbca4ef7a7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47195230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a1cfdef91c967e238f5720cf87a29b8207ef9ac72ed8428e541eceb6b1ad76`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:56b9d2d0e0360f64ade3cbe073b446e10c8e6bd253b761c16b5f319a8103d181 in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:5b04226d50f1c00a6c8950192ad70a2038016868ab6ffb162ad447e35e67a3cb`  
		Last Modified: Tue, 23 Jul 2024 00:02:06 GMT  
		Size: 28.9 MB (28930588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fa7b2cc0df7aa267d17dafdc3c404a5094c67516e27c7e80330909d603e393`  
		Last Modified: Tue, 23 Jul 2024 14:37:37 GMT  
		Size: 1.1 MB (1059693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83477c5b0cd3eb0ab37e3ba0f3d70e8129581e276146ca092c899d693552bd54`  
		Last Modified: Tue, 23 Jul 2024 15:41:11 GMT  
		Size: 10.8 MB (10782199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257325225470b493faa1668f74cadf8a40b9c511483df1f80a4404e7d8bf7669`  
		Last Modified: Tue, 23 Jul 2024 15:41:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d3e71eb392bbbe30498bd7ded9a8e5f7b4f2fd5dd4f9e5aa3007a4d13ef3c`  
		Last Modified: Thu, 01 Aug 2024 20:28:50 GMT  
		Size: 2.8 MB (2771323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848fc5a9716988b8dcab7df300ee754384434d8847dc3a04cb6499f027bf7c07`  
		Last Modified: Thu, 01 Aug 2024 22:34:45 GMT  
		Size: 3.7 MB (3651198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:38c703c297141057a6d267938c5b5891be6434df2c6957434080ca2e91a879dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44dbc09e909e9a527c77d8157dbf4521d589be23381e5d0d077ed964b8d20c98`

```dockerfile
```

-	Layers:
	-	`sha256:117b5725af77585e09a1d6be6f7c392ae1668ec375bd6062f103d1bbb20b89b6`  
		Last Modified: Thu, 01 Aug 2024 22:34:45 GMT  
		Size: 2.7 MB (2709936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0381a660d81c6bb62b576e6969156815cb9f0c3f0f015ed820bc6dfa9858aadc`  
		Last Modified: Thu, 01 Aug 2024 22:34:44 GMT  
		Size: 8.6 KB (8579 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:5c0c2c4438d2693e72928241dca1f3e5272f7d81e6729379a3d4575f1ebfcf7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44427747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7b946abb4be0a3e7f1c1e153af08ced97a191c3acbb4f54983972f1bd62d07`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c9d7c20d74535173edfbc4d8e362c0e63d98913c7ecf68fd8dc96f799adbf2`  
		Last Modified: Wed, 24 Jul 2024 09:25:30 GMT  
		Size: 1.0 MB (1041680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdd99d5c5a841388c70953ad12dcdde08a03ebc5fbeba4d7e14fe217d501b54`  
		Last Modified: Wed, 24 Jul 2024 12:43:53 GMT  
		Size: 10.4 MB (10374422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d838ef427ba482fb3df0450acb6ac4934d2d62d8ef8a89982779ab104768542`  
		Last Modified: Wed, 24 Jul 2024 12:43:52 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771615d90d5a1a2f9eaee17ae423d2d3ab7e98801494dc8b45bfc91c405e6df`  
		Last Modified: Thu, 01 Aug 2024 22:57:58 GMT  
		Size: 2.8 MB (2771204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f499227ca924c6a13f9883173b1b1935500580005ab47f7be0f7bff950dd871d`  
		Last Modified: Fri, 02 Aug 2024 02:28:45 GMT  
		Size: 3.7 MB (3651078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:f7f7ad134f291e46233012444feccbb10de64ab426eb5e6be402838e91d3494c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f344c7179331b35b112e6961eb2dc3aca7e34047002f57b0fb3d295993d69018`

```dockerfile
```

-	Layers:
	-	`sha256:f7107ac8bf6339adfa85c365f6147428dd9a1e55d6b24b63d6d1e378c97bfa6a`  
		Last Modified: Fri, 02 Aug 2024 02:28:45 GMT  
		Size: 2.7 MB (2711944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb24692cb47440ca80368b7dcfcda7f4725eda997d229614dfda99d6a15f92f`  
		Last Modified: Fri, 02 Aug 2024 02:28:44 GMT  
		Size: 8.6 KB (8579 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4706475acaeccb096e36c2fc872b1ab6330870f592b017791fcbf0a5787c550b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48664453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddce631000163bb2bf0c7541b5f996699bc2bdca9c139a7452f01468e4892d69`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc65893f013f219d9d96f98bf8b5fe07b132f85d9fd95cd71a02bb9b02fcf3f`  
		Last Modified: Thu, 01 Aug 2024 21:36:09 GMT  
		Size: 1.1 MB (1064121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65142bfa462789b88db1d31ffa243584084e792b4ffa2446d658ff3002cca1e`  
		Last Modified: Fri, 02 Aug 2024 03:01:55 GMT  
		Size: 11.1 MB (11101508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4811d1654708ba7bd213ef0415bc22856588c4391a42bf0203325d07425f7`  
		Last Modified: Fri, 02 Aug 2024 03:01:54 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149a42b790d923d1524f4122d4e23bce3a7355618bfae64efd7ced5ba2455c96`  
		Last Modified: Fri, 02 Aug 2024 03:01:55 GMT  
		Size: 2.8 MB (2771497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5e15adc3c8fed423acab7b332a4b107f72a6abb6d4af82e25f92788dbd035d`  
		Last Modified: Fri, 02 Aug 2024 05:56:37 GMT  
		Size: 3.7 MB (3651011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:e0c636ebc4cd622f5c5de4d5e26f7b19eeeecadcf7c0e9f1e02121b60227334e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef30f0fa6ceaf0416e85e5960b076b2592f17eb8c16b57fbf9804c8b7f50dea`

```dockerfile
```

-	Layers:
	-	`sha256:a2a3fd1ed8aeb05214c482b7645d4e2fce1e461c577b28ee44c907fd5e0d9838`  
		Last Modified: Fri, 02 Aug 2024 05:56:37 GMT  
		Size: 2.7 MB (2709954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f1176ada4c49c52d6f55394a70f01e96c339535fa8623323b0d65e31186cfa`  
		Last Modified: Fri, 02 Aug 2024 05:56:37 GMT  
		Size: 8.9 KB (8888 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:7b5453007399a1f9672596d5ca14867f936ba0bd251fc45ccfc17d18a252af22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51104172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e0733eacb4c03d3937a785116a867b24264ee431d965848bbd073bf4b88f38`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721fe40c3a7de02676cd9782c085a45429b60a7c81925b49a6ed19a3361cbc5`  
		Last Modified: Tue, 13 Aug 2024 01:16:42 GMT  
		Size: 1.1 MB (1088810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718912d5db4bb4dd0af8ce1a2560f6c25d2945a8a34eaff1e85ae473f355bcf9`  
		Last Modified: Tue, 13 Aug 2024 01:16:43 GMT  
		Size: 11.2 MB (11181300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474eb9734fb4d31722d83875d8a0c7a0501f8e8f797ff8eba53292221bb3f785`  
		Last Modified: Tue, 13 Aug 2024 01:16:42 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f714bb6e2e78be588411b0ea3b2e42d74dc4d20724cfbf2508eeb0c669a282`  
		Last Modified: Tue, 13 Aug 2024 01:16:42 GMT  
		Size: 2.8 MB (2772210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f439117219d4972fe1a6cb7c9e779ac613115d9cb244c05bad8c8d69238098b`  
		Last Modified: Tue, 13 Aug 2024 02:17:32 GMT  
		Size: 3.6 MB (3647836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:d01a3c7dc32a6d0689b8ccde715c095c5fc55fbf5f2f3ae2d5535b31c0d5288c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2715258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ff884d95913a03a3e3863086d98d2735066b58f258273f48592dcfe3ffedc9`

```dockerfile
```

-	Layers:
	-	`sha256:3b8b3b90d6cdacb657d69c69944a29535ccd57a1b100d8d00b35950b4f0b3870`  
		Last Modified: Tue, 13 Aug 2024 02:17:32 GMT  
		Size: 2.7 MB (2706800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3db36a0b4d3156c36c3aa69891a35be77bfec7288cc575684c69a2f32c9989f`  
		Last Modified: Tue, 13 Aug 2024 02:17:31 GMT  
		Size: 8.5 KB (8458 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9-bullseye` - linux; mips64le

```console
$ docker pull hylang@sha256:721c07deea2bc0c31f57a5b3e2d6fbaf3d1492ac1ba4b3116a625b2ef03155e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48132740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1530b5fcc12afbb49ab09f4c16d015091ae808a3f22d52d3d63a3a69c69e0a1a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:aa937b31fe693810c8c6e110de59ba07264dbc020fabac9e1ac045df57efc0c3 in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:83b27ea307774a387b0a5203cb6aa8f117e44bb5321ed6c8de8b0a0c43d895ca`  
		Last Modified: Tue, 23 Jul 2024 00:50:32 GMT  
		Size: 29.6 MB (29646085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8ecdbe7cf151b4b74007762e3654e1cd892dcd3eefc2a01de115531ec0fe2c`  
		Last Modified: Thu, 25 Jul 2024 09:12:37 GMT  
		Size: 1.1 MB (1050088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90002fe31fede79c3328a499bb875093c7178192241c67fa7f1255c9263b35c7`  
		Last Modified: Thu, 25 Jul 2024 09:12:38 GMT  
		Size: 11.0 MB (11012434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46c0474a9a8703a93afaa570a1f0ab2f92b01797f7359ae6b38a148f293f433`  
		Last Modified: Thu, 25 Jul 2024 09:12:37 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a288fe0b6f662287135aeba8b007c4a3040cf3db976206be4584aa573eec5596`  
		Last Modified: Thu, 01 Aug 2024 18:05:57 GMT  
		Size: 2.8 MB (2772339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc06c9ee7081fc103072cd46eff8e25299cd6b786e67565bba47138fb4064065`  
		Last Modified: Thu, 01 Aug 2024 19:01:08 GMT  
		Size: 3.7 MB (3651562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:a699ee1a17df3d578a92db1e01f83ea71d671ebe7ffdf023b79247fbcac5c9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 KB (8350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96fd479c9f68395bd657f7840c515f4779de9a81509a02b1318f37edfa90c18`

```dockerfile
```

-	Layers:
	-	`sha256:55af4da5bc27747aeaad13a41c287c539b841ec897ad335c58a5625d7f65bbcc`  
		Last Modified: Thu, 01 Aug 2024 19:01:07 GMT  
		Size: 8.3 KB (8350 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9-bullseye` - linux; ppc64le

```console
$ docker pull hylang@sha256:be6543690f122e7c4ea40fe83be261d5b7e6a451fc426fe47ec6a550c77c7e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54207070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df876b33f6bdac7c578829b028e34b5d610f6bc64a10cb3323c8694e8768f009`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31dd3dcf16603e1e8476609c6307f05981e92aa030f5bd37385095ebe836284d`  
		Last Modified: Wed, 24 Jul 2024 06:00:59 GMT  
		Size: 1.1 MB (1094915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a365bf0698f79f01ea6f7a7b8c3a904b3a54649383c544fa7c44730e7e2ef9`  
		Last Modified: Wed, 24 Jul 2024 09:26:03 GMT  
		Size: 11.4 MB (11383724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9623bbc013707362f72f4ab31d2d83b43dffad3dc84fdc318f365188e647ff`  
		Last Modified: Wed, 24 Jul 2024 09:26:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc539671cb67698711f23bf5036857a1968d1fe387b6fb99758aca6923d53ad2`  
		Last Modified: Thu, 01 Aug 2024 23:44:01 GMT  
		Size: 2.8 MB (2771966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395a2815e62d1b2a13b3b86f60440a48d7b90fbc6a410b476e563080889b4bfc`  
		Last Modified: Fri, 02 Aug 2024 02:07:49 GMT  
		Size: 3.7 MB (3651029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:75d7faab0426f9246861551e34acc6dbb25c574c05af13c018619d4f83b4f8d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e329d6bbe6c418320387ff75489491420a10ce5f8882a21983b777773a4cff`

```dockerfile
```

-	Layers:
	-	`sha256:b0ca6884b924f162c1760ceed4b4f4b05615c4c2672b1e8e31075fbb081161de`  
		Last Modified: Fri, 02 Aug 2024 02:07:49 GMT  
		Size: 2.7 MB (2714071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db0c29a9d0d5f3d0ec3c92538b5cf008a1b4991af0b533ccb0010a13e1bd708`  
		Last Modified: Fri, 02 Aug 2024 02:07:48 GMT  
		Size: 8.5 KB (8547 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.9-bullseye` - linux; s390x

```console
$ docker pull hylang@sha256:185db606b759398e085912a9095b082090cef4e255769df336bea3e8ad03adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48136589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149182c56a3381521634d784af085101dc1c41369096a2af8eed45378cb712e9`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jul 2024 23:46:02 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["bash"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jul 2024 23:46:02 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_VERSION=3.9.19
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Wed, 10 Jul 2024 23:46:02 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Wed, 10 Jul 2024 23:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
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
	-	`sha256:de4a305fc1af45cc7ae97020dfe639e8990f6d00b7e0ef222c4cdd720f0fc373`  
		Last Modified: Tue, 23 Jul 2024 02:33:12 GMT  
		Size: 29.7 MB (29669018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5738ba6e6f7a02dd4d7722b0d73b5e67886a4df0fabdfe571479b3dc12fefc1f`  
		Last Modified: Mon, 05 Aug 2024 00:35:46 GMT  
		Size: 1.1 MB (1075864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769d46566bb0fed459c99e769709f7d2ea70ca9d1a07c00dccea1987ee928739`  
		Last Modified: Mon, 05 Aug 2024 19:10:18 GMT  
		Size: 11.0 MB (10971353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087da4d0425f1dd8f5095e499ea3113903f7aff9c7da44305bb414f924d3ce53`  
		Last Modified: Mon, 05 Aug 2024 19:10:18 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1168835024d3ef7c8744cd2cc73e0d599a038959c6deb6f5d184a734b62262d8`  
		Last Modified: Mon, 05 Aug 2024 19:10:18 GMT  
		Size: 2.8 MB (2772365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4d1224bbadcbaddb7bbfe0748af1250827509b0c64c6b6e37e94ad279974bd`  
		Last Modified: Wed, 07 Aug 2024 00:21:17 GMT  
		Size: 3.6 MB (3647757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:8ae48d82ec5e733657f1174025464b51a077f5511c167cd03a911b1e18ac4eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d988bc401cfbc7424da10bb47d1ccd9ffc0d8f3d6fa298b713b78ab6261b52`

```dockerfile
```

-	Layers:
	-	`sha256:e65ffad3ee656d1d9546d77e1c2738061bc9d4b9b355365959ddd5182a56b80c`  
		Last Modified: Wed, 07 Aug 2024 00:21:17 GMT  
		Size: 2.7 MB (2709890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fd527795304fe4c30fe27f5a1e9c1cb6d9a3b29e3a4e28aac362deb2d0a174c`  
		Last Modified: Wed, 07 Aug 2024 00:21:17 GMT  
		Size: 8.5 KB (8502 bytes)  
		MIME: application/vnd.in-toto+json
