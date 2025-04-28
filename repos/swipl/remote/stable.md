## `swipl:stable`

```console
$ docker pull swipl@sha256:d21b563ac55b232356cda21235a33fdeebbcbeb3944be8309edc56d8d26c0e53
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
$ docker pull swipl@sha256:94aed66d9f791f9b8f37879c400cd106c83920375950e4245160d7f0d5e388de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95967295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca577621844d729aa0061528b0472c5d41e0772056e398fe2ffc0d4db2fd2cd`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 18 Apr 2025 09:02:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Fri, 18 Apr 2025 09:02:20 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 18 Apr 2025 09:02:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 09:02:20 GMT
ENV LANG=C.UTF-8
# Fri, 18 Apr 2025 09:02:20 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 18 Apr 2025 09:02:20 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ca2f6f2dd000d1f774fd7c5043f8eb2eefba4403c45628ce3381fcd46b7b17`  
		Last Modified: Mon, 28 Apr 2025 22:07:24 GMT  
		Size: 49.2 MB (49209690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c18a176745ea767c84876cd3196f10dcf23174755671e951166fb57cfe56dec`  
		Last Modified: Mon, 28 Apr 2025 22:07:24 GMT  
		Size: 18.5 MB (18529963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:9080531bd402a63827c3909f46a54d7d765500d3040bb1dd2bcf489c9a9e38b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c27ac96d9e2c3aa0c89978a54942752e676542c4979a145d3c809a4e2c9bc`

```dockerfile
```

-	Layers:
	-	`sha256:8b16e77e942af553fab25c061c9a17f94ae1dab400776b33399bcaf688127b32`  
		Last Modified: Mon, 28 Apr 2025 22:07:23 GMT  
		Size: 3.2 MB (3163444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1988a2c581c28ae500ca246555e8b420cf826931ed2e57c91f2340e8926e8318`  
		Last Modified: Mon, 28 Apr 2025 22:07:23 GMT  
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
