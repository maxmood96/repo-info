<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:9.2.9`](#swipl929)
-	[`swipl:9.3.22`](#swipl9322)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:9.2.9`

```console
$ docker pull swipl@sha256:dde77437b260188809bd474ee9ae2a31bab4fcccebd7a11376fbf9f4a3eabfce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.2.9` - linux; amd64

```console
$ docker pull swipl@sha256:c31c6897b9998d65fb3364666fe4711d4b1109883c1eaa71b68298e70080a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95966413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ddd85f7c1344d2f490feaff19d821b2c42e0cb2abd31c45e77d1711823ec08`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 02 Apr 2025 19:29:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 19:29:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 02 Apr 2025 19:29:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 02 Apr 2025 19:29:01 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04d2a6b26d0b6858ea0411289c1fcee8e33975dd4dfa657bc417179dd3b8818`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 49.2 MB (49209599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2dcd39a1bfac5c7fcb662cd6bf9e95e97356165485582d174609ac42b6e1ad`  
		Last Modified: Tue, 08 Apr 2025 01:36:23 GMT  
		Size: 18.5 MB (18529555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.9` - unknown; unknown

```console
$ docker pull swipl@sha256:cc619a1d42aff7fe1d3c37c6f05d1552dbbb634156f141c068d30c7344bf99de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61862ccbfafc68e19d2a8d4509d524a3e19a13461f01e4415857d763587e8fd`

```dockerfile
```

-	Layers:
	-	`sha256:132df1386726d0bb9f8c9d6dcbb115ec7d8ab0aac6ccc0b3f5e48448a9a5e504`  
		Last Modified: Tue, 08 Apr 2025 01:36:23 GMT  
		Size: 3.2 MB (3163444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4440f0130002e4c50d79b636358541f5376779bb1b95e85a784d573322a1be4`  
		Last Modified: Tue, 08 Apr 2025 01:36:23 GMT  
		Size: 17.5 KB (17507 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.9` - linux; arm variant v7

```console
$ docker pull swipl@sha256:9757eb645ea4e058f16f866f4e390678355722f3a4a3c6882b445f76d7ef64ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81788802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdef9fb7ab6a27c31a6d3e17044c3d4179be102063ed928451ca3df72d44c9a`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 02 Apr 2025 19:29:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 19:29:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 02 Apr 2025 19:29:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 02 Apr 2025 19:29:01 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be49c815f412a5892219def7cab7e51bf8a679928616f947f3d04d6abdfe9c4`  
		Last Modified: Tue, 08 Apr 2025 07:26:05 GMT  
		Size: 43.8 MB (43752159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc98f4bc3164d847d7e1a92e786f620b7e955ca521c2e7bba61c19c279d46e6f`  
		Last Modified: Tue, 08 Apr 2025 07:28:52 GMT  
		Size: 14.1 MB (14098776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.9` - unknown; unknown

```console
$ docker pull swipl@sha256:68aea1fb94603ba9cbcf732dc12ec95c3d19a105e7a8a2104fc51e2fe83c05cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce42f0326651c2e0a736dab09d8f1e33e27c889fc1f649c8c7d2221e9418707`

```dockerfile
```

-	Layers:
	-	`sha256:db96a5f997d5f4fb2c4dd99fddd9ca535d767b1a7c2c1615ba51949d711cddc4`  
		Last Modified: Tue, 08 Apr 2025 07:28:52 GMT  
		Size: 3.2 MB (3162290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba1c2712c32d7012bea36fc972aa80d8e4bc1bb8dc6431b399638f03cab76982`  
		Last Modified: Tue, 08 Apr 2025 07:28:52 GMT  
		Size: 17.6 KB (17580 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.9` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:d9c6e103913a3d5204336eda3b84bc13ccf311a4d5d79dca7ecc8920248de192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93736738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4613f9ba0239f7a2543c9c8b9495af54c0a12313bdd5a02d5ff1c053f3011601`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 02 Apr 2025 19:29:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 19:29:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 02 Apr 2025 19:29:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 02 Apr 2025 19:29:01 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef0d8dbeb045b2af1e3e38f75beb87a80d1e8c6bf494419caee988443e95f63`  
		Last Modified: Tue, 08 Apr 2025 05:48:44 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c74b6b0c4e91c5addb2a6eadeff2d7dafa1a21fc5c97f6706e583e129fa7b0`  
		Last Modified: Tue, 08 Apr 2025 05:55:06 GMT  
		Size: 17.9 MB (17939007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.9` - unknown; unknown

```console
$ docker pull swipl@sha256:5488c5639db2353ee225876cf70afdd3eac08e148e910f74266823acff85d1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3181386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc173c0a7680c2b19e0a31d08e144f5d61aad647067b3841c172d0029ecb5298`

```dockerfile
```

-	Layers:
	-	`sha256:0faca33e93d0084cd7887dfba3806746f1121dca640237e1a103fcce97c85115`  
		Last Modified: Tue, 08 Apr 2025 05:55:05 GMT  
		Size: 3.2 MB (3163784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51bf5f8a2de0f622c7c92942dd81f69983bab17ae13efd7673e7e93874059e39`  
		Last Modified: Tue, 08 Apr 2025 05:55:05 GMT  
		Size: 17.6 KB (17602 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:9.3.22`

```console
$ docker pull swipl@sha256:50482f7bfe0115d5820d33868a649644a1cbeb9fb60a9ff6059e3426efc13e9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.3.22` - linux; amd64

```console
$ docker pull swipl@sha256:e7e369a833a79993a58050e773295bec811586e2dd703a9358c5dafa8a6572f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96255592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a4b1a10feea90d272c89c47d23d1b7ab56ed9679cca971e930bd98119801fb`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 02 Apr 2025 19:29:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 19:29:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 02 Apr 2025 19:29:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 02 Apr 2025 19:29:01 GMT
RUN set -eux;     SWIPL_VER=9.3.22;     SWIPL_CHECKSUM=1b1bfee1ed6026c1eedfa9b03494ed1f03a02578d630b430e59742e196edd048;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1367c7197a7f335382611c08469b65f6d4a81911b5d579e906920f59798bb7`  
		Last Modified: Tue, 08 Apr 2025 01:36:12 GMT  
		Size: 49.2 MB (49209781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca44612709e8e96d2725169aa0ac84c7d344c40062434edb419e33b3775e36`  
		Last Modified: Tue, 08 Apr 2025 01:36:11 GMT  
		Size: 18.8 MB (18818552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.22` - unknown; unknown

```console
$ docker pull swipl@sha256:4ec9829c4a1eee49075a2c5fc0c48451121bd776e00d97e7d52458aecd56b034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066682e6800d56518f0df2ff2372a4c49e2aa4d4f2e0f45277173a8ec502317f`

```dockerfile
```

-	Layers:
	-	`sha256:81bbd1632b43c572a507d209c59d60861ff57ae2aa1e3f3b958a1477691e639c`  
		Last Modified: Tue, 08 Apr 2025 01:36:11 GMT  
		Size: 3.2 MB (3163448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:897bcd70c8609f45212ff2f7204f2d791d74ee7bf2da3d1cf8a1a4a8fdfa542e`  
		Last Modified: Tue, 08 Apr 2025 01:36:11 GMT  
		Size: 17.5 KB (17511 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.22` - linux; arm variant v7

```console
$ docker pull swipl@sha256:5f22eb49c2f53dfcf7e7ab4976986213e2eaf03b83b140eb2da1023a8138b9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82126163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d1c96b402b121aaeb2740f3939327378a7157b2eab5698c51bc40146dbe547`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 02 Apr 2025 19:29:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 19:29:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 02 Apr 2025 19:29:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 02 Apr 2025 19:29:01 GMT
RUN set -eux;     SWIPL_VER=9.3.22;     SWIPL_CHECKSUM=1b1bfee1ed6026c1eedfa9b03494ed1f03a02578d630b430e59742e196edd048;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be49c815f412a5892219def7cab7e51bf8a679928616f947f3d04d6abdfe9c4`  
		Last Modified: Tue, 08 Apr 2025 07:26:05 GMT  
		Size: 43.8 MB (43752159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ac37d230de99dd78bfa23eef86c089b3cdf2e0371c2ab7430b56ea12d48ee0`  
		Last Modified: Tue, 08 Apr 2025 07:26:05 GMT  
		Size: 14.4 MB (14436137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.22` - unknown; unknown

```console
$ docker pull swipl@sha256:663bf08f315004d31ce681363ab7e0d7832287d0eda315ba975983b96a2a337a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15858ba0118c64ae53da22528abddd7caae5bab07d45ca5e82e8ef3e3c3e3a17`

```dockerfile
```

-	Layers:
	-	`sha256:20dc1bfffc5f36db38b58d3daf5609bb8a0ead3f69c59abf5f42a66363b89c35`  
		Last Modified: Tue, 08 Apr 2025 07:26:04 GMT  
		Size: 3.2 MB (3162294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef5884bab244c69461a0a73ab285cea50664aa5123cead6359361b59c1484bb5`  
		Last Modified: Tue, 08 Apr 2025 07:26:04 GMT  
		Size: 17.6 KB (17584 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.22` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:806f6a15cb998576e487c98d5244fee06864e02019f5348a2784ef7d6c99ff6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94008139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1ab62f8171493ebee80a3aa21b3ba7b5c7d2501af14017e547d2d26ca603c4`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 02 Apr 2025 19:29:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 19:29:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 02 Apr 2025 19:29:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 02 Apr 2025 19:29:01 GMT
RUN set -eux;     SWIPL_VER=9.3.22;     SWIPL_CHECKSUM=1b1bfee1ed6026c1eedfa9b03494ed1f03a02578d630b430e59742e196edd048;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef0d8dbeb045b2af1e3e38f75beb87a80d1e8c6bf494419caee988443e95f63`  
		Last Modified: Tue, 08 Apr 2025 05:48:44 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703d330fbdf1f2c9d8aae5ff05bf366f5832f95d1824b0138e3a82827c2af93c`  
		Last Modified: Tue, 08 Apr 2025 05:48:43 GMT  
		Size: 18.2 MB (18210408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.22` - unknown; unknown

```console
$ docker pull swipl@sha256:58a3a852f34f9e89301473c17809d94755a69475040837786417b868d87edcf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3181393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e223c5ef9eae9235cabdaf3edceef0ffb44bfa2c0b41267120534aeca2bd68ba`

```dockerfile
```

-	Layers:
	-	`sha256:343694059ee9bc8679831e490820ba42ecb1e3c4dbdf98a80b26ae169ac9bad2`  
		Last Modified: Tue, 08 Apr 2025 05:48:42 GMT  
		Size: 3.2 MB (3163788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b11f2acfec948a75382ccaadf0d347e44e9ff84a8845f9b70adc95d557e5859`  
		Last Modified: Tue, 08 Apr 2025 05:48:42 GMT  
		Size: 17.6 KB (17605 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:latest`

```console
$ docker pull swipl@sha256:50482f7bfe0115d5820d33868a649644a1cbeb9fb60a9ff6059e3426efc13e9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:latest` - linux; amd64

```console
$ docker pull swipl@sha256:e7e369a833a79993a58050e773295bec811586e2dd703a9358c5dafa8a6572f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96255592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a4b1a10feea90d272c89c47d23d1b7ab56ed9679cca971e930bd98119801fb`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 02 Apr 2025 19:29:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 19:29:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 02 Apr 2025 19:29:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 02 Apr 2025 19:29:01 GMT
RUN set -eux;     SWIPL_VER=9.3.22;     SWIPL_CHECKSUM=1b1bfee1ed6026c1eedfa9b03494ed1f03a02578d630b430e59742e196edd048;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1367c7197a7f335382611c08469b65f6d4a81911b5d579e906920f59798bb7`  
		Last Modified: Tue, 08 Apr 2025 01:36:12 GMT  
		Size: 49.2 MB (49209781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca44612709e8e96d2725169aa0ac84c7d344c40062434edb419e33b3775e36`  
		Last Modified: Tue, 08 Apr 2025 01:36:11 GMT  
		Size: 18.8 MB (18818552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:4ec9829c4a1eee49075a2c5fc0c48451121bd776e00d97e7d52458aecd56b034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066682e6800d56518f0df2ff2372a4c49e2aa4d4f2e0f45277173a8ec502317f`

```dockerfile
```

-	Layers:
	-	`sha256:81bbd1632b43c572a507d209c59d60861ff57ae2aa1e3f3b958a1477691e639c`  
		Last Modified: Tue, 08 Apr 2025 01:36:11 GMT  
		Size: 3.2 MB (3163448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:897bcd70c8609f45212ff2f7204f2d791d74ee7bf2da3d1cf8a1a4a8fdfa542e`  
		Last Modified: Tue, 08 Apr 2025 01:36:11 GMT  
		Size: 17.5 KB (17511 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:5f22eb49c2f53dfcf7e7ab4976986213e2eaf03b83b140eb2da1023a8138b9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82126163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d1c96b402b121aaeb2740f3939327378a7157b2eab5698c51bc40146dbe547`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 02 Apr 2025 19:29:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 19:29:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 02 Apr 2025 19:29:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 02 Apr 2025 19:29:01 GMT
RUN set -eux;     SWIPL_VER=9.3.22;     SWIPL_CHECKSUM=1b1bfee1ed6026c1eedfa9b03494ed1f03a02578d630b430e59742e196edd048;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be49c815f412a5892219def7cab7e51bf8a679928616f947f3d04d6abdfe9c4`  
		Last Modified: Tue, 08 Apr 2025 07:26:05 GMT  
		Size: 43.8 MB (43752159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ac37d230de99dd78bfa23eef86c089b3cdf2e0371c2ab7430b56ea12d48ee0`  
		Last Modified: Tue, 08 Apr 2025 07:26:05 GMT  
		Size: 14.4 MB (14436137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:663bf08f315004d31ce681363ab7e0d7832287d0eda315ba975983b96a2a337a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15858ba0118c64ae53da22528abddd7caae5bab07d45ca5e82e8ef3e3c3e3a17`

```dockerfile
```

-	Layers:
	-	`sha256:20dc1bfffc5f36db38b58d3daf5609bb8a0ead3f69c59abf5f42a66363b89c35`  
		Last Modified: Tue, 08 Apr 2025 07:26:04 GMT  
		Size: 3.2 MB (3162294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef5884bab244c69461a0a73ab285cea50664aa5123cead6359361b59c1484bb5`  
		Last Modified: Tue, 08 Apr 2025 07:26:04 GMT  
		Size: 17.6 KB (17584 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:806f6a15cb998576e487c98d5244fee06864e02019f5348a2784ef7d6c99ff6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94008139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1ab62f8171493ebee80a3aa21b3ba7b5c7d2501af14017e547d2d26ca603c4`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 02 Apr 2025 19:29:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 19:29:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 02 Apr 2025 19:29:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 02 Apr 2025 19:29:01 GMT
RUN set -eux;     SWIPL_VER=9.3.22;     SWIPL_CHECKSUM=1b1bfee1ed6026c1eedfa9b03494ed1f03a02578d630b430e59742e196edd048;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef0d8dbeb045b2af1e3e38f75beb87a80d1e8c6bf494419caee988443e95f63`  
		Last Modified: Tue, 08 Apr 2025 05:48:44 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703d330fbdf1f2c9d8aae5ff05bf366f5832f95d1824b0138e3a82827c2af93c`  
		Last Modified: Tue, 08 Apr 2025 05:48:43 GMT  
		Size: 18.2 MB (18210408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:58a3a852f34f9e89301473c17809d94755a69475040837786417b868d87edcf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3181393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e223c5ef9eae9235cabdaf3edceef0ffb44bfa2c0b41267120534aeca2bd68ba`

```dockerfile
```

-	Layers:
	-	`sha256:343694059ee9bc8679831e490820ba42ecb1e3c4dbdf98a80b26ae169ac9bad2`  
		Last Modified: Tue, 08 Apr 2025 05:48:42 GMT  
		Size: 3.2 MB (3163788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b11f2acfec948a75382ccaadf0d347e44e9ff84a8845f9b70adc95d557e5859`  
		Last Modified: Tue, 08 Apr 2025 05:48:42 GMT  
		Size: 17.6 KB (17605 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:stable`

```console
$ docker pull swipl@sha256:dde77437b260188809bd474ee9ae2a31bab4fcccebd7a11376fbf9f4a3eabfce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:stable` - linux; amd64

```console
$ docker pull swipl@sha256:c31c6897b9998d65fb3364666fe4711d4b1109883c1eaa71b68298e70080a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95966413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ddd85f7c1344d2f490feaff19d821b2c42e0cb2abd31c45e77d1711823ec08`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 02 Apr 2025 19:29:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 19:29:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 02 Apr 2025 19:29:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 02 Apr 2025 19:29:01 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04d2a6b26d0b6858ea0411289c1fcee8e33975dd4dfa657bc417179dd3b8818`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 49.2 MB (49209599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2dcd39a1bfac5c7fcb662cd6bf9e95e97356165485582d174609ac42b6e1ad`  
		Last Modified: Tue, 08 Apr 2025 01:36:23 GMT  
		Size: 18.5 MB (18529555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:cc619a1d42aff7fe1d3c37c6f05d1552dbbb634156f141c068d30c7344bf99de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61862ccbfafc68e19d2a8d4509d524a3e19a13461f01e4415857d763587e8fd`

```dockerfile
```

-	Layers:
	-	`sha256:132df1386726d0bb9f8c9d6dcbb115ec7d8ab0aac6ccc0b3f5e48448a9a5e504`  
		Last Modified: Tue, 08 Apr 2025 01:36:23 GMT  
		Size: 3.2 MB (3163444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4440f0130002e4c50d79b636358541f5376779bb1b95e85a784d573322a1be4`  
		Last Modified: Tue, 08 Apr 2025 01:36:23 GMT  
		Size: 17.5 KB (17507 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:9757eb645ea4e058f16f866f4e390678355722f3a4a3c6882b445f76d7ef64ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81788802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdef9fb7ab6a27c31a6d3e17044c3d4179be102063ed928451ca3df72d44c9a`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 02 Apr 2025 19:29:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 19:29:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 02 Apr 2025 19:29:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 02 Apr 2025 19:29:01 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be49c815f412a5892219def7cab7e51bf8a679928616f947f3d04d6abdfe9c4`  
		Last Modified: Tue, 08 Apr 2025 07:26:05 GMT  
		Size: 43.8 MB (43752159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc98f4bc3164d847d7e1a92e786f620b7e955ca521c2e7bba61c19c279d46e6f`  
		Last Modified: Tue, 08 Apr 2025 07:28:52 GMT  
		Size: 14.1 MB (14098776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:68aea1fb94603ba9cbcf732dc12ec95c3d19a105e7a8a2104fc51e2fe83c05cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce42f0326651c2e0a736dab09d8f1e33e27c889fc1f649c8c7d2221e9418707`

```dockerfile
```

-	Layers:
	-	`sha256:db96a5f997d5f4fb2c4dd99fddd9ca535d767b1a7c2c1615ba51949d711cddc4`  
		Last Modified: Tue, 08 Apr 2025 07:28:52 GMT  
		Size: 3.2 MB (3162290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba1c2712c32d7012bea36fc972aa80d8e4bc1bb8dc6431b399638f03cab76982`  
		Last Modified: Tue, 08 Apr 2025 07:28:52 GMT  
		Size: 17.6 KB (17580 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:d9c6e103913a3d5204336eda3b84bc13ccf311a4d5d79dca7ecc8920248de192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93736738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4613f9ba0239f7a2543c9c8b9495af54c0a12313bdd5a02d5ff1c053f3011601`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 02 Apr 2025 19:29:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 19:29:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 02 Apr 2025 19:29:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 02 Apr 2025 19:29:01 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 02 Apr 2025 19:29:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef0d8dbeb045b2af1e3e38f75beb87a80d1e8c6bf494419caee988443e95f63`  
		Last Modified: Tue, 08 Apr 2025 05:48:44 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c74b6b0c4e91c5addb2a6eadeff2d7dafa1a21fc5c97f6706e583e129fa7b0`  
		Last Modified: Tue, 08 Apr 2025 05:55:06 GMT  
		Size: 17.9 MB (17939007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:5488c5639db2353ee225876cf70afdd3eac08e148e910f74266823acff85d1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3181386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc173c0a7680c2b19e0a31d08e144f5d61aad647067b3841c172d0029ecb5298`

```dockerfile
```

-	Layers:
	-	`sha256:0faca33e93d0084cd7887dfba3806746f1121dca640237e1a103fcce97c85115`  
		Last Modified: Tue, 08 Apr 2025 05:55:05 GMT  
		Size: 3.2 MB (3163784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51bf5f8a2de0f622c7c92942dd81f69983bab17ae13efd7673e7e93874059e39`  
		Last Modified: Tue, 08 Apr 2025 05:55:05 GMT  
		Size: 17.6 KB (17602 bytes)  
		MIME: application/vnd.in-toto+json
