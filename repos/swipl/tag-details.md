<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:9.2.4`](#swipl924)
-	[`swipl:9.3.6`](#swipl936)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:9.2.4`

```console
$ docker pull swipl@sha256:3d5e9bdc6cfb77567ac0e5a55a990c2a5fd1306c37c98c8613ed7b296ae38f3b
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
$ docker pull swipl@sha256:93af2394dc5e1fb8dd168537c1b50f9cf140211275e3db9021fc4c6c7a080c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82889699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c7ab85c21ac51b8a3158fcb6c13adbfe6eec8561bc63e3c413a18065367531`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:21:07 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 14 May 2024 12:21:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 May 2024 12:21:07 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 12:21:07 GMT
RUN set -eux;     SWIPL_VER=9.2.4;     SWIPL_CHECKSUM=d53cc13380b60ec4edeea0caead26af4d0e6bd877f458cf4fc6d6f90bd6e987c;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 14 May 2024 12:21:07 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34321325c0b8a549e746addf7628b2f639404d7bafca34fd293351f7028c2581`  
		Last Modified: Tue, 14 May 2024 20:31:23 GMT  
		Size: 43.7 MB (43706383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb2fc40a7d687d7b6deb7864360632afa1adeb2d0c1a8d07ee731c789399caa`  
		Last Modified: Tue, 14 May 2024 20:31:23 GMT  
		Size: 14.4 MB (14443111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.4` - unknown; unknown

```console
$ docker pull swipl@sha256:ae88f91f8996a9e2ea0258d2f6b8e2e4be8aeb4a4871f1e154f5ed091b9f64d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6591521e86a35f894daf8b27ee1e20dae031afe86415ea42b4ac258d77d0a5`

```dockerfile
```

-	Layers:
	-	`sha256:f8aea848729320c93bdba7f4139d4847a7dfa3263c783e16e3fd1bad40ac0ffc`  
		Last Modified: Tue, 14 May 2024 20:31:22 GMT  
		Size: 3.1 MB (3114080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633ba708100def7d0cf3b43763edabca1f69cd41fc13f4330a93c837dc608ee3`  
		Last Modified: Tue, 14 May 2024 20:31:22 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.4` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:1a15e5db2d03b041b96513d5e34a8cecd84da60c75bcf969f51dd30d034e2373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94482544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed021fabe331c63f26ecfffd8c7acd633ccfabcb3291d303b11c0bb7dc0a8786`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:21:07 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 14 May 2024 12:21:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 May 2024 12:21:07 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 12:21:07 GMT
RUN set -eux;     SWIPL_VER=9.2.4;     SWIPL_CHECKSUM=d53cc13380b60ec4edeea0caead26af4d0e6bd877f458cf4fc6d6f90bd6e987c;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 14 May 2024 12:21:07 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae165731273e36f24fa3464c4097bfed02c3e06d75442acc825f5cc91ff46f8`  
		Last Modified: Tue, 14 May 2024 23:50:38 GMT  
		Size: 47.7 MB (47679246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dbfc134ba6537dd453ae30267cce4d401f27cff1547ccd98561514aef4f2d`  
		Last Modified: Tue, 14 May 2024 23:50:37 GMT  
		Size: 17.6 MB (17623795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.4` - unknown; unknown

```console
$ docker pull swipl@sha256:150b922d9c4b566d27e5a22eaef0f3dfe8642d9fcd258fb4c0e7ff3225b5cd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fbb8458d43f5c9f9aeb930c48751abe0d9630cb4372c7accf9434266157936`

```dockerfile
```

-	Layers:
	-	`sha256:7cc73e7027cac5c478d8977493e9011a27b665273faeab99caa0c3e39a3595a3`  
		Last Modified: Tue, 14 May 2024 23:50:37 GMT  
		Size: 3.1 MB (3111871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb786b05b9d039fb3739141130efeb39c743e1df8e96762c4fb8f7bd11a6b195`  
		Last Modified: Tue, 14 May 2024 23:50:36 GMT  
		Size: 17.1 KB (17110 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:9.3.6`

```console
$ docker pull swipl@sha256:d267dabfcb638059c5ab12a7e32757c13dddc72605ce507dc029d74159be3bad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.3.6` - linux; amd64

```console
$ docker pull swipl@sha256:d0dcd71dac59e5214393ac714199c49b04958f6774eb5c25e9543de69b0fb5dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96639293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e96485004712a88f7b872a01a083adab0df7f1340dace97e379ef32db1aaa04`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:21:07 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 14 May 2024 12:21:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 May 2024 12:21:07 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 12:21:07 GMT
RUN set -eux;     SWIPL_VER=9.3.6;     SWIPL_CHECKSUM=381074a9c82bc3ccfd864d84c1e2f9589b8fe64b89ecf459a0068518850777a3;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 14 May 2024 12:21:07 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c328561a41acb45d3e8fa30d600d43f8114d21005b284e492fae12de2b963060`  
		Last Modified: Tue, 14 May 2024 19:09:31 GMT  
		Size: 49.2 MB (49207432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bad39bcdf1dbc64f7df6a9e9958189cddf6d7eab60098d1c36643d68059fd76`  
		Last Modified: Tue, 14 May 2024 19:09:30 GMT  
		Size: 18.3 MB (18281450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.6` - unknown; unknown

```console
$ docker pull swipl@sha256:94beb34050c5dc92d6d4b27b5055823dddb81e9e251cbdc181b178917c1613de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa661fb6e99e27fda815adf1ec6c5fe45253a83e46f2fa5739d758507a84613`

```dockerfile
```

-	Layers:
	-	`sha256:aa5f1f5bc387b3f72082f8b42884a480d6b6141bd8477e1b6520b2b046b647c6`  
		Last Modified: Tue, 14 May 2024 19:09:30 GMT  
		Size: 3.1 MB (3111558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e166e6a9a44a337009d319343706bbaab2dae2a91ef6f5f3358ebec314e920dc`  
		Last Modified: Tue, 14 May 2024 19:09:30 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.6` - linux; arm variant v7

```console
$ docker pull swipl@sha256:dc02996f2838bddfb7db08cd2f53b2d4c82730d90813c5a367e7be1bfcbfab2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83075148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747fba9467a8bbbdc60e19ea00a68969d53d54ca624139d9f5fac7cac9156c36`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:21:07 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 14 May 2024 12:21:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 May 2024 12:21:07 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 12:21:07 GMT
RUN set -eux;     SWIPL_VER=9.3.6;     SWIPL_CHECKSUM=381074a9c82bc3ccfd864d84c1e2f9589b8fe64b89ecf459a0068518850777a3;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 14 May 2024 12:21:07 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34321325c0b8a549e746addf7628b2f639404d7bafca34fd293351f7028c2581`  
		Last Modified: Tue, 14 May 2024 20:31:23 GMT  
		Size: 43.7 MB (43706383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3384735e20da690bc9461403c82dd5836795a1b24f57db54cec985948b39323`  
		Last Modified: Wed, 15 May 2024 07:51:41 GMT  
		Size: 14.6 MB (14628560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.6` - unknown; unknown

```console
$ docker pull swipl@sha256:d3804cce51a99d7696e28cd16a6f5df43d4c59f2f209a6cfe3ee7e41e106b27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd585a2fd608d01451032823d0d2f82eabea414ca057b08303f96241f2e575ed`

```dockerfile
```

-	Layers:
	-	`sha256:23f1dff10a7f71dfced183d0f42a535e189f4b74b1a786ea64c542f26dee4035`  
		Last Modified: Wed, 15 May 2024 07:51:41 GMT  
		Size: 3.1 MB (3114080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b38879d58afd7bd99a8ce8f53b48967557e3691b3c4aaf30ae10b9407b231625`  
		Last Modified: Wed, 15 May 2024 07:51:40 GMT  
		Size: 17.2 KB (17170 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.6` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:43888ba9f9cff0eee7f587c96625c6c52c34890388a0c3172da89f64d3bf754e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94590927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094d87a01780721c84cf5b6935df2309beaea8f0fbc8eba42e0ed252ab895252`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:21:07 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 14 May 2024 12:21:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 May 2024 12:21:07 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 12:21:07 GMT
RUN set -eux;     SWIPL_VER=9.3.6;     SWIPL_CHECKSUM=381074a9c82bc3ccfd864d84c1e2f9589b8fe64b89ecf459a0068518850777a3;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 14 May 2024 12:21:07 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae165731273e36f24fa3464c4097bfed02c3e06d75442acc825f5cc91ff46f8`  
		Last Modified: Tue, 14 May 2024 23:50:38 GMT  
		Size: 47.7 MB (47679246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98eeea5cfc66bee47b76ee2723394b66d1956a20e57d61ff4f0a2725dcb20487`  
		Last Modified: Wed, 15 May 2024 15:06:11 GMT  
		Size: 17.7 MB (17732178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.6` - unknown; unknown

```console
$ docker pull swipl@sha256:6480db0bebc9f446efd002547e878ec527ba60bfd60551fb6dd13cabb6232cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96b8103323cf856a865aa2adac7fabec8d1eec0786f201c3b5d7d20147f5cfa`

```dockerfile
```

-	Layers:
	-	`sha256:9973e81976e587ce9d797bd4b22367a7dcaf5f10b096350f0c143701bce4966b`  
		Last Modified: Wed, 15 May 2024 15:06:11 GMT  
		Size: 3.1 MB (3111871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeccfed8d4ecc839eb825719310fe8ff063665214d3d5e6643908db27bbaad31`  
		Last Modified: Wed, 15 May 2024 15:06:11 GMT  
		Size: 17.1 KB (17109 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:latest`

```console
$ docker pull swipl@sha256:d267dabfcb638059c5ab12a7e32757c13dddc72605ce507dc029d74159be3bad
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
$ docker pull swipl@sha256:d0dcd71dac59e5214393ac714199c49b04958f6774eb5c25e9543de69b0fb5dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96639293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e96485004712a88f7b872a01a083adab0df7f1340dace97e379ef32db1aaa04`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:21:07 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 14 May 2024 12:21:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 May 2024 12:21:07 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 12:21:07 GMT
RUN set -eux;     SWIPL_VER=9.3.6;     SWIPL_CHECKSUM=381074a9c82bc3ccfd864d84c1e2f9589b8fe64b89ecf459a0068518850777a3;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 14 May 2024 12:21:07 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c328561a41acb45d3e8fa30d600d43f8114d21005b284e492fae12de2b963060`  
		Last Modified: Tue, 14 May 2024 19:09:31 GMT  
		Size: 49.2 MB (49207432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bad39bcdf1dbc64f7df6a9e9958189cddf6d7eab60098d1c36643d68059fd76`  
		Last Modified: Tue, 14 May 2024 19:09:30 GMT  
		Size: 18.3 MB (18281450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:94beb34050c5dc92d6d4b27b5055823dddb81e9e251cbdc181b178917c1613de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa661fb6e99e27fda815adf1ec6c5fe45253a83e46f2fa5739d758507a84613`

```dockerfile
```

-	Layers:
	-	`sha256:aa5f1f5bc387b3f72082f8b42884a480d6b6141bd8477e1b6520b2b046b647c6`  
		Last Modified: Tue, 14 May 2024 19:09:30 GMT  
		Size: 3.1 MB (3111558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e166e6a9a44a337009d319343706bbaab2dae2a91ef6f5f3358ebec314e920dc`  
		Last Modified: Tue, 14 May 2024 19:09:30 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:dc02996f2838bddfb7db08cd2f53b2d4c82730d90813c5a367e7be1bfcbfab2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83075148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747fba9467a8bbbdc60e19ea00a68969d53d54ca624139d9f5fac7cac9156c36`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:21:07 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 14 May 2024 12:21:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 May 2024 12:21:07 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 12:21:07 GMT
RUN set -eux;     SWIPL_VER=9.3.6;     SWIPL_CHECKSUM=381074a9c82bc3ccfd864d84c1e2f9589b8fe64b89ecf459a0068518850777a3;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 14 May 2024 12:21:07 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34321325c0b8a549e746addf7628b2f639404d7bafca34fd293351f7028c2581`  
		Last Modified: Tue, 14 May 2024 20:31:23 GMT  
		Size: 43.7 MB (43706383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3384735e20da690bc9461403c82dd5836795a1b24f57db54cec985948b39323`  
		Last Modified: Wed, 15 May 2024 07:51:41 GMT  
		Size: 14.6 MB (14628560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:d3804cce51a99d7696e28cd16a6f5df43d4c59f2f209a6cfe3ee7e41e106b27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd585a2fd608d01451032823d0d2f82eabea414ca057b08303f96241f2e575ed`

```dockerfile
```

-	Layers:
	-	`sha256:23f1dff10a7f71dfced183d0f42a535e189f4b74b1a786ea64c542f26dee4035`  
		Last Modified: Wed, 15 May 2024 07:51:41 GMT  
		Size: 3.1 MB (3114080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b38879d58afd7bd99a8ce8f53b48967557e3691b3c4aaf30ae10b9407b231625`  
		Last Modified: Wed, 15 May 2024 07:51:40 GMT  
		Size: 17.2 KB (17170 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:43888ba9f9cff0eee7f587c96625c6c52c34890388a0c3172da89f64d3bf754e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94590927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094d87a01780721c84cf5b6935df2309beaea8f0fbc8eba42e0ed252ab895252`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:21:07 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 14 May 2024 12:21:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 May 2024 12:21:07 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 12:21:07 GMT
RUN set -eux;     SWIPL_VER=9.3.6;     SWIPL_CHECKSUM=381074a9c82bc3ccfd864d84c1e2f9589b8fe64b89ecf459a0068518850777a3;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 14 May 2024 12:21:07 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae165731273e36f24fa3464c4097bfed02c3e06d75442acc825f5cc91ff46f8`  
		Last Modified: Tue, 14 May 2024 23:50:38 GMT  
		Size: 47.7 MB (47679246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98eeea5cfc66bee47b76ee2723394b66d1956a20e57d61ff4f0a2725dcb20487`  
		Last Modified: Wed, 15 May 2024 15:06:11 GMT  
		Size: 17.7 MB (17732178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:6480db0bebc9f446efd002547e878ec527ba60bfd60551fb6dd13cabb6232cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96b8103323cf856a865aa2adac7fabec8d1eec0786f201c3b5d7d20147f5cfa`

```dockerfile
```

-	Layers:
	-	`sha256:9973e81976e587ce9d797bd4b22367a7dcaf5f10b096350f0c143701bce4966b`  
		Last Modified: Wed, 15 May 2024 15:06:11 GMT  
		Size: 3.1 MB (3111871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeccfed8d4ecc839eb825719310fe8ff063665214d3d5e6643908db27bbaad31`  
		Last Modified: Wed, 15 May 2024 15:06:11 GMT  
		Size: 17.1 KB (17109 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:stable`

```console
$ docker pull swipl@sha256:3d5e9bdc6cfb77567ac0e5a55a990c2a5fd1306c37c98c8613ed7b296ae38f3b
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
$ docker pull swipl@sha256:93af2394dc5e1fb8dd168537c1b50f9cf140211275e3db9021fc4c6c7a080c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82889699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c7ab85c21ac51b8a3158fcb6c13adbfe6eec8561bc63e3c413a18065367531`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:21:07 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 14 May 2024 12:21:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 May 2024 12:21:07 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 12:21:07 GMT
RUN set -eux;     SWIPL_VER=9.2.4;     SWIPL_CHECKSUM=d53cc13380b60ec4edeea0caead26af4d0e6bd877f458cf4fc6d6f90bd6e987c;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 14 May 2024 12:21:07 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34321325c0b8a549e746addf7628b2f639404d7bafca34fd293351f7028c2581`  
		Last Modified: Tue, 14 May 2024 20:31:23 GMT  
		Size: 43.7 MB (43706383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb2fc40a7d687d7b6deb7864360632afa1adeb2d0c1a8d07ee731c789399caa`  
		Last Modified: Tue, 14 May 2024 20:31:23 GMT  
		Size: 14.4 MB (14443111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:ae88f91f8996a9e2ea0258d2f6b8e2e4be8aeb4a4871f1e154f5ed091b9f64d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6591521e86a35f894daf8b27ee1e20dae031afe86415ea42b4ac258d77d0a5`

```dockerfile
```

-	Layers:
	-	`sha256:f8aea848729320c93bdba7f4139d4847a7dfa3263c783e16e3fd1bad40ac0ffc`  
		Last Modified: Tue, 14 May 2024 20:31:22 GMT  
		Size: 3.1 MB (3114080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633ba708100def7d0cf3b43763edabca1f69cd41fc13f4330a93c837dc608ee3`  
		Last Modified: Tue, 14 May 2024 20:31:22 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:1a15e5db2d03b041b96513d5e34a8cecd84da60c75bcf969f51dd30d034e2373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94482544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed021fabe331c63f26ecfffd8c7acd633ccfabcb3291d303b11c0bb7dc0a8786`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:21:07 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 14 May 2024 12:21:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 May 2024 12:21:07 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 12:21:07 GMT
RUN set -eux;     SWIPL_VER=9.2.4;     SWIPL_CHECKSUM=d53cc13380b60ec4edeea0caead26af4d0e6bd877f458cf4fc6d6f90bd6e987c;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 14 May 2024 12:21:07 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae165731273e36f24fa3464c4097bfed02c3e06d75442acc825f5cc91ff46f8`  
		Last Modified: Tue, 14 May 2024 23:50:38 GMT  
		Size: 47.7 MB (47679246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9dbfc134ba6537dd453ae30267cce4d401f27cff1547ccd98561514aef4f2d`  
		Last Modified: Tue, 14 May 2024 23:50:37 GMT  
		Size: 17.6 MB (17623795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:150b922d9c4b566d27e5a22eaef0f3dfe8642d9fcd258fb4c0e7ff3225b5cd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fbb8458d43f5c9f9aeb930c48751abe0d9630cb4372c7accf9434266157936`

```dockerfile
```

-	Layers:
	-	`sha256:7cc73e7027cac5c478d8977493e9011a27b665273faeab99caa0c3e39a3595a3`  
		Last Modified: Tue, 14 May 2024 23:50:37 GMT  
		Size: 3.1 MB (3111871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb786b05b9d039fb3739141130efeb39c743e1df8e96762c4fb8f7bd11a6b195`  
		Last Modified: Tue, 14 May 2024 23:50:36 GMT  
		Size: 17.1 KB (17110 bytes)  
		MIME: application/vnd.in-toto+json
