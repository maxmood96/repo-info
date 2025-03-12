<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:9.2.9`](#swipl929)
-	[`swipl:9.3.21`](#swipl9321)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:9.2.9`

```console
$ docker pull swipl@sha256:3e7f8782776788d5dea2d8ff94136f6348744e19b624b3f777c3c8c484458d13
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
$ docker pull swipl@sha256:10b8d9313bd287f404d76b20c570a4e4e2a5fac6cfcd7d9962eeffa46aaeb731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95968699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241709c908fd79219a642a7ffe7699b8533057e64562dbce44f4feb17b99429f`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 07 Feb 2025 09:42:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Fri, 07 Feb 2025 09:42:02 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 07 Feb 2025 09:42:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 09:42:02 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbd0c7e5307eeaf20c3daeec0c326d9766861c0f39340e927c17db22b6adb8c`  
		Last Modified: Tue, 25 Feb 2025 02:25:11 GMT  
		Size: 49.2 MB (49219523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b96b9d36b4dbe95d05737829cec7fd497093ab5611b0111241cff8b8dc6cafc`  
		Last Modified: Tue, 25 Feb 2025 02:25:10 GMT  
		Size: 18.5 MB (18529875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.9` - unknown; unknown

```console
$ docker pull swipl@sha256:6b0c6cfb2652a71fb094b7f53e07e4b1ec92b28c082920e95e7c11c64fb094e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd92056cb0c4298789ac6c0337d4d9643dae5f8bc47453906176b7773f7c333`

```dockerfile
```

-	Layers:
	-	`sha256:b2f2dfc7927b9259edc2ff2abab60608a9d0a6ceb6984b11af008759c4688876`  
		Last Modified: Tue, 25 Feb 2025 02:25:10 GMT  
		Size: 3.2 MB (3157154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f564a0f29d6117d04ae773ad5b5b0082fe2fe42cf146e3df3cd0724c1d893b6b`  
		Last Modified: Tue, 25 Feb 2025 02:25:10 GMT  
		Size: 17.5 KB (17507 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.9` - linux; arm variant v7

```console
$ docker pull swipl@sha256:12532b5015df4a9a7a905bf4337d644f95de1742d60044006c8828a5d2197e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81753873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8907e2cd76b02387f87e0e60a392d6b58cebabdab1baa059346882185774c91`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 07 Feb 2025 09:42:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Fri, 07 Feb 2025 09:42:02 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 07 Feb 2025 09:42:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 09:42:02 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305e8a0576b2f4219a57d8b5c45a1208703d7a74ca0c139b4afaecf9b3a9c7f4`  
		Last Modified: Tue, 25 Feb 2025 07:05:30 GMT  
		Size: 43.7 MB (43734854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f696c16340fd522c93ffcff313a1ee563f4eaf00b6d8b9104b21b0a130e320`  
		Last Modified: Tue, 25 Feb 2025 07:08:15 GMT  
		Size: 14.1 MB (14099285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.9` - unknown; unknown

```console
$ docker pull swipl@sha256:b833c2c79dfb73feb7c430e2cb75a2667d49a10b9dd204280e41171262cb6cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548de6d308583bd3e404fb399b55a7039abf435dd25de1933f9c6bfa948fc81c`

```dockerfile
```

-	Layers:
	-	`sha256:843f4c874c97e614f07c87e158e75459536f2745d63bcfaae02260c52188a9a6`  
		Last Modified: Tue, 25 Feb 2025 07:08:15 GMT  
		Size: 3.2 MB (3160902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa63f53a120de1876545e0cb331495bec72bb806e28605ded3030e1f0415016c`  
		Last Modified: Tue, 25 Feb 2025 07:08:14 GMT  
		Size: 17.6 KB (17579 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.9` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:18eab6138ce8b3aa1d2ae0247104ce4c97027c94403334ca0187bfd1ea5b246d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93698713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a2bae18ae1cfcf7cbbe5a6d212437b60dae91f345c8113ca12bee76ecf84d9`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 07 Feb 2025 09:42:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Feb 2025 09:42:02 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 07 Feb 2025 09:42:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 09:42:02 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fec9a977601a412a7fefeba409da4e206a08c097549eef3cf355126fd2ef439`  
		Last Modified: Tue, 25 Feb 2025 05:27:22 GMT  
		Size: 47.7 MB (47713656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddad5aa83e7a8888b2ccf1c24a28ee7938fadc683e05b548138983e3a49e0205`  
		Last Modified: Tue, 25 Feb 2025 05:33:47 GMT  
		Size: 17.9 MB (17936632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.9` - unknown; unknown

```console
$ docker pull swipl@sha256:7fcd8e6152bc958582cdaedc366e765065942299ffa0ce18f2d30bf67aeee1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f174556170ca84e038cd90d2e5b415d58a41a616db132b6996fd6ce1bbe30e`

```dockerfile
```

-	Layers:
	-	`sha256:c7dbe93d2b599f37abb42d9b034d656da145198df133400abacfc579c25ad4d5`  
		Last Modified: Tue, 25 Feb 2025 05:33:47 GMT  
		Size: 3.2 MB (3162396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37780778e3b87a424cfff627ba649aa707859191b2d4f61ff076ca4fda876020`  
		Last Modified: Tue, 25 Feb 2025 05:33:46 GMT  
		Size: 17.6 KB (17602 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:9.3.21`

```console
$ docker pull swipl@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `swipl:latest`

```console
$ docker pull swipl@sha256:d5c0794dc20765b5a2a568cd07a1bd20b494c86dbf52922510a3682666882dee
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
$ docker pull swipl@sha256:edfd3a0490a230ac6175bbdfbca0cf4829eea93b5f850665189c3e389f7d35b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96212427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939b1e60fdc567e24c5d9e4169c5a03a4e1052bc6cb50c3b61e1ce1ecd1f88d9`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 07 Feb 2025 09:42:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Fri, 07 Feb 2025 09:42:02 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 07 Feb 2025 09:42:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 09:42:02 GMT
RUN set -eux;     SWIPL_VER=9.3.20;     SWIPL_CHECKSUM=81cae918f75778c285bbecfc2b17c7117b574238e00213043a1fa0022acc36d6;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b910a50fd8e8e9344fa583ae54bf515453a94d419e58b4d40b524eb712764d34`  
		Last Modified: Tue, 25 Feb 2025 02:25:29 GMT  
		Size: 49.2 MB (49219217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cfc6076351d70722fc610c9beb8193934c98e7d2a1ab77a0e72583389a2a0a`  
		Last Modified: Tue, 25 Feb 2025 02:25:27 GMT  
		Size: 18.8 MB (18773909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:c871a8ffcbb86d7832839c913b322e73eac56baa7c28a24f879ecd4df8a41c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808f067a479bc01d7cac153223540f1ffea5f1afcbb6b73d1e826dba2898f439`

```dockerfile
```

-	Layers:
	-	`sha256:a016014d4e788924317cc8bc9dd3bc4cdd87c3e0715cd1b7bf2300e70b24713c`  
		Last Modified: Tue, 25 Feb 2025 02:25:27 GMT  
		Size: 3.2 MB (3157158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96f60e68bbce53d87d6eca3c936ab9ca8610f156ccdcce802efaf5fdce7723b6`  
		Last Modified: Tue, 25 Feb 2025 02:25:26 GMT  
		Size: 17.5 KB (17511 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:77110e0bc9b9c62da4b14ca55ee03f9bac5d5625876569bee11506ae5da77341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82044725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37106ad3ef1edbd5fb4bff79d571a12635339094d7566fedee87a2d6ab870dd4`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 07 Feb 2025 09:42:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Fri, 07 Feb 2025 09:42:02 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 07 Feb 2025 09:42:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 09:42:02 GMT
RUN set -eux;     SWIPL_VER=9.3.20;     SWIPL_CHECKSUM=81cae918f75778c285bbecfc2b17c7117b574238e00213043a1fa0022acc36d6;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305e8a0576b2f4219a57d8b5c45a1208703d7a74ca0c139b4afaecf9b3a9c7f4`  
		Last Modified: Tue, 25 Feb 2025 07:05:30 GMT  
		Size: 43.7 MB (43734854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7d4e255dc1c97597a32e87c7b267c779220d0814d623fdaaf78b13fcf17bb5`  
		Last Modified: Tue, 25 Feb 2025 07:05:29 GMT  
		Size: 14.4 MB (14390137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:c8e0ba20f089186f33a3e34cddb8589058e3df5dd780bb6c3f92d9db3c69a935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb3009cfb83e458be86c816eacb373becda72de1b39f73bedde5681eecfca6e`

```dockerfile
```

-	Layers:
	-	`sha256:4d24060c45d6301c4684aa5e67ff59caed5c276f79011f660db0fdba3ef9a461`  
		Last Modified: Tue, 25 Feb 2025 07:05:29 GMT  
		Size: 3.2 MB (3160906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb2bd88e90b4f8a295c4de112cbdbd4d7fa0f14ebbd6b8b362f654f80066677`  
		Last Modified: Tue, 25 Feb 2025 07:05:28 GMT  
		Size: 17.6 KB (17583 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:cad61268dafce44708346401e0669d97003115770e6ab5f545ffefd5ac28b8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93931309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba6ee00dea687d8af6b5cc14156746fc787750f643db99611eb902d220770ed`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 07 Feb 2025 09:42:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Feb 2025 09:42:02 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 07 Feb 2025 09:42:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 09:42:02 GMT
RUN set -eux;     SWIPL_VER=9.3.20;     SWIPL_CHECKSUM=81cae918f75778c285bbecfc2b17c7117b574238e00213043a1fa0022acc36d6;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fec9a977601a412a7fefeba409da4e206a08c097549eef3cf355126fd2ef439`  
		Last Modified: Tue, 25 Feb 2025 05:27:22 GMT  
		Size: 47.7 MB (47713656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4057f6687a3cc84e07cd410237b05493813fd9d0d669c15299ede0110b315db0`  
		Last Modified: Tue, 25 Feb 2025 05:27:18 GMT  
		Size: 18.2 MB (18169228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:bfa87afb5ba7f98885dca66be529620f940cb26c56142244cd62475de396f49c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0b9986a6be921b52e27ad257efd7665ba5b6b45d56bc56ffce43735ddc3b81`

```dockerfile
```

-	Layers:
	-	`sha256:2698e4478f1dbd10835e32dc513c1ab79e4a2b2e05c95ed8782af3b5d9cc394a`  
		Last Modified: Tue, 25 Feb 2025 05:27:18 GMT  
		Size: 3.2 MB (3162400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209ac165858c3d0837a24b0f6dc539b65bd4104f6812b2bdaaedada5268ec652`  
		Last Modified: Tue, 25 Feb 2025 05:27:18 GMT  
		Size: 17.6 KB (17606 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:stable`

```console
$ docker pull swipl@sha256:3e7f8782776788d5dea2d8ff94136f6348744e19b624b3f777c3c8c484458d13
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
$ docker pull swipl@sha256:10b8d9313bd287f404d76b20c570a4e4e2a5fac6cfcd7d9962eeffa46aaeb731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95968699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241709c908fd79219a642a7ffe7699b8533057e64562dbce44f4feb17b99429f`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 07 Feb 2025 09:42:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Fri, 07 Feb 2025 09:42:02 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 07 Feb 2025 09:42:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 09:42:02 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbd0c7e5307eeaf20c3daeec0c326d9766861c0f39340e927c17db22b6adb8c`  
		Last Modified: Tue, 25 Feb 2025 02:25:11 GMT  
		Size: 49.2 MB (49219523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b96b9d36b4dbe95d05737829cec7fd497093ab5611b0111241cff8b8dc6cafc`  
		Last Modified: Tue, 25 Feb 2025 02:25:10 GMT  
		Size: 18.5 MB (18529875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:6b0c6cfb2652a71fb094b7f53e07e4b1ec92b28c082920e95e7c11c64fb094e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd92056cb0c4298789ac6c0337d4d9643dae5f8bc47453906176b7773f7c333`

```dockerfile
```

-	Layers:
	-	`sha256:b2f2dfc7927b9259edc2ff2abab60608a9d0a6ceb6984b11af008759c4688876`  
		Last Modified: Tue, 25 Feb 2025 02:25:10 GMT  
		Size: 3.2 MB (3157154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f564a0f29d6117d04ae773ad5b5b0082fe2fe42cf146e3df3cd0724c1d893b6b`  
		Last Modified: Tue, 25 Feb 2025 02:25:10 GMT  
		Size: 17.5 KB (17507 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:12532b5015df4a9a7a905bf4337d644f95de1742d60044006c8828a5d2197e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81753873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8907e2cd76b02387f87e0e60a392d6b58cebabdab1baa059346882185774c91`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 07 Feb 2025 09:42:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Fri, 07 Feb 2025 09:42:02 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 07 Feb 2025 09:42:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 09:42:02 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305e8a0576b2f4219a57d8b5c45a1208703d7a74ca0c139b4afaecf9b3a9c7f4`  
		Last Modified: Tue, 25 Feb 2025 07:05:30 GMT  
		Size: 43.7 MB (43734854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f696c16340fd522c93ffcff313a1ee563f4eaf00b6d8b9104b21b0a130e320`  
		Last Modified: Tue, 25 Feb 2025 07:08:15 GMT  
		Size: 14.1 MB (14099285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:b833c2c79dfb73feb7c430e2cb75a2667d49a10b9dd204280e41171262cb6cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548de6d308583bd3e404fb399b55a7039abf435dd25de1933f9c6bfa948fc81c`

```dockerfile
```

-	Layers:
	-	`sha256:843f4c874c97e614f07c87e158e75459536f2745d63bcfaae02260c52188a9a6`  
		Last Modified: Tue, 25 Feb 2025 07:08:15 GMT  
		Size: 3.2 MB (3160902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa63f53a120de1876545e0cb331495bec72bb806e28605ded3030e1f0415016c`  
		Last Modified: Tue, 25 Feb 2025 07:08:14 GMT  
		Size: 17.6 KB (17579 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:18eab6138ce8b3aa1d2ae0247104ce4c97027c94403334ca0187bfd1ea5b246d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93698713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a2bae18ae1cfcf7cbbe5a6d212437b60dae91f345c8113ca12bee76ecf84d9`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 07 Feb 2025 09:42:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Feb 2025 09:42:02 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Fri, 07 Feb 2025 09:42:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 09:42:02 GMT
RUN set -eux;     SWIPL_VER=9.2.9;     SWIPL_CHECKSUM=53f428e2d9bbdf30e53b06c9c42def9a13ff82fc36a111d410fc8b0bc889ee2d;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Fri, 07 Feb 2025 09:42:02 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fec9a977601a412a7fefeba409da4e206a08c097549eef3cf355126fd2ef439`  
		Last Modified: Tue, 25 Feb 2025 05:27:22 GMT  
		Size: 47.7 MB (47713656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddad5aa83e7a8888b2ccf1c24a28ee7938fadc683e05b548138983e3a49e0205`  
		Last Modified: Tue, 25 Feb 2025 05:33:47 GMT  
		Size: 17.9 MB (17936632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:7fcd8e6152bc958582cdaedc366e765065942299ffa0ce18f2d30bf67aeee1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f174556170ca84e038cd90d2e5b415d58a41a616db132b6996fd6ce1bbe30e`

```dockerfile
```

-	Layers:
	-	`sha256:c7dbe93d2b599f37abb42d9b034d656da145198df133400abacfc579c25ad4d5`  
		Last Modified: Tue, 25 Feb 2025 05:33:47 GMT  
		Size: 3.2 MB (3162396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37780778e3b87a424cfff627ba649aa707859191b2d4f61ff076ca4fda876020`  
		Last Modified: Tue, 25 Feb 2025 05:33:46 GMT  
		Size: 17.6 KB (17602 bytes)  
		MIME: application/vnd.in-toto+json
