## `swipl:latest`

```console
$ docker pull swipl@sha256:1dcf5073e33dc2be9cb5e5f8f2182bb2fd9a35f9d0560160f639bef5d7d11987
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
