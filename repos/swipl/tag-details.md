<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:9.2.4`](#swipl924)
-	[`swipl:9.3.2`](#swipl932)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:9.2.4`

```console
$ docker pull swipl@sha256:352bd50afc38e3194064bd2998df0eb9add4cbb423723ad06edf1afd9fcd6e8e
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
$ docker pull swipl@sha256:734b01ee632cae3fdc5ee73dac9b073df8b5093659dd0e2a72e04a33262c8891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96520806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6596e893e23929369b66a270245dff463c024408570fbd93454b7180f27fa1d1`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
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
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdbb49795e16d488ac926e83c5b871a9f566f91fc1a3f8ed8c7e6bfaab689e8`  
		Last Modified: Fri, 26 Apr 2024 20:33:35 GMT  
		Size: 49.2 MB (49207345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61cc37016c6ddfef9a96573b0a566c0f23e1b6b8547597a0b939d56b8070f89`  
		Last Modified: Fri, 26 Apr 2024 20:33:34 GMT  
		Size: 18.2 MB (18162982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.4` - unknown; unknown

```console
$ docker pull swipl@sha256:bd3164f70da514385a873d267716d472be9cdf73ff4b7934b979fb0239e59969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7a6e5f7f9a0128da24e7c7f4c3d0a31b3659eca0121819309285acdc6381cf`

```dockerfile
```

-	Layers:
	-	`sha256:825c248d313f9ce65fb0b7b1c5b912f1ae90be0fc146e5a9b19647788b1d93c1`  
		Last Modified: Fri, 26 Apr 2024 20:33:33 GMT  
		Size: 3.1 MB (3111558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44fbdfa545796c4f38649ea7b1a261ce921304c8385013179df1bed341a5175`  
		Last Modified: Fri, 26 Apr 2024 20:33:33 GMT  
		Size: 17.3 KB (17271 bytes)  
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

## `swipl:9.3.2`

```console
$ docker pull swipl@sha256:732ef84dbc2454d43e98056c39563bd3286f2d0befd23354380167cada3d912d
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
$ docker pull swipl@sha256:0f6dd13cd626cdeb48680738f9ba85cef6d2404d1598d8f3be74cc9e5a2d790b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96497757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f942ce9f7ff4bdc88eb96c0698ffd58da08aafe51d450794d7877aaf1117c812`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
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
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51927acb419d417fc5ae774c4df4ec132a122698caddaa0671206f4a447e39fa`  
		Last Modified: Wed, 24 Apr 2024 05:23:22 GMT  
		Size: 49.2 MB (49207381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b369fd82b914073be5c845342fe9bf3fe86688c1920e39cd0b12badeba321a0`  
		Last Modified: Wed, 24 Apr 2024 05:23:21 GMT  
		Size: 18.1 MB (18139897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.2` - unknown; unknown

```console
$ docker pull swipl@sha256:ecef6c761163512b67fed3d122dae29df648d18b6378c97cb01741621ac13b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da27c677dfb68a908c6ddcd5cd1f3cf0e801033b8371708da2ba61c1f7b41b9`

```dockerfile
```

-	Layers:
	-	`sha256:b60470bcb11e45548ae9cfd95f3d7c4ca1eae31fdb917c5713a4aea1d2734428`  
		Last Modified: Wed, 24 Apr 2024 05:23:21 GMT  
		Size: 3.1 MB (3111558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2350edf270dc5e52318f82bf1346d5c006be8b82caf721ae2e02c582282db13`  
		Last Modified: Wed, 24 Apr 2024 05:23:21 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.2` - linux; arm variant v7

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

### `swipl:9.3.2` - unknown; unknown

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

### `swipl:9.3.2` - linux; arm64 variant v8

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

### `swipl:9.3.2` - unknown; unknown

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

## `swipl:latest`

```console
$ docker pull swipl@sha256:732ef84dbc2454d43e98056c39563bd3286f2d0befd23354380167cada3d912d
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
$ docker pull swipl@sha256:0f6dd13cd626cdeb48680738f9ba85cef6d2404d1598d8f3be74cc9e5a2d790b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96497757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f942ce9f7ff4bdc88eb96c0698ffd58da08aafe51d450794d7877aaf1117c812`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 05 Apr 2024 10:22:13 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
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
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51927acb419d417fc5ae774c4df4ec132a122698caddaa0671206f4a447e39fa`  
		Last Modified: Wed, 24 Apr 2024 05:23:22 GMT  
		Size: 49.2 MB (49207381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b369fd82b914073be5c845342fe9bf3fe86688c1920e39cd0b12badeba321a0`  
		Last Modified: Wed, 24 Apr 2024 05:23:21 GMT  
		Size: 18.1 MB (18139897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:ecef6c761163512b67fed3d122dae29df648d18b6378c97cb01741621ac13b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da27c677dfb68a908c6ddcd5cd1f3cf0e801033b8371708da2ba61c1f7b41b9`

```dockerfile
```

-	Layers:
	-	`sha256:b60470bcb11e45548ae9cfd95f3d7c4ca1eae31fdb917c5713a4aea1d2734428`  
		Last Modified: Wed, 24 Apr 2024 05:23:21 GMT  
		Size: 3.1 MB (3111558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2350edf270dc5e52318f82bf1346d5c006be8b82caf721ae2e02c582282db13`  
		Last Modified: Wed, 24 Apr 2024 05:23:21 GMT  
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
$ docker pull swipl@sha256:352bd50afc38e3194064bd2998df0eb9add4cbb423723ad06edf1afd9fcd6e8e
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
$ docker pull swipl@sha256:734b01ee632cae3fdc5ee73dac9b073df8b5093659dd0e2a72e04a33262c8891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96520806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6596e893e23929369b66a270245dff463c024408570fbd93454b7180f27fa1d1`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
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
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdbb49795e16d488ac926e83c5b871a9f566f91fc1a3f8ed8c7e6bfaab689e8`  
		Last Modified: Fri, 26 Apr 2024 20:33:35 GMT  
		Size: 49.2 MB (49207345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61cc37016c6ddfef9a96573b0a566c0f23e1b6b8547597a0b939d56b8070f89`  
		Last Modified: Fri, 26 Apr 2024 20:33:34 GMT  
		Size: 18.2 MB (18162982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:bd3164f70da514385a873d267716d472be9cdf73ff4b7934b979fb0239e59969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7a6e5f7f9a0128da24e7c7f4c3d0a31b3659eca0121819309285acdc6381cf`

```dockerfile
```

-	Layers:
	-	`sha256:825c248d313f9ce65fb0b7b1c5b912f1ae90be0fc146e5a9b19647788b1d93c1`  
		Last Modified: Fri, 26 Apr 2024 20:33:33 GMT  
		Size: 3.1 MB (3111558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44fbdfa545796c4f38649ea7b1a261ce921304c8385013179df1bed341a5175`  
		Last Modified: Fri, 26 Apr 2024 20:33:33 GMT  
		Size: 17.3 KB (17271 bytes)  
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
