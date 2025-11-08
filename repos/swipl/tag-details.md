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
		Last Modified: Fri, 07 Nov 2025 21:19:11 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4604c33fb79f648ed98d14e249cc8bdce50627cbbc0d44c3c20af29ef6c177`  
		Last Modified: Sat, 08 Nov 2025 09:42:57 GMT  
		Size: 49.2 MB (49226327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6195631d5e167da985651681e2e4958d9ece4a6508fddab985fab2ceed41bdd`  
		Last Modified: Sat, 08 Nov 2025 09:42:54 GMT  
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
		Last Modified: Mon, 08 Sep 2025 21:37:00 GMT  
		Size: 3.3 MB (3326532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b714355986373660e91e493c8f52ad3c51098e8071cbd7c1483ebbd9724ea8`  
		Last Modified: Mon, 08 Sep 2025 21:37:00 GMT  
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

```console
$ docker pull swipl@sha256:493adc80d23ca3cadfff65f515b7d0734bf6e92aa042a8fcb429e9efbf182585
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.3.34` - linux; amd64

```console
$ docker pull swipl@sha256:d4bef50935475c5faa537b7695b48d72167fbc90cc26922a8364536868301cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98623385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7fe1981873a7820aeccb6ff0cb2cf30ce51bd38ac7a13b2410cccd35613581`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 20:10:53 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 05 Nov 2025 20:10:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 20:10:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 20:17:03 GMT
RUN set -eux;     SWIPL_VER=9.3.34;     SWIPL_CHECKSUM=89d7c860dcf1261f0a4ae990faaa038168225fe11708252a9d09d45aac8ab583;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 05 Nov 2025 20:17:03 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bb27ab38377413b3c6158bbc91a1dd2b32c751e8c588b246826f89f273588f`  
		Last Modified: Wed, 05 Nov 2025 20:17:30 GMT  
		Size: 49.2 MB (49228909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5c9872959e8ac97f0906d131bc4fad4c58779b66cab5e226fea32cb5efa92f`  
		Last Modified: Wed, 05 Nov 2025 20:17:27 GMT  
		Size: 21.2 MB (21165909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.34` - unknown; unknown

```console
$ docker pull swipl@sha256:70739b78cdf0d7a39945a9ee214c2afc991ce521336ec03c4fb2ee9490abff94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92702cfbedccdeb40e5076af5b521cf819839c3067001c58f813adb2583a02cc`

```dockerfile
```

-	Layers:
	-	`sha256:57b2e058be342c2dca6e136e031958c218e1cd7fc7b5ceadc448f93c4212027b`  
		Last Modified: Wed, 05 Nov 2025 21:12:20 GMT  
		Size: 3.3 MB (3326536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cad5cdf95aa4d45c6bd2b2706bde7c53c76d1cab0c82d0e236e43b9f0423e22e`  
		Last Modified: Wed, 05 Nov 2025 21:12:22 GMT  
		Size: 17.9 KB (17884 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.34` - linux; arm variant v7

```console
$ docker pull swipl@sha256:d847caf3ff7ce092b128c0286c10518530252a7f788cbd8693a0251367da21eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84411114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ed0520236ba3722650752da0c45968c1d8bc43a97d9c6f2b4358b5af632ab9`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 20:11:50 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 05 Nov 2025 20:11:50 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 20:11:50 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 20:14:26 GMT
RUN set -eux;     SWIPL_VER=9.3.34;     SWIPL_CHECKSUM=89d7c860dcf1261f0a4ae990faaa038168225fe11708252a9d09d45aac8ab583;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 05 Nov 2025 20:14:26 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c8a51f1cf002dcf2247bb366e672fce722072b9ccfbc481f458117c1571fa7`  
		Last Modified: Wed, 05 Nov 2025 20:14:50 GMT  
		Size: 43.8 MB (43767798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a02e430ae61b9a707cdbaf434c6778c83864171d25600dc9709414d084eb3d`  
		Last Modified: Wed, 05 Nov 2025 20:14:47 GMT  
		Size: 16.7 MB (16709190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.34` - unknown; unknown

```console
$ docker pull swipl@sha256:b60c867399862f8a2a71fedbeea744431b10cf161a38c3f16eef3699f35dfb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e007c1e96e6d1e7b97f30ec4bc6c1c223f2a36eece249fc752c0e0cca4a383`

```dockerfile
```

-	Layers:
	-	`sha256:6f3febabf0c3c8da5c8706e536049539d664a9adf156f432709e58a798d1defa`  
		Last Modified: Wed, 05 Nov 2025 21:12:26 GMT  
		Size: 3.3 MB (3325382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cc103844211e606667b492a01c71c9faba9046a917723e74f94358f5034540`  
		Last Modified: Wed, 05 Nov 2025 21:12:27 GMT  
		Size: 18.0 KB (17962 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.34` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:fcf3defbc4952fefe0fe202c7610b104fc719f37e689960a08ed2692f225937c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96440422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec72fefd2589b480ca736eb89c12b6601bca34224d47d23e6294736a74379c2e`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 20:11:39 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 05 Nov 2025 20:11:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 20:11:39 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 20:17:57 GMT
RUN set -eux;     SWIPL_VER=9.3.34;     SWIPL_CHECKSUM=89d7c860dcf1261f0a4ae990faaa038168225fe11708252a9d09d45aac8ab583;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 05 Nov 2025 20:17:57 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd1311cdf1d9a5a1d3d5d79a0617e5cb04693114bcc03afc00fcd674c41bbb9`  
		Last Modified: Wed, 05 Nov 2025 20:18:20 GMT  
		Size: 47.8 MB (47807927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf447a7ed698c4d756c8a575e5d5a7878dc1aa0784b2fa4b6e76c2aecad53e`  
		Last Modified: Wed, 05 Nov 2025 20:18:19 GMT  
		Size: 20.5 MB (20530119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.34` - unknown; unknown

```console
$ docker pull swipl@sha256:59726b91905547be1d6615a50f0118723c10c21b233bcab51e9a77f5be1439c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1abb65b2cfcc23b45b59563b326ceaf105575978644d0c2dbae49964b89a36`

```dockerfile
```

-	Layers:
	-	`sha256:1dbe6e9fcabe79c72367c2edf4e17f574e6c1605d8a4f7696d7edbc2fa75fb7a`  
		Last Modified: Wed, 05 Nov 2025 21:12:32 GMT  
		Size: 3.3 MB (3326876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33706212c18fd77d629949ec5c7bd3b647c459c5c45476e72a842d11f56055b1`  
		Last Modified: Wed, 05 Nov 2025 21:12:33 GMT  
		Size: 18.0 KB (17980 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:latest`

```console
$ docker pull swipl@sha256:493adc80d23ca3cadfff65f515b7d0734bf6e92aa042a8fcb429e9efbf182585
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
$ docker pull swipl@sha256:d4bef50935475c5faa537b7695b48d72167fbc90cc26922a8364536868301cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98623385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7fe1981873a7820aeccb6ff0cb2cf30ce51bd38ac7a13b2410cccd35613581`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 20:10:53 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 05 Nov 2025 20:10:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 20:10:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 20:17:03 GMT
RUN set -eux;     SWIPL_VER=9.3.34;     SWIPL_CHECKSUM=89d7c860dcf1261f0a4ae990faaa038168225fe11708252a9d09d45aac8ab583;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 05 Nov 2025 20:17:03 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bb27ab38377413b3c6158bbc91a1dd2b32c751e8c588b246826f89f273588f`  
		Last Modified: Wed, 05 Nov 2025 20:17:30 GMT  
		Size: 49.2 MB (49228909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5c9872959e8ac97f0906d131bc4fad4c58779b66cab5e226fea32cb5efa92f`  
		Last Modified: Wed, 05 Nov 2025 20:17:27 GMT  
		Size: 21.2 MB (21165909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:70739b78cdf0d7a39945a9ee214c2afc991ce521336ec03c4fb2ee9490abff94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92702cfbedccdeb40e5076af5b521cf819839c3067001c58f813adb2583a02cc`

```dockerfile
```

-	Layers:
	-	`sha256:57b2e058be342c2dca6e136e031958c218e1cd7fc7b5ceadc448f93c4212027b`  
		Last Modified: Wed, 05 Nov 2025 21:12:20 GMT  
		Size: 3.3 MB (3326536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cad5cdf95aa4d45c6bd2b2706bde7c53c76d1cab0c82d0e236e43b9f0423e22e`  
		Last Modified: Wed, 05 Nov 2025 21:12:22 GMT  
		Size: 17.9 KB (17884 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:d847caf3ff7ce092b128c0286c10518530252a7f788cbd8693a0251367da21eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84411114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ed0520236ba3722650752da0c45968c1d8bc43a97d9c6f2b4358b5af632ab9`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 20:11:50 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 05 Nov 2025 20:11:50 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 20:11:50 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 20:14:26 GMT
RUN set -eux;     SWIPL_VER=9.3.34;     SWIPL_CHECKSUM=89d7c860dcf1261f0a4ae990faaa038168225fe11708252a9d09d45aac8ab583;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 05 Nov 2025 20:14:26 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c8a51f1cf002dcf2247bb366e672fce722072b9ccfbc481f458117c1571fa7`  
		Last Modified: Wed, 05 Nov 2025 20:14:50 GMT  
		Size: 43.8 MB (43767798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a02e430ae61b9a707cdbaf434c6778c83864171d25600dc9709414d084eb3d`  
		Last Modified: Wed, 05 Nov 2025 20:14:47 GMT  
		Size: 16.7 MB (16709190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:b60c867399862f8a2a71fedbeea744431b10cf161a38c3f16eef3699f35dfb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e007c1e96e6d1e7b97f30ec4bc6c1c223f2a36eece249fc752c0e0cca4a383`

```dockerfile
```

-	Layers:
	-	`sha256:6f3febabf0c3c8da5c8706e536049539d664a9adf156f432709e58a798d1defa`  
		Last Modified: Wed, 05 Nov 2025 21:12:26 GMT  
		Size: 3.3 MB (3325382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cc103844211e606667b492a01c71c9faba9046a917723e74f94358f5034540`  
		Last Modified: Wed, 05 Nov 2025 21:12:27 GMT  
		Size: 18.0 KB (17962 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:fcf3defbc4952fefe0fe202c7610b104fc719f37e689960a08ed2692f225937c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96440422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec72fefd2589b480ca736eb89c12b6601bca34224d47d23e6294736a74379c2e`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 20:11:39 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 05 Nov 2025 20:11:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 20:11:39 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 20:17:57 GMT
RUN set -eux;     SWIPL_VER=9.3.34;     SWIPL_CHECKSUM=89d7c860dcf1261f0a4ae990faaa038168225fe11708252a9d09d45aac8ab583;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 05 Nov 2025 20:17:57 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd1311cdf1d9a5a1d3d5d79a0617e5cb04693114bcc03afc00fcd674c41bbb9`  
		Last Modified: Wed, 05 Nov 2025 20:18:20 GMT  
		Size: 47.8 MB (47807927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf447a7ed698c4d756c8a575e5d5a7878dc1aa0784b2fa4b6e76c2aecad53e`  
		Last Modified: Wed, 05 Nov 2025 20:18:19 GMT  
		Size: 20.5 MB (20530119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:59726b91905547be1d6615a50f0118723c10c21b233bcab51e9a77f5be1439c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1abb65b2cfcc23b45b59563b326ceaf105575978644d0c2dbae49964b89a36`

```dockerfile
```

-	Layers:
	-	`sha256:1dbe6e9fcabe79c72367c2edf4e17f574e6c1605d8a4f7696d7edbc2fa75fb7a`  
		Last Modified: Wed, 05 Nov 2025 21:12:32 GMT  
		Size: 3.3 MB (3326876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33706212c18fd77d629949ec5c7bd3b647c459c5c45476e72a842d11f56055b1`  
		Last Modified: Wed, 05 Nov 2025 21:12:33 GMT  
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
		Last Modified: Fri, 07 Nov 2025 21:19:11 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4604c33fb79f648ed98d14e249cc8bdce50627cbbc0d44c3c20af29ef6c177`  
		Last Modified: Sat, 08 Nov 2025 09:42:57 GMT  
		Size: 49.2 MB (49226327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6195631d5e167da985651681e2e4958d9ece4a6508fddab985fab2ceed41bdd`  
		Last Modified: Sat, 08 Nov 2025 09:42:54 GMT  
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
		Last Modified: Mon, 08 Sep 2025 21:37:00 GMT  
		Size: 3.3 MB (3326532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b714355986373660e91e493c8f52ad3c51098e8071cbd7c1483ebbd9724ea8`  
		Last Modified: Mon, 08 Sep 2025 21:37:00 GMT  
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
