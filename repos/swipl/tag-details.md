<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:9.2.9`](#swipl929)
-	[`swipl:9.3.34`](#swipl9334)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:9.2.9`

```console
$ docker pull swipl@sha256:3cc45ca98b5a362fe1eec2bdf3358b1222751e5645145957fe4e17acbf0bc6df
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
$ docker pull swipl@sha256:0f42569dfc68ecf064685f96ea448f4c1df3db02024aa3b8e6dd46dbc7db80de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95986182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b53e0894dbc4ddbd6e969267cf1f78abef4efd7e22dc352c574603dfaa94c8`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 01 Sep 2025 15:19:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 01 Sep 2025 15:19:10 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Mon, 01 Sep 2025 15:19:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 15:19:10 GMT
ENV LANG=C.UTF-8
# Mon, 01 Sep 2025 15:19:10 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Mon, 01 Sep 2025 15:19:10 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4604c33fb79f648ed98d14e249cc8bdce50627cbbc0d44c3c20af29ef6c177`  
		Last Modified: Mon, 08 Sep 2025 22:36:48 GMT  
		Size: 49.2 MB (49226327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6195631d5e167da985651681e2e4958d9ece4a6508fddab985fab2ceed41bdd`  
		Last Modified: Mon, 08 Sep 2025 22:36:53 GMT  
		Size: 18.5 MB (18531509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.9` - unknown; unknown

```console
$ docker pull swipl@sha256:334f145209f33ae2ee082846380a3658b6a25eb34ee1f53d05371264b596f122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d1d93482e750ffcd88b4d6ebdb5419c329d7cbb249a90b03a69a0be03c101b`

```dockerfile
```

-	Layers:
	-	`sha256:49653a17ef3d217b5a627514398ce14c480befdab0464214e400b6491fbc7d9c`  
		Last Modified: Mon, 08 Sep 2025 23:12:33 GMT  
		Size: 3.3 MB (3326532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b714355986373660e91e493c8f52ad3c51098e8071cbd7c1483ebbd9724ea8`  
		Last Modified: Mon, 08 Sep 2025 23:12:34 GMT  
		Size: 17.5 KB (17507 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.9` - linux; arm variant v7

```console
$ docker pull swipl@sha256:878593af2b4e794af89d6b35299d33e226c2dd7c00a5ab0fb89e0f9b25dabeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81801172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0b081eaf9b21134bed6b416832b986cd4ae5eb243591c41e43d11a048bd53d`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:36:00 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 04 Nov 2025 00:36:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:36:00 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:38:04 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 04 Nov 2025 00:38:04 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d86c04fd1143f83ffb7dad114a54477d0091f3a2a4760a0bdc7f79e8e42bcf9`  
		Last Modified: Tue, 04 Nov 2025 00:38:33 GMT  
		Size: 43.8 MB (43767869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507fd9e0de51a56b22c23ac04381f9fa703dc7fe95207591e21fc9d4046ded0a`  
		Last Modified: Tue, 04 Nov 2025 00:38:28 GMT  
		Size: 14.1 MB (14099177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.9` - unknown; unknown

```console
$ docker pull swipl@sha256:10486b9f5e447bac7756dd55c596f0d55456f03c6e22a67e28a26372c85ee633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3342919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0258d18ecda14819b32b8cde14fd665c6f68b22fc12b6d89a98de809d0f2b0c`

```dockerfile
```

-	Layers:
	-	`sha256:26199b395310bf628953bd07a6114ff3b679b9c61093bde7b7231073dcd77353`  
		Last Modified: Tue, 04 Nov 2025 12:12:26 GMT  
		Size: 3.3 MB (3325378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604331f940dfd5a926754d47aeb5925293bbfcc3f05421c6cc9bb3761c998f56`  
		Last Modified: Tue, 04 Nov 2025 12:12:27 GMT  
		Size: 17.5 KB (17541 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.9` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:fffc77833703f80038050a3a4f9792b36eeb786ccf78ab54627f009856d97728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93850165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7cb40fa6dcc2034a1b03951fd8eabe85f88f362fc2f4152632d7d96f07c910e`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:29:25 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 04 Nov 2025 00:29:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:25 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:35:00 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 04 Nov 2025 00:35:00 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c21a4ef8384e23e0d5a64c6b27b6d008216434e25b727916c51bb38d74b2577`  
		Last Modified: Tue, 04 Nov 2025 00:35:31 GMT  
		Size: 47.8 MB (47808067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641f2b9c36e67de857746e9a70a32c2ef9069af7d00662e25caaf3bb2e905e37`  
		Last Modified: Tue, 04 Nov 2025 00:35:29 GMT  
		Size: 17.9 MB (17939722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.9` - unknown; unknown

```console
$ docker pull swipl@sha256:2db2125bb0130f95bcd8c57309689e7af1601cfbe47b47f9c9e78fe9abab1160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fafcecc6a3122e1e42647ed9333d2b02fe647d4ae896e37a7207599f290a1e`

```dockerfile
```

-	Layers:
	-	`sha256:2b169eb9b33ab8354d69864d0c84fce7018e311ee052f251edb433df91087291`  
		Last Modified: Tue, 04 Nov 2025 12:12:30 GMT  
		Size: 3.3 MB (3326872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f66169d6295913b8b63425d035fefc7bcc92411ccec78bd4caa9ded2402b3f8`  
		Last Modified: Tue, 04 Nov 2025 12:12:31 GMT  
		Size: 17.6 KB (17559 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:9.3.34`

**does not exist** (yet?)

## `swipl:latest`

```console
$ docker pull swipl@sha256:f744a102ee3ded4493c993b619ec76895873ff2b1a0ec196a525cb6cb0fdaf8c
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
$ docker pull swipl@sha256:ebf9d16a4bef7e5a156dd05def58c0757613a390320bd9a4b57ec247921d80d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98605381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab0b088e44e253b008181e42954c2acccf42b040b46c508f268e4bd210535ff`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:23 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 04 Nov 2025 00:27:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:27:23 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:33:18 GMT
RUN set -eux;     SWIPL_VER=9.3.33;     SWIPL_CHECKSUM=706dbfa7b8a38cdf771720bb3e6071c61e5dc6f2013e2cfea7e9f255212f3aff;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 04 Nov 2025 00:33:18 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9957ef8f75dd6e2cf746e97ede49faa5849cfa728bbfa33ea400afd633ac723`  
		Last Modified: Tue, 04 Nov 2025 00:33:43 GMT  
		Size: 49.2 MB (49228837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9991853325bbbef54e98b9b0f6d1d019c37739bf567ee25a81c0d3bfaf69e68b`  
		Last Modified: Tue, 04 Nov 2025 00:33:39 GMT  
		Size: 21.1 MB (21147977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:f52494bf847d4f3531f2e22f1502fda1dac62324016e6f02e0ae25688e425c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a12c66101e7ace31be7a53a92df305f0c181525e1acb16fd549349fc8b2d83`

```dockerfile
```

-	Layers:
	-	`sha256:ef00dff279907955dc4313a7f1a913c7a346603926c210d092ee94c4b96be50c`  
		Last Modified: Tue, 04 Nov 2025 09:12:17 GMT  
		Size: 3.3 MB (3326536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f0728eaebefa7117091a689885c0777e9ff9776bee9231ea9b90601578f6a13`  
		Last Modified: Tue, 04 Nov 2025 09:12:18 GMT  
		Size: 17.9 KB (17885 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:46e5948c48fa6ed4826d5b587348d047ee2e471d7b3c69d89a1b8840f0ef4472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84407181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56aadf719dba5b159d8b45079562c23e9efada8485b7699173fb225064ebe51f`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:45 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 04 Nov 2025 00:35:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:35:45 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:38:17 GMT
RUN set -eux;     SWIPL_VER=9.3.33;     SWIPL_CHECKSUM=706dbfa7b8a38cdf771720bb3e6071c61e5dc6f2013e2cfea7e9f255212f3aff;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 04 Nov 2025 00:38:17 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9764e64895d975dc5ab2fc47fa89548c3ba9c4321c848ef71741a66d065b4a39`  
		Last Modified: Tue, 04 Nov 2025 00:38:40 GMT  
		Size: 43.8 MB (43767767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2764528472782cfd73b161c4d22ade31650ec1a4ae857cc50c130cff17a9786e`  
		Last Modified: Tue, 04 Nov 2025 00:38:37 GMT  
		Size: 16.7 MB (16705288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:60e581ce1620df9c499e40c93332132aeaf9cd5d52116d822455984eebdcd0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc84225ee0149b06b6cc0cb7e790c1635b4d3692743d5d555b1be41f04013454`

```dockerfile
```

-	Layers:
	-	`sha256:daddc033b48a32fb0767571c9de30b22a25d0e7e97ea4d5e030a5ff1628642c3`  
		Last Modified: Tue, 04 Nov 2025 12:12:32 GMT  
		Size: 3.3 MB (3325382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8f156134d6c77ae7ea0359caf1eb593974e3ceb52e9e1e879d660acbd6c532`  
		Last Modified: Tue, 04 Nov 2025 12:12:32 GMT  
		Size: 18.0 KB (17962 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:ef1732eaca40bdbdca4de3414614c44880b8380682a3dc5b77615d7266a70bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96439743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59ac98908fc2c98dfcc0e366329ef37e4b8263d28e7a69355bb685390faef66`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:29:22 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 04 Nov 2025 00:29:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:22 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:35:12 GMT
RUN set -eux;     SWIPL_VER=9.3.33;     SWIPL_CHECKSUM=706dbfa7b8a38cdf771720bb3e6071c61e5dc6f2013e2cfea7e9f255212f3aff;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 04 Nov 2025 00:35:12 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53ec909832272d0c57d32a543ab5a5d9a504abe8ebc1458b1ae650aea5bd943`  
		Last Modified: Tue, 04 Nov 2025 00:35:38 GMT  
		Size: 47.8 MB (47807939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2903d366e0895176eb981853dd9353e29856b3a2a69eb6601a3eb86f3e9c3399`  
		Last Modified: Tue, 04 Nov 2025 00:35:36 GMT  
		Size: 20.5 MB (20529428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:d4bf2c837d1972a86471e3fbf4c496aee74719230f2100d7e78be32f523c70a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bf46d8d468f75b919665fcc61271238cac96fb7745c95ae685bb3ab25dd53f`

```dockerfile
```

-	Layers:
	-	`sha256:1433fcfa710f485536a65d0d9fb249818f6f7d7369457523be2919134701ebf8`  
		Last Modified: Tue, 04 Nov 2025 12:12:36 GMT  
		Size: 3.3 MB (3326876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e311bca66b25625f1ff5ed54799d6fe7774e1a250ff7b0306aa002b5e5b87916`  
		Last Modified: Tue, 04 Nov 2025 12:12:37 GMT  
		Size: 18.0 KB (17980 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:stable`

```console
$ docker pull swipl@sha256:3cc45ca98b5a362fe1eec2bdf3358b1222751e5645145957fe4e17acbf0bc6df
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
$ docker pull swipl@sha256:0f42569dfc68ecf064685f96ea448f4c1df3db02024aa3b8e6dd46dbc7db80de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95986182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b53e0894dbc4ddbd6e969267cf1f78abef4efd7e22dc352c574603dfaa94c8`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 01 Sep 2025 15:19:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 01 Sep 2025 15:19:10 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Mon, 01 Sep 2025 15:19:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 15:19:10 GMT
ENV LANG=C.UTF-8
# Mon, 01 Sep 2025 15:19:10 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Mon, 01 Sep 2025 15:19:10 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4604c33fb79f648ed98d14e249cc8bdce50627cbbc0d44c3c20af29ef6c177`  
		Last Modified: Mon, 08 Sep 2025 22:36:48 GMT  
		Size: 49.2 MB (49226327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6195631d5e167da985651681e2e4958d9ece4a6508fddab985fab2ceed41bdd`  
		Last Modified: Mon, 08 Sep 2025 22:36:53 GMT  
		Size: 18.5 MB (18531509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:334f145209f33ae2ee082846380a3658b6a25eb34ee1f53d05371264b596f122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d1d93482e750ffcd88b4d6ebdb5419c329d7cbb249a90b03a69a0be03c101b`

```dockerfile
```

-	Layers:
	-	`sha256:49653a17ef3d217b5a627514398ce14c480befdab0464214e400b6491fbc7d9c`  
		Last Modified: Mon, 08 Sep 2025 23:12:33 GMT  
		Size: 3.3 MB (3326532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b714355986373660e91e493c8f52ad3c51098e8071cbd7c1483ebbd9724ea8`  
		Last Modified: Mon, 08 Sep 2025 23:12:34 GMT  
		Size: 17.5 KB (17507 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:878593af2b4e794af89d6b35299d33e226c2dd7c00a5ab0fb89e0f9b25dabeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81801172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0b081eaf9b21134bed6b416832b986cd4ae5eb243591c41e43d11a048bd53d`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:36:00 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 04 Nov 2025 00:36:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:36:00 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:38:04 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 04 Nov 2025 00:38:04 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d86c04fd1143f83ffb7dad114a54477d0091f3a2a4760a0bdc7f79e8e42bcf9`  
		Last Modified: Tue, 04 Nov 2025 00:38:33 GMT  
		Size: 43.8 MB (43767869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507fd9e0de51a56b22c23ac04381f9fa703dc7fe95207591e21fc9d4046ded0a`  
		Last Modified: Tue, 04 Nov 2025 00:38:28 GMT  
		Size: 14.1 MB (14099177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:10486b9f5e447bac7756dd55c596f0d55456f03c6e22a67e28a26372c85ee633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3342919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0258d18ecda14819b32b8cde14fd665c6f68b22fc12b6d89a98de809d0f2b0c`

```dockerfile
```

-	Layers:
	-	`sha256:26199b395310bf628953bd07a6114ff3b679b9c61093bde7b7231073dcd77353`  
		Last Modified: Tue, 04 Nov 2025 12:12:26 GMT  
		Size: 3.3 MB (3325378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604331f940dfd5a926754d47aeb5925293bbfcc3f05421c6cc9bb3761c998f56`  
		Last Modified: Tue, 04 Nov 2025 12:12:27 GMT  
		Size: 17.5 KB (17541 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:fffc77833703f80038050a3a4f9792b36eeb786ccf78ab54627f009856d97728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93850165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7cb40fa6dcc2034a1b03951fd8eabe85f88f362fc2f4152632d7d96f07c910e`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:29:25 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 04 Nov 2025 00:29:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:25 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:35:00 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 04 Nov 2025 00:35:00 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c21a4ef8384e23e0d5a64c6b27b6d008216434e25b727916c51bb38d74b2577`  
		Last Modified: Tue, 04 Nov 2025 00:35:31 GMT  
		Size: 47.8 MB (47808067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641f2b9c36e67de857746e9a70a32c2ef9069af7d00662e25caaf3bb2e905e37`  
		Last Modified: Tue, 04 Nov 2025 00:35:29 GMT  
		Size: 17.9 MB (17939722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:2db2125bb0130f95bcd8c57309689e7af1601cfbe47b47f9c9e78fe9abab1160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fafcecc6a3122e1e42647ed9333d2b02fe647d4ae896e37a7207599f290a1e`

```dockerfile
```

-	Layers:
	-	`sha256:2b169eb9b33ab8354d69864d0c84fce7018e311ee052f251edb433df91087291`  
		Last Modified: Tue, 04 Nov 2025 12:12:30 GMT  
		Size: 3.3 MB (3326872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f66169d6295913b8b63425d035fefc7bcc92411ccec78bd4caa9ded2402b3f8`  
		Last Modified: Tue, 04 Nov 2025 12:12:31 GMT  
		Size: 17.6 KB (17559 bytes)  
		MIME: application/vnd.in-toto+json
