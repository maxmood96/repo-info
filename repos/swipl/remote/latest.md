## `swipl:latest`

```console
$ docker pull swipl@sha256:9acd19606ee66734f457a751cfe7593d8ddd1932c29c031f7ea70e753ab62853
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
$ docker pull swipl@sha256:e888d0bdce29b574e38369ddb18d470ad70017ac48482b029951b5f7039cb4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98090493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67033a9f722b734b261eca5447c10f18dcd3c556ebe3077891506b52f2a7f0f8`
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
RUN set -eux;     SWIPL_VER=9.3.23;     SWIPL_CHECKSUM=754a35f3abf4cdfbbe9625973d2baacc55d4375a41a8c8bf505fd451b206e59e;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 18 Apr 2025 09:02:20 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e10c5bcd9c16b053f0d91c9cd30ef40a438025256e5b311e1b1eb363669ca3d`  
		Last Modified: Mon, 28 Apr 2025 22:07:25 GMT  
		Size: 49.2 MB (49209682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8204bd08274d48ea464103c197fe59b472a9e725dc8f86a1885aaac4ba8f5974`  
		Last Modified: Mon, 28 Apr 2025 22:07:25 GMT  
		Size: 20.7 MB (20653169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:df8ee6c2f4c08d21b99c2b0ae0f78f8727a1b83985635cdf75e6fdf712d5fcb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d70cd18f11fca473f0daf6e0fa3dec29ae658e4931e7ac3dd6d7db3bc047b9`

```dockerfile
```

-	Layers:
	-	`sha256:abf22938e63d033c82b8b0e3e138e9e00e5002713d5cd757cf0b55da0a9ce6f0`  
		Last Modified: Mon, 28 Apr 2025 22:07:24 GMT  
		Size: 3.2 MB (3163448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87edb65af893131ffac383eb70ecd103f69e620b3b252d231a2833626aee0156`  
		Last Modified: Mon, 28 Apr 2025 22:07:24 GMT  
		Size: 17.5 KB (17511 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:7a36caca584db2ac44954518f01f67f62a6e0073bafabcb86f5f3a86c2d1e36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86066156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f927f532e0a161a11dbf70e98f16054c1f83bc307bed487c1cce2e58ec1e11fb`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Fri, 18 Apr 2025 09:02:20 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 18 Apr 2025 09:02:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 09:02:20 GMT
ENV LANG=C.UTF-8
# Fri, 18 Apr 2025 09:02:20 GMT
RUN set -eux;     SWIPL_VER=9.3.23;     SWIPL_CHECKSUM=754a35f3abf4cdfbbe9625973d2baacc55d4375a41a8c8bf505fd451b206e59e;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 18 Apr 2025 09:02:20 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099c6ffa6d4611ab077ff10578ac98798fa5df3b31912564556ddb57654ae30a`  
		Last Modified: Fri, 18 Apr 2025 18:11:56 GMT  
		Size: 43.8 MB (43751714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc9fec1016ca603d83aaabf157823ab250a8dae0f7c910ccab2b963aad0539c`  
		Last Modified: Fri, 18 Apr 2025 18:11:55 GMT  
		Size: 18.4 MB (18376575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:0921d30b9ae9de6af56f92b903dfc21b92573002f563f9b2a2ad1cf4321d4676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7814ed2e4a214e8fb0568e5fc5c96b77fec2cf043ad94af398955b7e1a981e3a`

```dockerfile
```

-	Layers:
	-	`sha256:e96065a28239a59c354a90c8c530b01056c54296cab34acd98b1d821d8a8f5e5`  
		Last Modified: Fri, 18 Apr 2025 18:11:55 GMT  
		Size: 3.2 MB (3162294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f032ed0758457e2630109d63730128e3869757a4542aa0f586ddd63b3ce2d3ec`  
		Last Modified: Fri, 18 Apr 2025 18:11:55 GMT  
		Size: 17.6 KB (17584 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:0612b468d0c84d7992f0844abd7c513cc1a60f403a37239d83f000a0566ab0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95835531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba860b0e9b451617edda27fbd23f4126e8b2dd985cd9991a48f9391232f28906`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 18 Apr 2025 09:02:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Fri, 18 Apr 2025 09:02:20 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 18 Apr 2025 09:02:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 09:02:20 GMT
ENV LANG=C.UTF-8
# Fri, 18 Apr 2025 09:02:20 GMT
RUN set -eux;     SWIPL_VER=9.3.23;     SWIPL_CHECKSUM=754a35f3abf4cdfbbe9625973d2baacc55d4375a41a8c8bf505fd451b206e59e;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 18 Apr 2025 09:02:20 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca5f37e2576990cca711971efc9f32d1d10aa0df685391668834a6a3afef40b`  
		Last Modified: Tue, 29 Apr 2025 01:32:51 GMT  
		Size: 47.7 MB (47731538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53a8895f034acc71346f4851e9d805d99ddf4b623949ae0a52df0b74702e4ce`  
		Last Modified: Tue, 29 Apr 2025 01:32:50 GMT  
		Size: 20.0 MB (20037371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:1cc75cad1401546c24ff923ee46a68304c0bb1dfb62a64fccbe68fee7f9ef80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3181393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65205a90c387e2fc9060af2ec2aaa21c2368ced6bee0808cb17caf2a4080afb`

```dockerfile
```

-	Layers:
	-	`sha256:72415f2304ea2426f96b6a8f54ee56019c008dd8f71b40ead727e44294777470`  
		Last Modified: Tue, 29 Apr 2025 01:32:50 GMT  
		Size: 3.2 MB (3163788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:085d6e98e63c13c4b5d592ecbd98f1b09b381f6d1ca194586f752778510b9637`  
		Last Modified: Tue, 29 Apr 2025 01:32:49 GMT  
		Size: 17.6 KB (17605 bytes)  
		MIME: application/vnd.in-toto+json
