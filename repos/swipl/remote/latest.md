## `swipl:latest`

```console
$ docker pull swipl@sha256:f8fc8ce2a340ba1604c6b3ad1301a4b6a41035df18cc5d47889714c568949de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `swipl:latest` - linux; amd64

```console
$ docker pull swipl@sha256:285f284fb57a9683fb418a3b5321dfef59747519c4f0c9427c805e4fe045ad09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151590587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34dafb218a7fc893cd4c1c4ecdcc1e2cd98beb1924182ed1489ca52ece8610c4`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 17:07:33 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 19 Dec 2023 17:07:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtool     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos-3.9.0     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3-dev     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 17:07:57 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:15:41 GMT
RUN set -eux;     SWIPL_VER=9.1.19;     SWIPL_CHECKSUM=6f1abee4d03f4a683c6ea0394623f10e43ce55d4e0307a1731bc1a196139d1dc;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev libgeos-dev libspatialindex-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin space https://github.com/JanWielemaker/space.git 8ab230a67e2babb3e81fac043512a7de7f4593bf;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git e62d815b1fc392f2b8f80d0d17479a1f55e0c573;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git 48a46160bc2768182be757ab179c26935db41de7;     apt-get purge -y --auto-remove $BUILD_DEPS
# Tue, 19 Dec 2023 17:15:42 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14838b12221ada2e01b3a849c9c75b623be091ac0124e9d26329d9de80e3dcf8`  
		Last Modified: Tue, 19 Dec 2023 17:24:27 GMT  
		Size: 102.0 MB (101968021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570490a04bfd3147688b7543d3ff638d181905b3dbb39c05ae09fa890c51df5e`  
		Last Modified: Tue, 19 Dec 2023 17:24:16 GMT  
		Size: 18.2 MB (18204693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:dcdf742d75d77c2215c41d3c78a9b2e59ede76a67449202b10ea6841af7f8ba9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (82974243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc74b768e0d47aa86ad6a63abae8fe9a02152427cd42a49455e5a3fffa0c6a6`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:30:53 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 11 Jan 2024 19:31:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:31:33 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 19:36:42 GMT
RUN set -eux;     SWIPL_VER=9.1.21;     SWIPL_CHECKSUM=8536acab1892edb7db3fa46df439fc19158a8448341af98a33c6359b312ef705;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS
# Thu, 11 Jan 2024 19:36:43 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3607d03c783b40ab4460e0f95200431bf692d64f9b21a3cc09237ebb17484b1`  
		Last Modified: Thu, 11 Jan 2024 19:48:26 GMT  
		Size: 43.7 MB (43703910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e98f30ce3710f96246aa6f7ddad6c3a05ebe5ba811d411d2ac5b3d2a859df1`  
		Last Modified: Thu, 11 Jan 2024 19:48:20 GMT  
		Size: 14.6 MB (14552207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:f880d86f7bc1d938b9728308a263cdf969437493cba79dcff344296b1083dce9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94563061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e05753cc77dfb53e20029d4fc564b3f9f207b5dec30a8e536caa80a2645e0d4`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:32:49 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 11 Jan 2024 08:33:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:33:05 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 08:38:24 GMT
RUN set -eux;     SWIPL_VER=9.1.21;     SWIPL_CHECKSUM=8536acab1892edb7db3fa46df439fc19158a8448341af98a33c6359b312ef705;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS
# Thu, 11 Jan 2024 08:38:24 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4445f3d05ace346635e1aebad518a151bef9bd9820894756ea53b74bc6df2bea`  
		Last Modified: Thu, 11 Jan 2024 08:44:32 GMT  
		Size: 47.7 MB (47679741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097711a8f4bef0388bcd8bfedaec56f08d8515353094b33ed89e6b3522ff430`  
		Last Modified: Thu, 11 Jan 2024 08:44:29 GMT  
		Size: 17.7 MB (17725985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
