## `swipl:latest`

```console
$ docker pull swipl@sha256:3795310d9c33cd03f5215403c46e9fc9943ede2898b3b4c45640c663acc72dfa
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
$ docker pull swipl@sha256:f789ca0ffe5c659b89a3544cd48bd9e06f6a4821909ab2d938786fa539806c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97023100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0777a14981e84cd676578770b091449ba5d9985feb2aaeb1ad31995f6fc1459d`
-	Default Command: `["swipl"]`

```dockerfile
# Sun, 08 Sep 2024 08:35:01 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["bash"]
# Sun, 08 Sep 2024 08:35:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sun, 08 Sep 2024 08:35:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 08:35:01 GMT
RUN set -eux;     SWIPL_VER=9.3.11;     SWIPL_CHECKSUM=b8bffac671ee031ee34d033c168fed0a6f4ea0a906e2a13f5a19f00b59cd4b55;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1deec53db446ab1709ef3aa348656dba6b9dc509b13f867952a832ff22777a`  
		Last Modified: Fri, 27 Sep 2024 06:29:32 GMT  
		Size: 49.2 MB (49221421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aae806d14b17be1cf23518674a1f5bf906babdce758eba51caae703f5814a8`  
		Last Modified: Fri, 27 Sep 2024 06:29:31 GMT  
		Size: 18.7 MB (18675403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:fe5d3f699a02942512bc8dae5156241c566359f1960c461b43d0859dc1077735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b62cfea7380055f1ca2170440f23a9ea3d685e9d1c8a5f1377e2e84261ccc2b`

```dockerfile
```

-	Layers:
	-	`sha256:b931cbeaf4536f79ba729f06b90a6d0a61bfa150848e425079bc08f9393102f3`  
		Last Modified: Fri, 27 Sep 2024 06:29:31 GMT  
		Size: 3.1 MB (3144010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:732231b17e5a71cc9c681a9f31c415c16212ac782e75c5ade7b810a844401b4c`  
		Last Modified: Fri, 27 Sep 2024 06:29:30 GMT  
		Size: 17.3 KB (17299 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:0ce869d3b60e1f4ec28b6eeeaeae674d2ab0f7814fe9b9120139c75e1f35d1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82738087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad3aac2c6692ec8aebb750947f6c191d3b8efd305c894ceb0314408c123edfa`
-	Default Command: `["swipl"]`

```dockerfile
# Sun, 08 Sep 2024 08:35:01 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["bash"]
# Sun, 08 Sep 2024 08:35:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sun, 08 Sep 2024 08:35:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 08:35:01 GMT
RUN set -eux;     SWIPL_VER=9.3.11;     SWIPL_CHECKSUM=b8bffac671ee031ee34d033c168fed0a6f4ea0a906e2a13f5a19f00b59cd4b55;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8d771fa51d762ca800a343818d5089f10d021da236680cc8107ca03281d773`  
		Last Modified: Fri, 27 Sep 2024 18:46:50 GMT  
		Size: 43.7 MB (43723801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a551053fc0e4035d9613521d16b45478eec4314eec7f5d3610e6c08bb2a335`  
		Last Modified: Fri, 27 Sep 2024 18:46:49 GMT  
		Size: 14.3 MB (14296141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:c5a04391b1ce65cc79766054723b4d9b8a72cd5a81fd95340cd2cd59fcf6c7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3163898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14996b6f2d0f9fc226dc7ba3d65b3b62d6874cba200763a0f64f0aef4c362aa1`

```dockerfile
```

-	Layers:
	-	`sha256:cce116daf4fccefaf7d041551b8731fdd4d0afe40235886d7c09fdc527f7ad18`  
		Last Modified: Fri, 27 Sep 2024 18:46:49 GMT  
		Size: 3.1 MB (3146532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6c9ddfde98d6c0fa052a5b3764e5f326ca3586bb0a1ba78c24812ca5c6da779`  
		Last Modified: Fri, 27 Sep 2024 18:46:48 GMT  
		Size: 17.4 KB (17366 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:96d7f7bd8ed4bbb48d8e12f872efee0fb350493c3ca6b35adf735ef671fd9b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94931752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3102e99096d4a17624fb4d2f188df07cf96fbae5cbcadced1f4ba6020a2b693b`
-	Default Command: `["swipl"]`

```dockerfile
# Sun, 08 Sep 2024 08:35:01 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["bash"]
# Sun, 08 Sep 2024 08:35:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sun, 08 Sep 2024 08:35:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 08:35:01 GMT
RUN set -eux;     SWIPL_VER=9.3.11;     SWIPL_CHECKSUM=b8bffac671ee031ee34d033c168fed0a6f4ea0a906e2a13f5a19f00b59cd4b55;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04be04db0f19489d1a2e0da09b7d8d2de707ee700e26000abcee5d02fd0df4bb`  
		Last Modified: Fri, 27 Sep 2024 23:46:59 GMT  
		Size: 47.7 MB (47713641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c408468d04662284a3ebd37bb6e409907125e77e46ade000e23c095fa76c63af`  
		Last Modified: Fri, 27 Sep 2024 23:46:58 GMT  
		Size: 18.1 MB (18061742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:e32a9d80d6ca9637ddc52bbae3b47bdc76d39eb2e6905a5a7ceba30dd465644a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d591e5c69236198566629e8396459631487a5041c7bb88e6110b66b459f09e9`

```dockerfile
```

-	Layers:
	-	`sha256:20175c78fb32b2e1b300caf0219a0ffd886151df5be08289543ad3298bbac2d1`  
		Last Modified: Fri, 27 Sep 2024 23:46:58 GMT  
		Size: 3.1 MB (3144349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f280cd7dd5656465aa72c9a9ba77338595d846f470a7c4c9986e9c60cd02f91`  
		Last Modified: Fri, 27 Sep 2024 23:46:57 GMT  
		Size: 17.6 KB (17584 bytes)  
		MIME: application/vnd.in-toto+json
