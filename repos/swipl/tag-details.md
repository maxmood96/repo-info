<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:9.2.8`](#swipl928)
-	[`swipl:9.3.14`](#swipl9314)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:9.2.8`

```console
$ docker pull swipl@sha256:94e9188aee2e42c08758cf9e379493eca790e9b08f1687965b03f58f0e079ccd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.2.8` - linux; amd64

```console
$ docker pull swipl@sha256:9d88196372ae372366c3521e128ce53d294ce9d18c4212d2f71dceaba4f93481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96896551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d36b32fd16c03219714ae384c3f80c0c6856019d2d3b111554e8d608be4b3dc`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.2.8;     SWIPL_CHECKSUM=b331637a57c913c49edcfcb10ddcf6c031278ce93d2411d54542778531abb5c7;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03630e44222222e34a9b723b7ebdddaf0d55bbedbfda113c1cef30bbe06dbafe`  
		Last Modified: Tue, 12 Nov 2024 02:24:23 GMT  
		Size: 49.2 MB (49222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618ebb0d6203ef8afe7f315237fa04971cbecbfffe362caca2c375b2850cbfc1`  
		Last Modified: Tue, 12 Nov 2024 02:24:23 GMT  
		Size: 18.5 MB (18545882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.8` - unknown; unknown

```console
$ docker pull swipl@sha256:0e34b6884630329fbb2fdd982ddf1b3143ff7abbd46ecc0a13b1d16c02291562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3184740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2344c1a670c92b8e1a6258d684c204502bdc2902fae5f77de76d0d19bd672b77`

```dockerfile
```

-	Layers:
	-	`sha256:a31ecbc89b4dbdb7b4afedddda43a7bd363fb838af0ed8d6a03d18e5a83fe44a`  
		Last Modified: Tue, 12 Nov 2024 02:24:22 GMT  
		Size: 3.2 MB (3167233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2136514aad85ed501329dd609915e59b537ae41178e61efa73e1c541975ac6c9`  
		Last Modified: Tue, 12 Nov 2024 02:24:22 GMT  
		Size: 17.5 KB (17507 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.8` - linux; arm variant v7

```console
$ docker pull swipl@sha256:9b8d91ac38193908e70b29917dec0464e97b126c206d86b5fd31d9a78fc99d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82560059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4acad6b4a3d5c27b1d51cb4b6bbb6595ced07d8305662a1be130b2e313b16fe`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.2.8;     SWIPL_CHECKSUM=b331637a57c913c49edcfcb10ddcf6c031278ce93d2411d54542778531abb5c7;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d737c752fb77e2ad5236d232ab5a86ea38bcdb521b3ab893a6fa979c8c5966b8`  
		Last Modified: Fri, 18 Oct 2024 02:13:19 GMT  
		Size: 43.7 MB (43723347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba398d2029fc5d3f702fe99398d3e2d32d34245bb6188ab65c017811b36c6cb`  
		Last Modified: Wed, 23 Oct 2024 22:58:27 GMT  
		Size: 14.1 MB (14118515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.8` - unknown; unknown

```console
$ docker pull swipl@sha256:fd4b91dc09e2af07ae4454c26b6922dbe7109a711490b5c562a917d605f9c365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3183465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180b251363d33d8491d329591a062e87225deafe31f3036226aed34d75dda3df`

```dockerfile
```

-	Layers:
	-	`sha256:7973f13f4cc7c35f98d70a2f4ee83e1ad7d26f669ac9c5c510b1f8a4a4279961`  
		Last Modified: Thu, 31 Oct 2024 23:00:47 GMT  
		Size: 3.2 MB (3166069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da65cb1ef35fdf209d56f7c6830b6f73970a20782e2a44d57ee64e269dc89d0c`  
		Last Modified: Thu, 31 Oct 2024 23:00:47 GMT  
		Size: 17.4 KB (17396 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.8` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:c1dffbdd621d26db2705382efde17b701fc47c9f8cfaf615d5f97c1d639333cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94804611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84634ddb9071f382a213df9fd7c54243fc9438497747e24612a3d5f5dc6f9a5`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.2.8;     SWIPL_CHECKSUM=b331637a57c913c49edcfcb10ddcf6c031278ce93d2411d54542778531abb5c7;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a12bec5040e38e2a3fd6e76bc71d86a43b628b60cdfc3433840178d7ec515f3`  
		Last Modified: Tue, 12 Nov 2024 10:36:50 GMT  
		Size: 47.7 MB (47706414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f5f075eccffb4f018fcd03ed02d3fce251b3c6fdc8226d71899f6d9dadba8c`  
		Last Modified: Tue, 12 Nov 2024 10:43:20 GMT  
		Size: 17.9 MB (17940841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.8` - unknown; unknown

```console
$ docker pull swipl@sha256:cfcade3ab5f2e2ca9e5ec823c3472e96d15333beb541c2658bbbfab01af19fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102b4fb9dd32a29dc9ba98c58a1072478960babae012be47cca0c460098489f6`

```dockerfile
```

-	Layers:
	-	`sha256:55230ba367c34935362fdc38866c31ebcca5a1b1333916c4a92c2f772723dffc`  
		Last Modified: Tue, 12 Nov 2024 10:43:19 GMT  
		Size: 3.2 MB (3167572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e57fb79dcff598660520b1e0cbbc8c7bdf2424143a5b7383db60ff3ff1181b92`  
		Last Modified: Tue, 12 Nov 2024 10:43:18 GMT  
		Size: 17.6 KB (17602 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:9.3.14`

```console
$ docker pull swipl@sha256:3091a6fbc589a4f34f80922b6b30b94233d9d42641466affdbf456d61f8b1c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.3.14` - linux; amd64

```console
$ docker pull swipl@sha256:d9604dd73e5ef74d47af16f81a220456ce3daf6eace23a337771bc77cd233767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97061204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c03dedfe237b8eeb38b996b33a59bb00abdbb6acb9b59b5e7c20e301d82cf6`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.3.14;     SWIPL_CHECKSUM=81f73e13afdb3a191bea9238730884a34222cf424f92fe1255d455ebbe127224;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab05e7d2325e60000bbeb41e0be8a5a54d36cf40706a935ebcc6a398bc0bbf25`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 49.2 MB (49222850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6ff44cd7c96d81ac1b20bd5fcd182566f3dad1a75011e2df01f39f095bf4df`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 18.7 MB (18710359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.14` - unknown; unknown

```console
$ docker pull swipl@sha256:f63cee6056bbc0a87ee242064514eaf01c73bc24551b7d4d6c391defd9e632bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3184748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa48357424401ec6f748b5cd5a3dd7629b32972258f3ca951e5d59180a3da33f`

```dockerfile
```

-	Layers:
	-	`sha256:cac160fecae5b1fd0a8a20e9c0914007c1d849e2f14dc65af181bbd4b0d2761d`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 3.2 MB (3167237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c750cf1f1e83279ff3b5e01940ba45d326a1769620d254737eaa5f1c175876e3`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 17.5 KB (17511 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.14` - linux; arm variant v7

```console
$ docker pull swipl@sha256:f390b062c647d2f6ce9b7c4a45beafbc9ae95d5f4d79aadb2bd600459ef2a7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82776846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99df0c5d7302f9c54af3fa0f82c235d2ff8b866afe4c86198b90c92991af928c`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.3.14;     SWIPL_CHECKSUM=81f73e13afdb3a191bea9238730884a34222cf424f92fe1255d455ebbe127224;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d737c752fb77e2ad5236d232ab5a86ea38bcdb521b3ab893a6fa979c8c5966b8`  
		Last Modified: Fri, 18 Oct 2024 02:13:19 GMT  
		Size: 43.7 MB (43723347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ff220951c029e0a9477c0dc8b3fc5421d45c3baf70aad14ca3a2dff64ce1c3`  
		Last Modified: Thu, 31 Oct 2024 23:00:21 GMT  
		Size: 14.3 MB (14335302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.14` - unknown; unknown

```console
$ docker pull swipl@sha256:36c2c0a9b3bd8250f447710e22d3f6ab4f25255ed47da7353016469e782e227c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3183473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a035c752cff624a591564d260d7ffbc52cd6ed0a4328066a48f6b5ca532e3150`

```dockerfile
```

-	Layers:
	-	`sha256:eb312aad7ee24cb5eba9e513bf0739603f8b1615cd095c4aa067cba29cafdadb`  
		Last Modified: Thu, 31 Oct 2024 23:00:20 GMT  
		Size: 3.2 MB (3166073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:155e2cf530836bc26f1db67554392ece6dd15b775daaed0fecf541e11c889982`  
		Last Modified: Thu, 31 Oct 2024 23:00:20 GMT  
		Size: 17.4 KB (17400 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.14` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:6e7172d5985b9eb2d045ee69bda5129ec14bc887e57c4567f667d2d7b70790e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94971632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32bd6dc10e57b54baed4170ee7b74fb49f86e54cbabdaa71ea1f23622c841a5`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.3.14;     SWIPL_CHECKSUM=81f73e13afdb3a191bea9238730884a34222cf424f92fe1255d455ebbe127224;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a12bec5040e38e2a3fd6e76bc71d86a43b628b60cdfc3433840178d7ec515f3`  
		Last Modified: Tue, 12 Nov 2024 10:36:50 GMT  
		Size: 47.7 MB (47706414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbf84ecd6aadc86b9446ca9c5ec890064257d1dbc52a34b3dd914ccba43983`  
		Last Modified: Tue, 12 Nov 2024 10:36:49 GMT  
		Size: 18.1 MB (18107862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.14` - unknown; unknown

```console
$ docker pull swipl@sha256:93322623f292a146e5c0181590059e0244c010487bb75a7350adddbf5734e02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b632aefb25ade1348d4444e92b597854808291ab999c2f1079ef060725375f`

```dockerfile
```

-	Layers:
	-	`sha256:a07132287baa7ebd7c562842f40831b0d6ef8970d4ecc17f551b0a5782f5d5b5`  
		Last Modified: Tue, 12 Nov 2024 10:36:49 GMT  
		Size: 3.2 MB (3167576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16f523ac212951c6b08693e259107e2744ec9370ed38241b04d17e2960c25ce1`  
		Last Modified: Tue, 12 Nov 2024 10:36:48 GMT  
		Size: 17.6 KB (17606 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:latest`

```console
$ docker pull swipl@sha256:3091a6fbc589a4f34f80922b6b30b94233d9d42641466affdbf456d61f8b1c25
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
$ docker pull swipl@sha256:d9604dd73e5ef74d47af16f81a220456ce3daf6eace23a337771bc77cd233767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97061204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c03dedfe237b8eeb38b996b33a59bb00abdbb6acb9b59b5e7c20e301d82cf6`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.3.14;     SWIPL_CHECKSUM=81f73e13afdb3a191bea9238730884a34222cf424f92fe1255d455ebbe127224;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab05e7d2325e60000bbeb41e0be8a5a54d36cf40706a935ebcc6a398bc0bbf25`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 49.2 MB (49222850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6ff44cd7c96d81ac1b20bd5fcd182566f3dad1a75011e2df01f39f095bf4df`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 18.7 MB (18710359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:f63cee6056bbc0a87ee242064514eaf01c73bc24551b7d4d6c391defd9e632bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3184748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa48357424401ec6f748b5cd5a3dd7629b32972258f3ca951e5d59180a3da33f`

```dockerfile
```

-	Layers:
	-	`sha256:cac160fecae5b1fd0a8a20e9c0914007c1d849e2f14dc65af181bbd4b0d2761d`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 3.2 MB (3167237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c750cf1f1e83279ff3b5e01940ba45d326a1769620d254737eaa5f1c175876e3`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 17.5 KB (17511 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:f390b062c647d2f6ce9b7c4a45beafbc9ae95d5f4d79aadb2bd600459ef2a7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82776846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99df0c5d7302f9c54af3fa0f82c235d2ff8b866afe4c86198b90c92991af928c`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.3.14;     SWIPL_CHECKSUM=81f73e13afdb3a191bea9238730884a34222cf424f92fe1255d455ebbe127224;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d737c752fb77e2ad5236d232ab5a86ea38bcdb521b3ab893a6fa979c8c5966b8`  
		Last Modified: Fri, 18 Oct 2024 02:13:19 GMT  
		Size: 43.7 MB (43723347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ff220951c029e0a9477c0dc8b3fc5421d45c3baf70aad14ca3a2dff64ce1c3`  
		Last Modified: Thu, 31 Oct 2024 23:00:21 GMT  
		Size: 14.3 MB (14335302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:36c2c0a9b3bd8250f447710e22d3f6ab4f25255ed47da7353016469e782e227c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3183473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a035c752cff624a591564d260d7ffbc52cd6ed0a4328066a48f6b5ca532e3150`

```dockerfile
```

-	Layers:
	-	`sha256:eb312aad7ee24cb5eba9e513bf0739603f8b1615cd095c4aa067cba29cafdadb`  
		Last Modified: Thu, 31 Oct 2024 23:00:20 GMT  
		Size: 3.2 MB (3166073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:155e2cf530836bc26f1db67554392ece6dd15b775daaed0fecf541e11c889982`  
		Last Modified: Thu, 31 Oct 2024 23:00:20 GMT  
		Size: 17.4 KB (17400 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:6e7172d5985b9eb2d045ee69bda5129ec14bc887e57c4567f667d2d7b70790e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94971632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32bd6dc10e57b54baed4170ee7b74fb49f86e54cbabdaa71ea1f23622c841a5`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.3.14;     SWIPL_CHECKSUM=81f73e13afdb3a191bea9238730884a34222cf424f92fe1255d455ebbe127224;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a12bec5040e38e2a3fd6e76bc71d86a43b628b60cdfc3433840178d7ec515f3`  
		Last Modified: Tue, 12 Nov 2024 10:36:50 GMT  
		Size: 47.7 MB (47706414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbf84ecd6aadc86b9446ca9c5ec890064257d1dbc52a34b3dd914ccba43983`  
		Last Modified: Tue, 12 Nov 2024 10:36:49 GMT  
		Size: 18.1 MB (18107862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:93322623f292a146e5c0181590059e0244c010487bb75a7350adddbf5734e02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b632aefb25ade1348d4444e92b597854808291ab999c2f1079ef060725375f`

```dockerfile
```

-	Layers:
	-	`sha256:a07132287baa7ebd7c562842f40831b0d6ef8970d4ecc17f551b0a5782f5d5b5`  
		Last Modified: Tue, 12 Nov 2024 10:36:49 GMT  
		Size: 3.2 MB (3167576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16f523ac212951c6b08693e259107e2744ec9370ed38241b04d17e2960c25ce1`  
		Last Modified: Tue, 12 Nov 2024 10:36:48 GMT  
		Size: 17.6 KB (17606 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:stable`

```console
$ docker pull swipl@sha256:94e9188aee2e42c08758cf9e379493eca790e9b08f1687965b03f58f0e079ccd
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
$ docker pull swipl@sha256:9d88196372ae372366c3521e128ce53d294ce9d18c4212d2f71dceaba4f93481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96896551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d36b32fd16c03219714ae384c3f80c0c6856019d2d3b111554e8d608be4b3dc`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.2.8;     SWIPL_CHECKSUM=b331637a57c913c49edcfcb10ddcf6c031278ce93d2411d54542778531abb5c7;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03630e44222222e34a9b723b7ebdddaf0d55bbedbfda113c1cef30bbe06dbafe`  
		Last Modified: Tue, 12 Nov 2024 02:24:23 GMT  
		Size: 49.2 MB (49222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618ebb0d6203ef8afe7f315237fa04971cbecbfffe362caca2c375b2850cbfc1`  
		Last Modified: Tue, 12 Nov 2024 02:24:23 GMT  
		Size: 18.5 MB (18545882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:0e34b6884630329fbb2fdd982ddf1b3143ff7abbd46ecc0a13b1d16c02291562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3184740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2344c1a670c92b8e1a6258d684c204502bdc2902fae5f77de76d0d19bd672b77`

```dockerfile
```

-	Layers:
	-	`sha256:a31ecbc89b4dbdb7b4afedddda43a7bd363fb838af0ed8d6a03d18e5a83fe44a`  
		Last Modified: Tue, 12 Nov 2024 02:24:22 GMT  
		Size: 3.2 MB (3167233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2136514aad85ed501329dd609915e59b537ae41178e61efa73e1c541975ac6c9`  
		Last Modified: Tue, 12 Nov 2024 02:24:22 GMT  
		Size: 17.5 KB (17507 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:9b8d91ac38193908e70b29917dec0464e97b126c206d86b5fd31d9a78fc99d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82560059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4acad6b4a3d5c27b1d51cb4b6bbb6595ced07d8305662a1be130b2e313b16fe`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.2.8;     SWIPL_CHECKSUM=b331637a57c913c49edcfcb10ddcf6c031278ce93d2411d54542778531abb5c7;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d737c752fb77e2ad5236d232ab5a86ea38bcdb521b3ab893a6fa979c8c5966b8`  
		Last Modified: Fri, 18 Oct 2024 02:13:19 GMT  
		Size: 43.7 MB (43723347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba398d2029fc5d3f702fe99398d3e2d32d34245bb6188ab65c017811b36c6cb`  
		Last Modified: Wed, 23 Oct 2024 22:58:27 GMT  
		Size: 14.1 MB (14118515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:fd4b91dc09e2af07ae4454c26b6922dbe7109a711490b5c562a917d605f9c365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3183465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180b251363d33d8491d329591a062e87225deafe31f3036226aed34d75dda3df`

```dockerfile
```

-	Layers:
	-	`sha256:7973f13f4cc7c35f98d70a2f4ee83e1ad7d26f669ac9c5c510b1f8a4a4279961`  
		Last Modified: Thu, 31 Oct 2024 23:00:47 GMT  
		Size: 3.2 MB (3166069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da65cb1ef35fdf209d56f7c6830b6f73970a20782e2a44d57ee64e269dc89d0c`  
		Last Modified: Thu, 31 Oct 2024 23:00:47 GMT  
		Size: 17.4 KB (17396 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:c1dffbdd621d26db2705382efde17b701fc47c9f8cfaf615d5f97c1d639333cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94804611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84634ddb9071f382a213df9fd7c54243fc9438497747e24612a3d5f5dc6f9a5`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.2.8;     SWIPL_CHECKSUM=b331637a57c913c49edcfcb10ddcf6c031278ce93d2411d54542778531abb5c7;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a12bec5040e38e2a3fd6e76bc71d86a43b628b60cdfc3433840178d7ec515f3`  
		Last Modified: Tue, 12 Nov 2024 10:36:50 GMT  
		Size: 47.7 MB (47706414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f5f075eccffb4f018fcd03ed02d3fce251b3c6fdc8226d71899f6d9dadba8c`  
		Last Modified: Tue, 12 Nov 2024 10:43:20 GMT  
		Size: 17.9 MB (17940841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:cfcade3ab5f2e2ca9e5ec823c3472e96d15333beb541c2658bbbfab01af19fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102b4fb9dd32a29dc9ba98c58a1072478960babae012be47cca0c460098489f6`

```dockerfile
```

-	Layers:
	-	`sha256:55230ba367c34935362fdc38866c31ebcca5a1b1333916c4a92c2f772723dffc`  
		Last Modified: Tue, 12 Nov 2024 10:43:19 GMT  
		Size: 3.2 MB (3167572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e57fb79dcff598660520b1e0cbbc8c7bdf2424143a5b7383db60ff3ff1181b92`  
		Last Modified: Tue, 12 Nov 2024 10:43:18 GMT  
		Size: 17.6 KB (17602 bytes)  
		MIME: application/vnd.in-toto+json
