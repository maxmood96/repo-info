<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:9.2.4`](#swipl924)
-	[`swipl:9.3.6`](#swipl936)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:9.2.4`

```console
$ docker pull swipl@sha256:b1c25241b12060ce5cdff3ae6a77275280a3909cebb3ad2c1a99fa451d612d74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.2.4` - linux; amd64

```console
$ docker pull swipl@sha256:6444c9b3c5694b2408a9a92ab245eb20ae99dcc0f38cfde28c6f653d99e1034f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96520643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a39a31ecff2b317a357e5918343f7fd54b29c4a2c4c45e3f52f9453f0bdeef2`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 26 Apr 2024 16:13:38 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Fri, 26 Apr 2024 16:13:38 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 16:13:38 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 26 Apr 2024 16:13:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
ENV LANG=C.UTF-8
# Fri, 26 Apr 2024 16:13:38 GMT
RUN set -eux;     SWIPL_VER=9.2.4;     SWIPL_CHECKSUM=d53cc13380b60ec4edeea0caead26af4d0e6bd877f458cf4fc6d6f90bd6e987c;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51df949ce4ea429c4a5bef71872cd262035dd773889fc179b61cafc0110e7ff7`  
		Last Modified: Tue, 14 May 2024 03:08:51 GMT  
		Size: 49.2 MB (49207399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fbc908e2a28e9a24341fc7228d9ef2283b06988a1fc9c161c52b3561baa46c`  
		Last Modified: Tue, 14 May 2024 03:08:51 GMT  
		Size: 18.2 MB (18162833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.4` - unknown; unknown

```console
$ docker pull swipl@sha256:67c0a23df8a008493462041e25484eb58f2df8d77d98d690fc733b773d99d808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b201355c8f43edc9f72b2e95ffb0159d512c3a71f3e05ea48d76a9e50138c9`

```dockerfile
```

-	Layers:
	-	`sha256:6a3315b796f54d91b25dda575a3542cb5671e7a85e4848023acc1db3021618b1`  
		Last Modified: Tue, 14 May 2024 03:08:50 GMT  
		Size: 3.1 MB (3111558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cef1c8446462f1ac9ec3d8470a8268ab860869150f62d11181b78e9dcb9d5f4`  
		Last Modified: Tue, 14 May 2024 03:08:51 GMT  
		Size: 17.3 KB (17269 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.4` - linux; arm variant v7

```console
$ docker pull swipl@sha256:d084a8c246e4249e66fe0130e2fb7c625b37aebe259bee0929e5b290cf474f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82888974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abea2fdf6c043838c74afa9faa6f67b6eda2e0a0c8338bd318f595640838bb1`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 16:13:38 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 26 Apr 2024 16:13:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
ENV LANG=C.UTF-8
# Fri, 26 Apr 2024 16:13:38 GMT
RUN set -eux;     SWIPL_VER=9.2.4;     SWIPL_CHECKSUM=d53cc13380b60ec4edeea0caead26af4d0e6bd877f458cf4fc6d6f90bd6e987c;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a85f6c4f8d2b04a5f5c9a032f3c08054688f8a2e571990cbf419ddc1bfafe3f`  
		Last Modified: Thu, 25 Apr 2024 00:21:21 GMT  
		Size: 43.7 MB (43705883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9348cada5d8edbb87a9c99eeff9cc8670e8845a546e509210095718d5ccf2583`  
		Last Modified: Sat, 27 Apr 2024 00:17:33 GMT  
		Size: 14.4 MB (14442649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.4` - unknown; unknown

```console
$ docker pull swipl@sha256:ef33560796b17c337b94d68cdb75789160cfa8eb36d544f67cc0e0e906447d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ae5a08adb1f699ae58e0f43038609a9b186b871c612784075a6e5b92ba5dcb`

```dockerfile
```

-	Layers:
	-	`sha256:b3720f26ac176c9c2745cb0cc69863b01f155023ed8a6acdd1571eed4f2f0ba7`  
		Last Modified: Sat, 27 Apr 2024 00:17:32 GMT  
		Size: 3.1 MB (3114080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:281ba33030aca94f5b07613fd3e0aa688e32ec00929a4d6667407d91a84aa599`  
		Last Modified: Sat, 27 Apr 2024 00:17:31 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.4` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:14dde9f761f17ddef447f4eb3724c5803c84227086d053d3ec0df273624d73d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94482942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c8216f7194f9fa8da675342ac2d442ff17f7c789b38fc90ce486f9a620a6d9`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 16:13:38 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 26 Apr 2024 16:13:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
ENV LANG=C.UTF-8
# Fri, 26 Apr 2024 16:13:38 GMT
RUN set -eux;     SWIPL_VER=9.2.4;     SWIPL_CHECKSUM=d53cc13380b60ec4edeea0caead26af4d0e6bd877f458cf4fc6d6f90bd6e987c;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a7e47a35db174e980e1e92f33393550204e5126b6c76c6d091e9cf868283d2`  
		Last Modified: Tue, 30 Apr 2024 06:43:04 GMT  
		Size: 47.7 MB (47679099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfd04facdf27b0a73ba57ef2365b177840555875a0c8d8652cf9cc0f65c0aac`  
		Last Modified: Tue, 30 Apr 2024 06:43:04 GMT  
		Size: 17.6 MB (17623908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.4` - unknown; unknown

```console
$ docker pull swipl@sha256:1abf3f5a7f5ac1734e1e1696e0f358db026dd3f963123e296e75d0b94b4b71d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071853a933d22f9ec4308b85277a753a4c69dbde2515eb0407a5c21421f03f24`

```dockerfile
```

-	Layers:
	-	`sha256:bdb771d6dcb9df8dd061c5bc937143d32afeab34a7957a68604da6e0de30849e`  
		Last Modified: Tue, 30 Apr 2024 06:43:03 GMT  
		Size: 3.1 MB (3111871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c1d5e483e93af0e301990c5c542860c02f19796ade12bee7d69524366188fb2`  
		Last Modified: Tue, 30 Apr 2024 06:43:03 GMT  
		Size: 17.1 KB (17110 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:9.3.6`

**does not exist** (yet?)

## `swipl:latest`

```console
$ docker pull swipl@sha256:6777c951f9ced0bfe9f46380344f91be9c621c1bf5081c210b5cac836ac62f1d
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
$ docker pull swipl@sha256:4a6aa6193f83d7a77df834d823eafa274877d335ad81a97f62ccd25b41e13dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96500101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43b3ad938b59e80e6cff8453f9c17e0c282f50ce48920b2cc68cc50906b88c1`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 26 Apr 2024 16:13:38 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Fri, 26 Apr 2024 16:13:38 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 16:13:38 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 26 Apr 2024 16:13:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
ENV LANG=C.UTF-8
# Fri, 26 Apr 2024 16:13:38 GMT
RUN set -eux;     SWIPL_VER=9.3.2;     SWIPL_CHECKSUM=c329123b4f63aa8d1566f4097af58412588d4e7ad16a5fd743f97b4be6733410;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67091bb222a8adad1ee24c7abb5c15e299f3a040bb1a9cbd316e6c87a80c6446`  
		Last Modified: Tue, 14 May 2024 03:09:08 GMT  
		Size: 49.2 MB (49207279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cae2b631529c3801dbaaaccaff65b805e77e5cd7ea6a656cc911ff66020756`  
		Last Modified: Tue, 14 May 2024 03:09:06 GMT  
		Size: 18.1 MB (18142411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:1638d97290058b107e49e761e8ca67452f7747ee5db69a8e35a9e538c827fe2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bdce32622dd54e8a8d1f6154efb0ca6044ae9d3b0ae5c184801fbddd12fce8`

```dockerfile
```

-	Layers:
	-	`sha256:1824bdf44527b1977d1c2de9b43b4006a1b24eb45122579f4322dbf8d5f1e6ea`  
		Last Modified: Tue, 14 May 2024 03:09:06 GMT  
		Size: 3.1 MB (3111558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97b45cc3f95c73a8b0d082036594a40fe07c1bd2c1518a98d87081342d89c8d`  
		Last Modified: Tue, 14 May 2024 03:09:06 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:8aa46bdd36f381fad8727ee2f0b85e86dba041689cb4b65c0078faee4a72fd0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82872068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0145007f648c47d42280af78ca8c0acc25d1e84654d22240f663ecfba074045a`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
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
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a85f6c4f8d2b04a5f5c9a032f3c08054688f8a2e571990cbf419ddc1bfafe3f`  
		Last Modified: Thu, 25 Apr 2024 00:21:21 GMT  
		Size: 43.7 MB (43705883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b570b2dad1452724a3357462b75d7c415293c8fad36a9f8bbdcab5e5888125f`  
		Last Modified: Thu, 25 Apr 2024 00:21:20 GMT  
		Size: 14.4 MB (14425743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:edab33198a5e00c3c3dcd761edf8b7a9690993962c1788aa34c6357bee9b8af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1fb2d89d38a38d221174fa7d7bc8e78fbd7b5387e287d01f21e710b78c8fde`

```dockerfile
```

-	Layers:
	-	`sha256:43291b88cce5992aea32452193bf725c7b591cf257ac80b1c890253b52229bd1`  
		Last Modified: Thu, 25 Apr 2024 00:21:20 GMT  
		Size: 3.1 MB (3114080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:846eb5304ccd95dc01f0edd787e4e172ab8bfa9d4cc915521667ca9a90fea0cc`  
		Last Modified: Thu, 25 Apr 2024 00:21:19 GMT  
		Size: 17.2 KB (17170 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:61fab27cd61b55b21c18c4e428b6075640fe7400bdce1dd73521d64fa8191b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94459129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3aa8b76f1269ca22728907c203f4d4826b433a83fab7476e6219441cf14121`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
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
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f38391e5cb4f2236efca5d268a4dcf87e60aafb4065904332f077a3a294031`  
		Last Modified: Thu, 25 Apr 2024 19:42:50 GMT  
		Size: 47.7 MB (47679051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b7f6aa23cf827ea1b193db998b9ba0397ed396de43e20206551ca1eb4aecc1`  
		Last Modified: Thu, 25 Apr 2024 19:42:49 GMT  
		Size: 17.6 MB (17600143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:55f2aa2dfb767d2ed18b7b241d1d46282140fca232f7a1cf72b1b212e641231c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60b36dad2817fe2369c5b41025cd57ffc8039380b90b6c1618ff14a51e67760`

```dockerfile
```

-	Layers:
	-	`sha256:2dc9b9bceb3b524f54eae45ddd226fc04a325ff01b92ca618b2512e30ea66ae4`  
		Last Modified: Thu, 25 Apr 2024 19:42:49 GMT  
		Size: 3.1 MB (3111871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d424bc0aa7530fcf903cd69f02b168fd86d2a23fb86392c0c5404219d5eed67`  
		Last Modified: Thu, 25 Apr 2024 19:42:48 GMT  
		Size: 17.1 KB (17109 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:stable`

```console
$ docker pull swipl@sha256:b1c25241b12060ce5cdff3ae6a77275280a3909cebb3ad2c1a99fa451d612d74
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
$ docker pull swipl@sha256:6444c9b3c5694b2408a9a92ab245eb20ae99dcc0f38cfde28c6f653d99e1034f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96520643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a39a31ecff2b317a357e5918343f7fd54b29c4a2c4c45e3f52f9453f0bdeef2`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 26 Apr 2024 16:13:38 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Fri, 26 Apr 2024 16:13:38 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 16:13:38 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 26 Apr 2024 16:13:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
ENV LANG=C.UTF-8
# Fri, 26 Apr 2024 16:13:38 GMT
RUN set -eux;     SWIPL_VER=9.2.4;     SWIPL_CHECKSUM=d53cc13380b60ec4edeea0caead26af4d0e6bd877f458cf4fc6d6f90bd6e987c;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51df949ce4ea429c4a5bef71872cd262035dd773889fc179b61cafc0110e7ff7`  
		Last Modified: Tue, 14 May 2024 03:08:51 GMT  
		Size: 49.2 MB (49207399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fbc908e2a28e9a24341fc7228d9ef2283b06988a1fc9c161c52b3561baa46c`  
		Last Modified: Tue, 14 May 2024 03:08:51 GMT  
		Size: 18.2 MB (18162833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:67c0a23df8a008493462041e25484eb58f2df8d77d98d690fc733b773d99d808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b201355c8f43edc9f72b2e95ffb0159d512c3a71f3e05ea48d76a9e50138c9`

```dockerfile
```

-	Layers:
	-	`sha256:6a3315b796f54d91b25dda575a3542cb5671e7a85e4848023acc1db3021618b1`  
		Last Modified: Tue, 14 May 2024 03:08:50 GMT  
		Size: 3.1 MB (3111558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cef1c8446462f1ac9ec3d8470a8268ab860869150f62d11181b78e9dcb9d5f4`  
		Last Modified: Tue, 14 May 2024 03:08:51 GMT  
		Size: 17.3 KB (17269 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:d084a8c246e4249e66fe0130e2fb7c625b37aebe259bee0929e5b290cf474f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82888974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abea2fdf6c043838c74afa9faa6f67b6eda2e0a0c8338bd318f595640838bb1`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 16:13:38 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 26 Apr 2024 16:13:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
ENV LANG=C.UTF-8
# Fri, 26 Apr 2024 16:13:38 GMT
RUN set -eux;     SWIPL_VER=9.2.4;     SWIPL_CHECKSUM=d53cc13380b60ec4edeea0caead26af4d0e6bd877f458cf4fc6d6f90bd6e987c;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a85f6c4f8d2b04a5f5c9a032f3c08054688f8a2e571990cbf419ddc1bfafe3f`  
		Last Modified: Thu, 25 Apr 2024 00:21:21 GMT  
		Size: 43.7 MB (43705883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9348cada5d8edbb87a9c99eeff9cc8670e8845a546e509210095718d5ccf2583`  
		Last Modified: Sat, 27 Apr 2024 00:17:33 GMT  
		Size: 14.4 MB (14442649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:ef33560796b17c337b94d68cdb75789160cfa8eb36d544f67cc0e0e906447d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ae5a08adb1f699ae58e0f43038609a9b186b871c612784075a6e5b92ba5dcb`

```dockerfile
```

-	Layers:
	-	`sha256:b3720f26ac176c9c2745cb0cc69863b01f155023ed8a6acdd1571eed4f2f0ba7`  
		Last Modified: Sat, 27 Apr 2024 00:17:32 GMT  
		Size: 3.1 MB (3114080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:281ba33030aca94f5b07613fd3e0aa688e32ec00929a4d6667407d91a84aa599`  
		Last Modified: Sat, 27 Apr 2024 00:17:31 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:14dde9f761f17ddef447f4eb3724c5803c84227086d053d3ec0df273624d73d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94482942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c8216f7194f9fa8da675342ac2d442ff17f7c789b38fc90ce486f9a620a6d9`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 16:13:38 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 26 Apr 2024 16:13:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
ENV LANG=C.UTF-8
# Fri, 26 Apr 2024 16:13:38 GMT
RUN set -eux;     SWIPL_VER=9.2.4;     SWIPL_CHECKSUM=d53cc13380b60ec4edeea0caead26af4d0e6bd877f458cf4fc6d6f90bd6e987c;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 26 Apr 2024 16:13:38 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a7e47a35db174e980e1e92f33393550204e5126b6c76c6d091e9cf868283d2`  
		Last Modified: Tue, 30 Apr 2024 06:43:04 GMT  
		Size: 47.7 MB (47679099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfd04facdf27b0a73ba57ef2365b177840555875a0c8d8652cf9cc0f65c0aac`  
		Last Modified: Tue, 30 Apr 2024 06:43:04 GMT  
		Size: 17.6 MB (17623908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:1abf3f5a7f5ac1734e1e1696e0f358db026dd3f963123e296e75d0b94b4b71d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071853a933d22f9ec4308b85277a753a4c69dbde2515eb0407a5c21421f03f24`

```dockerfile
```

-	Layers:
	-	`sha256:bdb771d6dcb9df8dd061c5bc937143d32afeab34a7957a68604da6e0de30849e`  
		Last Modified: Tue, 30 Apr 2024 06:43:03 GMT  
		Size: 3.1 MB (3111871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c1d5e483e93af0e301990c5c542860c02f19796ade12bee7d69524366188fb2`  
		Last Modified: Tue, 30 Apr 2024 06:43:03 GMT  
		Size: 17.1 KB (17110 bytes)  
		MIME: application/vnd.in-toto+json
