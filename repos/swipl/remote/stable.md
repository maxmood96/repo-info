## `swipl:stable`

```console
$ docker pull swipl@sha256:377458e5502813d7c10f7fcd56ab8dfd538e5d6f397b80872c099791d2c9cd31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `swipl:stable` - linux; amd64

```console
$ docker pull swipl@sha256:bcc4728f8572ce4917716cf3cd907a7eccf5cfa4a2f91d20e4d77d308c5ae230
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78796298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c730f3fd9585aef165aa83424a994c45f73521504b1fa77f8a8ef807a02847`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 19:57:56 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 21 Nov 2023 20:05:59 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos-3.9.0     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 20:06:00 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:13:27 GMT
RUN set -eux;     SWIPL_VER=9.0.4;     SWIPL_CHECKSUM=feb2815a51d34fa81cb34e8149830405935a7e1d1c1950461239750baa8b49f0;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev libgeos-dev libspatialindex-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git 8ab230a67e2babb3e81fac043512a7de7f4593bf;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 634c31e928e2a5100fbcfd26c21cd32eeb6bf369;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git 48a46160bc2768182be757ab179c26935db41de7;     apt-get purge -y --auto-remove $BUILD_DEPS
# Tue, 21 Nov 2023 20:13:27 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3205202d158e94ef3e71889bf00465042d87b338d936093a29d07487b97a90`  
		Last Modified: Tue, 21 Nov 2023 20:14:16 GMT  
		Size: 30.0 MB (29998925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abd54ed94e242d48e26bd47b20e256d4acd8c79396a4ac491c409baa0f3bf84`  
		Last Modified: Tue, 21 Nov 2023 20:14:15 GMT  
		Size: 17.4 MB (17379549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:6b6316626b5354e85a71f557a60a5dee52a6ff373c4cee4c6f95185fbdae0703
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66621414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85dea93ed5830d877a7ba1aa598da833381456c731c581fc8dec27b08a8e5d72`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 15 Nov 2022 03:43:25 GMT
ADD file:1b5c939bd2a35667d7fc44c3009a56ed92a932f512a73df1617dec6ccbd6e6b1 in / 
# Tue, 15 Nov 2022 03:43:26 GMT
CMD ["bash"]
# Wed, 16 Nov 2022 09:26:34 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 16 Nov 2022 09:33:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-3.9.0     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Nov 2022 09:33:50 GMT
ENV LANG=C.UTF-8
# Wed, 16 Nov 2022 09:36:07 GMT
RUN set -eux;     SWIPL_VER=8.4.2;     SWIPL_CHECKSUM=be21bd3d6d1c9f3e9b0d8947ca6f3f5fd56922a3819cae03251728f3e1a6f389;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev libgeos-dev libspatialindex-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git fce744508d475768d11f4e0f3c81a450ff5a9c53;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git f110766ee97cfbc6fddd4c33b7238f00e76ecc18;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git 48a46160bc2768182be757ab179c26935db41de7;     apt-get purge -y --auto-remove $BUILD_DEPS
# Wed, 16 Nov 2022 09:36:07 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:fd18d0201d0ce0c5e103902d894f5d601fc5dde76688aa7dae786840141d23e4`  
		Last Modified: Tue, 15 Nov 2022 03:50:11 GMT  
		Size: 26.6 MB (26576195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b52f6c75f264431d3f1870bdb1d99634d10792d0a28241fc012af0bf9b78a4`  
		Last Modified: Wed, 16 Nov 2022 09:36:33 GMT  
		Size: 26.8 MB (26832335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c08b90359f5b2368e054491741a4394cd400cdf786c9145671f200bcc15b74`  
		Last Modified: Wed, 16 Nov 2022 09:36:31 GMT  
		Size: 13.2 MB (13212884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:e0c9290f5c318e13d3047f3edf52fcadcd1ee79a432f35a53ab334973c240094
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76039954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960fc400ff6429d417223df5cfc5d5e44cb947e95a054f91a25679bcdc22eea3`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:10:51 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 19 Dec 2023 11:16:37 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos-3.9.0     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:16:38 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 11:21:59 GMT
RUN set -eux;     SWIPL_VER=9.0.4;     SWIPL_CHECKSUM=feb2815a51d34fa81cb34e8149830405935a7e1d1c1950461239750baa8b49f0;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev libgeos-dev libspatialindex-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git 8ab230a67e2babb3e81fac043512a7de7f4593bf;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 634c31e928e2a5100fbcfd26c21cd32eeb6bf369;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git 48a46160bc2768182be757ab179c26935db41de7;     apt-get purge -y --auto-remove $BUILD_DEPS
# Tue, 19 Dec 2023 11:22:00 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab51e0b14d34df13726cf410b7b8ca62ba5ae60b6405b612296016ffe813d12`  
		Last Modified: Tue, 19 Dec 2023 11:22:35 GMT  
		Size: 29.1 MB (29069076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0936e2e0de635b4559b92cf26a1010474c0e09176082d9f9ac6c4682ec9a6534`  
		Last Modified: Tue, 19 Dec 2023 11:22:34 GMT  
		Size: 16.9 MB (16906826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
