<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:9.2.3`](#swipl923)
-	[`swipl:9.3.2`](#swipl932)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:9.2.3`

```console
$ docker pull swipl@sha256:8bfe511362d9cd039f466533a64e27c01919ee27844746923de994b1cb6c950d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.2.3` - linux; amd64

```console
$ docker pull swipl@sha256:570c7c3f3d2a6a8074e724ccd4e781b856d1765b802ac7230915363ab4a1f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96497791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1c4c7dea502bf322598e71ce57246efe05557727b16a7d4fbce787d261fd32`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 10:22:13 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 05 Apr 2024 10:22:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 10:22:13 GMT
RUN set -eux;     SWIPL_VER=9.2.3;     SWIPL_CHECKSUM=28329039526a93c10a160be5c7d90ca4fb7d1514e4a009a0852c6d237292e724;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439936bd2b2f872e9d221e1b897b623aeb7febeb9a3f67222c127e7bd30cd495`  
		Last Modified: Wed, 10 Apr 2024 03:10:16 GMT  
		Size: 49.2 MB (49202808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371204baf27b4b0b46eed4de086bc60b9953479d87e65df1b425f7dc8e0b91fc`  
		Last Modified: Wed, 10 Apr 2024 03:10:16 GMT  
		Size: 18.2 MB (18163625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.3` - unknown; unknown

```console
$ docker pull swipl@sha256:cef11bd5592077c9a3eea06e6534583380dacadafdaba0ab7fdceb6e47307642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877fc570bdba202647a5aa71d7d4060514519d7a1a2f9c0a59ec6ca60c3e469e`

```dockerfile
```

-	Layers:
	-	`sha256:6de5219eff56fe8dd8ef8f1dfcf572c9e193cdd1718ba1c84ae8b546ddae19bb`  
		Last Modified: Wed, 10 Apr 2024 03:10:16 GMT  
		Size: 3.1 MB (3111386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3f2397c16b4f8bd3853c3d9668307ad698966ba083a0c461d3c95e871e3b38`  
		Last Modified: Wed, 10 Apr 2024 03:10:16 GMT  
		Size: 17.3 KB (17267 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.3` - linux; arm variant v7

```console
$ docker pull swipl@sha256:0b2c065667aab4d0379adb37e27c6a3131b1ebff22af7f40f4b09512446fb822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82860182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad4a0eb72b76b7fc8041a90b7df39f300ebc5a8054795a27dc2f73470251382`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 10:22:13 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 05 Apr 2024 10:22:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 10:22:13 GMT
RUN set -eux;     SWIPL_VER=9.2.3;     SWIPL_CHECKSUM=28329039526a93c10a160be5c7d90ca4fb7d1514e4a009a0852c6d237292e724;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069b0c4e66aa57d8686e36cd7c6bd4409c5906569781c606f2d057bfb8279a36`  
		Last Modified: Thu, 11 Apr 2024 11:28:13 GMT  
		Size: 43.7 MB (43697272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7decc40cbf18bd1c28e60643f80e9ee344ab2f0390651816f21daf19d1285a92`  
		Last Modified: Thu, 11 Apr 2024 11:48:59 GMT  
		Size: 14.4 MB (14439987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.3` - unknown; unknown

```console
$ docker pull swipl@sha256:1f1f0cc9012a42f79382632577fd05a163e8c54f75ec720ba3af394465e1ae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d1a7081d6176b3190d7d8b9109e69f27abedecf8de5a9bdc5bec179d94250f`

```dockerfile
```

-	Layers:
	-	`sha256:05e733c9dba0ea10b31df8dcce7bb2bc89a392e3e275230987644c34417eabee`  
		Last Modified: Thu, 11 Apr 2024 11:48:58 GMT  
		Size: 3.1 MB (3113908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86119015b5e741834932fd5a10b74e20b81be85dd1cebeb158f1b42215ae0c7a`  
		Last Modified: Thu, 11 Apr 2024 11:48:58 GMT  
		Size: 17.2 KB (17167 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.3` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:c5a830a032b239f2d4fc2ddbbc7c22ade5342736cc97528c460fd25e028ce002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94461172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c72f47828c5fe4df334ca183ad1ac89fbc8f94527de50ee3c8c3bb83466e7e7`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 10:22:13 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 05 Apr 2024 10:22:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 10:22:13 GMT
RUN set -eux;     SWIPL_VER=9.2.3;     SWIPL_CHECKSUM=28329039526a93c10a160be5c7d90ca4fb7d1514e4a009a0852c6d237292e724;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b217c9897e3a1bf7af6efd2a876e6a97f753ffee0fd570eb9a6ff4d74098b384`  
		Last Modified: Wed, 10 Apr 2024 21:28:06 GMT  
		Size: 47.7 MB (47676154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e296334c3c6a0cc99fb42dbc8d28b6481286243d17ed95e3cb32dde010aaf9`  
		Last Modified: Wed, 10 Apr 2024 21:34:56 GMT  
		Size: 17.6 MB (17622861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.3` - unknown; unknown

```console
$ docker pull swipl@sha256:6e391bb1ba33ed7eecf647bf34f2005c7da070fcf4d6c511dc13c92579804a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6b1c278a2801e3706bef7992f9ecce3985e2eda303d8beca9e715ee6f927c9`

```dockerfile
```

-	Layers:
	-	`sha256:38410f1926e6592a4ddc4379051c3792df05d3d4cee6a19560cfee0a01a6fb12`  
		Last Modified: Wed, 10 Apr 2024 21:34:54 GMT  
		Size: 3.1 MB (3111699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2e488a65a35756b25d6ffe994cd4c1786936caf7f7b0f4bad683340b9c4eec4`  
		Last Modified: Wed, 10 Apr 2024 21:34:54 GMT  
		Size: 17.1 KB (17106 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:9.3.2`

```console
$ docker pull swipl@sha256:2b6a9e857d9fdaecded1e204bfa316f51c2b00d5a978421d74ba1254b1cbb6e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.3.2` - linux; amd64

```console
$ docker pull swipl@sha256:979ea669dc1820172dfb2cea50dfe7f054047742197f68d58aa1a57217876bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96474048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2db3a83dc25921db4e649ebfb92e25f73c14245ae0274f4f7abdb85d0088274`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 10:22:13 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 05 Apr 2024 10:22:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 10:22:13 GMT
RUN set -eux;     SWIPL_VER=9.3.2;     SWIPL_CHECKSUM=c329123b4f63aa8d1566f4097af58412588d4e7ad16a5fd743f97b4be6733410;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63732d325952fb00884eceed85517cb0adb9abb31640c9f82bb90d95184e8b76`  
		Last Modified: Wed, 10 Apr 2024 03:07:22 GMT  
		Size: 49.2 MB (49202898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a86dd40cfceedfae7e8e13dc4960b06465a831dd90708c60f822b93ffb8df2`  
		Last Modified: Wed, 10 Apr 2024 03:07:21 GMT  
		Size: 18.1 MB (18139792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.2` - unknown; unknown

```console
$ docker pull swipl@sha256:d92d89c401aade808c7419ba5a942cdb14b2d94b0247647ec4ffd6df9e480080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f6ee41364dc9409ff9f82a4f155bcd90d3819b1cf7abddd8a5d5fa98d835d8`

```dockerfile
```

-	Layers:
	-	`sha256:8a02b692bf69d72b6d3297a19d37fc758294bcd72bb407c971784c2035c7765a`  
		Last Modified: Wed, 10 Apr 2024 03:07:21 GMT  
		Size: 3.1 MB (3111386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5d1bd4ec8763e67ac2657aa0457d9216ac7b40827fcc7d2031be3f3e1f59af3`  
		Last Modified: Wed, 10 Apr 2024 03:07:21 GMT  
		Size: 17.3 KB (17266 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.2` - linux; arm variant v7

```console
$ docker pull swipl@sha256:5cd2ceb6b2171273812b2a9382b1d735cc4a0781decffbce39beb13dbc3d7b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82846868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15671573adde6bce7ccad4221a9927796af4e968782519456d3507c1a82b6306`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 10:22:13 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 05 Apr 2024 10:22:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 10:22:13 GMT
RUN set -eux;     SWIPL_VER=9.3.2;     SWIPL_CHECKSUM=c329123b4f63aa8d1566f4097af58412588d4e7ad16a5fd743f97b4be6733410;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069b0c4e66aa57d8686e36cd7c6bd4409c5906569781c606f2d057bfb8279a36`  
		Last Modified: Thu, 11 Apr 2024 11:28:13 GMT  
		Size: 43.7 MB (43697272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126064763732b3047fccd5ff3646e4d5dbf51b5227fd1c21ecaecb54400c0a60`  
		Last Modified: Thu, 11 Apr 2024 11:28:13 GMT  
		Size: 14.4 MB (14426673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.2` - unknown; unknown

```console
$ docker pull swipl@sha256:0347134a076f20abc60dc102f5fcbdd280d7176a2259ac33b53928f7f241c25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227115eb329a960a550057d144ed01a38605dbe0693e42828b28fe9c883d3f48`

```dockerfile
```

-	Layers:
	-	`sha256:a167c028489e05092d0397952995fcf8895f32969dd351760e7474440978c23b`  
		Last Modified: Thu, 11 Apr 2024 11:28:12 GMT  
		Size: 3.1 MB (3113908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a9251782542e3c3c8c41f0becf0df1f3a2f1748af93d640b61ab4aa4dc1bc9`  
		Last Modified: Thu, 11 Apr 2024 11:28:12 GMT  
		Size: 17.2 KB (17166 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.2` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:6b48ed154d8d382475dec478c813e246b3b4e66f913a4cc63f892e38273bdfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94438354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47e9580ea9a55144ac4e9769216058cdc81c1452e1081e740f4f473c49fdd8d`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 10:22:13 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 05 Apr 2024 10:22:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 10:22:13 GMT
RUN set -eux;     SWIPL_VER=9.3.2;     SWIPL_CHECKSUM=c329123b4f63aa8d1566f4097af58412588d4e7ad16a5fd743f97b4be6733410;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b217c9897e3a1bf7af6efd2a876e6a97f753ffee0fd570eb9a6ff4d74098b384`  
		Last Modified: Wed, 10 Apr 2024 21:28:06 GMT  
		Size: 47.7 MB (47676154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0f208dc2f1b7239a8904edce407d940647d69536f89e066697e5e837b2951f`  
		Last Modified: Wed, 10 Apr 2024 21:28:05 GMT  
		Size: 17.6 MB (17600043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.2` - unknown; unknown

```console
$ docker pull swipl@sha256:4907a027897c59d76f58412ccb8ee5e9cdef252714d7f5af39ff55172dba9adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2b66680328a47f6d2392b4fde2603c329369de0932dd083a563f8647a7c00d`

```dockerfile
```

-	Layers:
	-	`sha256:db056c65536d6020b960be67058a7d17865098ca789bcdb3308a5817aca4b5b9`  
		Last Modified: Wed, 10 Apr 2024 21:28:04 GMT  
		Size: 3.1 MB (3111699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a6c4d21c1360e0ca67570dd89ec888e631efc798049989a0eb334cd400ebde1`  
		Last Modified: Wed, 10 Apr 2024 21:28:04 GMT  
		Size: 17.1 KB (17105 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:latest`

```console
$ docker pull swipl@sha256:2b6a9e857d9fdaecded1e204bfa316f51c2b00d5a978421d74ba1254b1cbb6e0
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
$ docker pull swipl@sha256:979ea669dc1820172dfb2cea50dfe7f054047742197f68d58aa1a57217876bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96474048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2db3a83dc25921db4e649ebfb92e25f73c14245ae0274f4f7abdb85d0088274`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 10:22:13 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 05 Apr 2024 10:22:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 10:22:13 GMT
RUN set -eux;     SWIPL_VER=9.3.2;     SWIPL_CHECKSUM=c329123b4f63aa8d1566f4097af58412588d4e7ad16a5fd743f97b4be6733410;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63732d325952fb00884eceed85517cb0adb9abb31640c9f82bb90d95184e8b76`  
		Last Modified: Wed, 10 Apr 2024 03:07:22 GMT  
		Size: 49.2 MB (49202898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a86dd40cfceedfae7e8e13dc4960b06465a831dd90708c60f822b93ffb8df2`  
		Last Modified: Wed, 10 Apr 2024 03:07:21 GMT  
		Size: 18.1 MB (18139792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:d92d89c401aade808c7419ba5a942cdb14b2d94b0247647ec4ffd6df9e480080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f6ee41364dc9409ff9f82a4f155bcd90d3819b1cf7abddd8a5d5fa98d835d8`

```dockerfile
```

-	Layers:
	-	`sha256:8a02b692bf69d72b6d3297a19d37fc758294bcd72bb407c971784c2035c7765a`  
		Last Modified: Wed, 10 Apr 2024 03:07:21 GMT  
		Size: 3.1 MB (3111386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5d1bd4ec8763e67ac2657aa0457d9216ac7b40827fcc7d2031be3f3e1f59af3`  
		Last Modified: Wed, 10 Apr 2024 03:07:21 GMT  
		Size: 17.3 KB (17266 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:5cd2ceb6b2171273812b2a9382b1d735cc4a0781decffbce39beb13dbc3d7b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82846868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15671573adde6bce7ccad4221a9927796af4e968782519456d3507c1a82b6306`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 10:22:13 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 05 Apr 2024 10:22:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 10:22:13 GMT
RUN set -eux;     SWIPL_VER=9.3.2;     SWIPL_CHECKSUM=c329123b4f63aa8d1566f4097af58412588d4e7ad16a5fd743f97b4be6733410;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069b0c4e66aa57d8686e36cd7c6bd4409c5906569781c606f2d057bfb8279a36`  
		Last Modified: Thu, 11 Apr 2024 11:28:13 GMT  
		Size: 43.7 MB (43697272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126064763732b3047fccd5ff3646e4d5dbf51b5227fd1c21ecaecb54400c0a60`  
		Last Modified: Thu, 11 Apr 2024 11:28:13 GMT  
		Size: 14.4 MB (14426673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:0347134a076f20abc60dc102f5fcbdd280d7176a2259ac33b53928f7f241c25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227115eb329a960a550057d144ed01a38605dbe0693e42828b28fe9c883d3f48`

```dockerfile
```

-	Layers:
	-	`sha256:a167c028489e05092d0397952995fcf8895f32969dd351760e7474440978c23b`  
		Last Modified: Thu, 11 Apr 2024 11:28:12 GMT  
		Size: 3.1 MB (3113908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a9251782542e3c3c8c41f0becf0df1f3a2f1748af93d640b61ab4aa4dc1bc9`  
		Last Modified: Thu, 11 Apr 2024 11:28:12 GMT  
		Size: 17.2 KB (17166 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:6b48ed154d8d382475dec478c813e246b3b4e66f913a4cc63f892e38273bdfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94438354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47e9580ea9a55144ac4e9769216058cdc81c1452e1081e740f4f473c49fdd8d`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 10:22:13 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 05 Apr 2024 10:22:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 10:22:13 GMT
RUN set -eux;     SWIPL_VER=9.3.2;     SWIPL_CHECKSUM=c329123b4f63aa8d1566f4097af58412588d4e7ad16a5fd743f97b4be6733410;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b217c9897e3a1bf7af6efd2a876e6a97f753ffee0fd570eb9a6ff4d74098b384`  
		Last Modified: Wed, 10 Apr 2024 21:28:06 GMT  
		Size: 47.7 MB (47676154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0f208dc2f1b7239a8904edce407d940647d69536f89e066697e5e837b2951f`  
		Last Modified: Wed, 10 Apr 2024 21:28:05 GMT  
		Size: 17.6 MB (17600043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:4907a027897c59d76f58412ccb8ee5e9cdef252714d7f5af39ff55172dba9adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2b66680328a47f6d2392b4fde2603c329369de0932dd083a563f8647a7c00d`

```dockerfile
```

-	Layers:
	-	`sha256:db056c65536d6020b960be67058a7d17865098ca789bcdb3308a5817aca4b5b9`  
		Last Modified: Wed, 10 Apr 2024 21:28:04 GMT  
		Size: 3.1 MB (3111699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a6c4d21c1360e0ca67570dd89ec888e631efc798049989a0eb334cd400ebde1`  
		Last Modified: Wed, 10 Apr 2024 21:28:04 GMT  
		Size: 17.1 KB (17105 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:stable`

```console
$ docker pull swipl@sha256:8bfe511362d9cd039f466533a64e27c01919ee27844746923de994b1cb6c950d
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
$ docker pull swipl@sha256:570c7c3f3d2a6a8074e724ccd4e781b856d1765b802ac7230915363ab4a1f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96497791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1c4c7dea502bf322598e71ce57246efe05557727b16a7d4fbce787d261fd32`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 10:22:13 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 05 Apr 2024 10:22:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 10:22:13 GMT
RUN set -eux;     SWIPL_VER=9.2.3;     SWIPL_CHECKSUM=28329039526a93c10a160be5c7d90ca4fb7d1514e4a009a0852c6d237292e724;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439936bd2b2f872e9d221e1b897b623aeb7febeb9a3f67222c127e7bd30cd495`  
		Last Modified: Wed, 10 Apr 2024 03:10:16 GMT  
		Size: 49.2 MB (49202808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371204baf27b4b0b46eed4de086bc60b9953479d87e65df1b425f7dc8e0b91fc`  
		Last Modified: Wed, 10 Apr 2024 03:10:16 GMT  
		Size: 18.2 MB (18163625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:cef11bd5592077c9a3eea06e6534583380dacadafdaba0ab7fdceb6e47307642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877fc570bdba202647a5aa71d7d4060514519d7a1a2f9c0a59ec6ca60c3e469e`

```dockerfile
```

-	Layers:
	-	`sha256:6de5219eff56fe8dd8ef8f1dfcf572c9e193cdd1718ba1c84ae8b546ddae19bb`  
		Last Modified: Wed, 10 Apr 2024 03:10:16 GMT  
		Size: 3.1 MB (3111386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3f2397c16b4f8bd3853c3d9668307ad698966ba083a0c461d3c95e871e3b38`  
		Last Modified: Wed, 10 Apr 2024 03:10:16 GMT  
		Size: 17.3 KB (17267 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:0b2c065667aab4d0379adb37e27c6a3131b1ebff22af7f40f4b09512446fb822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82860182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad4a0eb72b76b7fc8041a90b7df39f300ebc5a8054795a27dc2f73470251382`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 10:22:13 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 05 Apr 2024 10:22:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 10:22:13 GMT
RUN set -eux;     SWIPL_VER=9.2.3;     SWIPL_CHECKSUM=28329039526a93c10a160be5c7d90ca4fb7d1514e4a009a0852c6d237292e724;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069b0c4e66aa57d8686e36cd7c6bd4409c5906569781c606f2d057bfb8279a36`  
		Last Modified: Thu, 11 Apr 2024 11:28:13 GMT  
		Size: 43.7 MB (43697272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7decc40cbf18bd1c28e60643f80e9ee344ab2f0390651816f21daf19d1285a92`  
		Last Modified: Thu, 11 Apr 2024 11:48:59 GMT  
		Size: 14.4 MB (14439987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:1f1f0cc9012a42f79382632577fd05a163e8c54f75ec720ba3af394465e1ae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d1a7081d6176b3190d7d8b9109e69f27abedecf8de5a9bdc5bec179d94250f`

```dockerfile
```

-	Layers:
	-	`sha256:05e733c9dba0ea10b31df8dcce7bb2bc89a392e3e275230987644c34417eabee`  
		Last Modified: Thu, 11 Apr 2024 11:48:58 GMT  
		Size: 3.1 MB (3113908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86119015b5e741834932fd5a10b74e20b81be85dd1cebeb158f1b42215ae0c7a`  
		Last Modified: Thu, 11 Apr 2024 11:48:58 GMT  
		Size: 17.2 KB (17167 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:c5a830a032b239f2d4fc2ddbbc7c22ade5342736cc97528c460fd25e028ce002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94461172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c72f47828c5fe4df334ca183ad1ac89fbc8f94527de50ee3c8c3bb83466e7e7`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 10:22:13 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 05 Apr 2024 10:22:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 10:22:13 GMT
RUN set -eux;     SWIPL_VER=9.2.3;     SWIPL_CHECKSUM=28329039526a93c10a160be5c7d90ca4fb7d1514e4a009a0852c6d237292e724;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 05 Apr 2024 10:22:13 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b217c9897e3a1bf7af6efd2a876e6a97f753ffee0fd570eb9a6ff4d74098b384`  
		Last Modified: Wed, 10 Apr 2024 21:28:06 GMT  
		Size: 47.7 MB (47676154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e296334c3c6a0cc99fb42dbc8d28b6481286243d17ed95e3cb32dde010aaf9`  
		Last Modified: Wed, 10 Apr 2024 21:34:56 GMT  
		Size: 17.6 MB (17622861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:6e391bb1ba33ed7eecf647bf34f2005c7da070fcf4d6c511dc13c92579804a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6b1c278a2801e3706bef7992f9ecce3985e2eda303d8beca9e715ee6f927c9`

```dockerfile
```

-	Layers:
	-	`sha256:38410f1926e6592a4ddc4379051c3792df05d3d4cee6a19560cfee0a01a6fb12`  
		Last Modified: Wed, 10 Apr 2024 21:34:54 GMT  
		Size: 3.1 MB (3111699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2e488a65a35756b25d6ffe994cd4c1786936caf7f7b0f4bad683340b9c4eec4`  
		Last Modified: Wed, 10 Apr 2024 21:34:54 GMT  
		Size: 17.1 KB (17106 bytes)  
		MIME: application/vnd.in-toto+json
