<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:10.0.2`](#swipl1002)
-	[`swipl:10.1.8`](#swipl1018)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:10.0.2`

```console
$ docker pull swipl@sha256:26cf6a0174374ebb7cf70a356ae7cace36181b25d522fca64354e094f30593fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:10.0.2` - linux; amd64

```console
$ docker pull swipl@sha256:c164a5248a9677ae9a3f6e797afa6095377cab7d0e8bd0d8b420d0558c3ca3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99111287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e459c7118a667623e0089546208533379dd97e811563e3df7ac77a1ca8e4a76`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:18:33 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 19 May 2026 23:18:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:24:55 GMT
RUN set -eux;     SWIPL_VER=10.0.2;     SWIPL_CHECKSUM=e42cc098f7b8a6051c4f79a99b55162d467098aba60f69649bdc7583f0734b57;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git d1463581484ec794d92700f88cee431b257f33dc;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 19 May 2026 23:24:55 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc13a076afde065de391de9cda4c74c42d81d022bda16e5ff64a247fa876f21`  
		Last Modified: Tue, 19 May 2026 23:25:10 GMT  
		Size: 49.2 MB (49238372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b970190cd19c0849f3a49f5d3530fdb6f01d3ef8728946f22c26fdff49616c02`  
		Last Modified: Tue, 19 May 2026 23:25:08 GMT  
		Size: 21.6 MB (21639372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:10.0.2` - unknown; unknown

```console
$ docker pull swipl@sha256:00046a56ec4e20fac0fb72f444886050d6210814309630a8f52c8180d7221ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952efc366917427f9d7160cbcc0b0f9d6ae348f61efbde1793519accca157cf4`

```dockerfile
```

-	Layers:
	-	`sha256:564827b346a619c36f6f60d8c8cac8dffed1e966ae5631a70e97901669138c2a`  
		Last Modified: Tue, 19 May 2026 23:25:08 GMT  
		Size: 3.3 MB (3326564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d17a7f863a8ed1b5aba04f579701c137eb98947eecf64cc883cdc8fcf41912`  
		Last Modified: Tue, 19 May 2026 23:25:07 GMT  
		Size: 17.9 KB (17886 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:10.0.2` - linux; arm variant v7

```console
$ docker pull swipl@sha256:67f7d113bc509a86310239970929de5c61477cfda4bb2017514d49deac30a656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84830307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ee14451a76e628099c36561c12d17aa48c37c535200a12be13950827e94c61`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:01:22 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 20 May 2026 00:01:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:01:22 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:03:55 GMT
RUN set -eux;     SWIPL_VER=10.0.2;     SWIPL_CHECKSUM=e42cc098f7b8a6051c4f79a99b55162d467098aba60f69649bdc7583f0734b57;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git d1463581484ec794d92700f88cee431b257f33dc;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 20 May 2026 00:03:55 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245337099e11728a994e85cbddcbcf2a1c0f9e5420fc6607e06dbfc3e7327522`  
		Last Modified: Wed, 20 May 2026 00:04:07 GMT  
		Size: 43.8 MB (43751910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3511bcaa3591068576d32ca9802f8cab19088bb33c55e6dbea732ce3dcb15153`  
		Last Modified: Wed, 20 May 2026 00:04:06 GMT  
		Size: 17.1 MB (17136754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:10.0.2` - unknown; unknown

```console
$ docker pull swipl@sha256:c4bb60ee44f12f13ca31ccc71849e68f58d8935513a3524e43ed387286f4632d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfddd5aa39cdede9abfc2aa440ed8465dffda478a6869577f104972d00a6f79e`

```dockerfile
```

-	Layers:
	-	`sha256:d2a2387cedee942d38c592b810ee0041ecf6c4453f606c3d188d00a6da9714aa`  
		Last Modified: Wed, 20 May 2026 00:04:06 GMT  
		Size: 3.3 MB (3325410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cd11ff1380d45f63153618daad1072c214109d2e72a3f754d41071213f2f5f6`  
		Last Modified: Wed, 20 May 2026 00:04:05 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:10.0.2` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:40995f8bf0152a304791f08f9a244f734a9735ba68c4c824c581d4a7bbd607e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96914984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527685fab3f5cba5668d852bddab31b19694a298d21fae18a7aabbab239a58cd`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:21:37 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 19 May 2026 23:21:37 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:21:37 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:27:33 GMT
RUN set -eux;     SWIPL_VER=10.0.2;     SWIPL_CHECKSUM=e42cc098f7b8a6051c4f79a99b55162d467098aba60f69649bdc7583f0734b57;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git d1463581484ec794d92700f88cee431b257f33dc;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 19 May 2026 23:27:33 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0886d6f0c4239984c1aca793add652a343e1c6b33a59a17a1d7676ed3d2076`  
		Last Modified: Tue, 19 May 2026 23:27:48 GMT  
		Size: 47.8 MB (47803276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4b6e132d5e678934d06dd9e655ad84913abcc5c6ea758d6be327154d6abfaf`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 21.0 MB (20996665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:10.0.2` - unknown; unknown

```console
$ docker pull swipl@sha256:fb331d3366123eef5802a408b00815928e39c16db87b4f9e40ea049305d7ee44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ceab182d7beddfcb95b87427ce50a748a35eba8eb956e190941fcfc8fce422`

```dockerfile
```

-	Layers:
	-	`sha256:8f3046137e85325a38a2b9c6b75180c80710318e41cb83c52fef56b171ffb11b`  
		Last Modified: Tue, 19 May 2026 23:27:46 GMT  
		Size: 3.3 MB (3326904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5382c40793d8d8f594fb48a3cc3333b187ac8aca01bda3f32d6917e9646d188`  
		Last Modified: Tue, 19 May 2026 23:27:46 GMT  
		Size: 18.0 KB (17981 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:10.1.8`

```console
$ docker pull swipl@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `swipl:latest`

```console
$ docker pull swipl@sha256:dd38ccc80e276e07fa0a6c9add34829a29d8e3c049a8966896f175519a57e65a
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
$ docker pull swipl@sha256:c3803feff5aabf459cdf252244c1fe72af6af59d2ec442a286dd4e30d9eb3123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104156777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74f41492b3daae1e40f9ca4867fb2d47dcc703ad1a183f72674ed20c94d7197`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:18:12 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 19 May 2026 23:18:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4t64     libarchive13t64     libyaml-0-2     libgmp10     libutf8proc3     libossp-uuid16     libssl3t64     ca-certificates     libdb5.3t64     libpcre2-8-0     libgeos-c1t64     libspatialindex8     libspatialindex-c8     libodbc2     libodbccr2     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.13     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:18:12 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:23:45 GMT
RUN set -eux;     SWIPL_VER=10.1.7;     SWIPL_CHECKSUM=68a134693c6626ae30a8a098238b8dd202c2ccbb358a4e0fb6466e231b846b5c;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libutf8proc-dev libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_GUI=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 831482c8f267e002147dc482c4e6509f9e27d97e;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git d1463581484ec794d92700f88cee431b257f33dc;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git ba23ea9aa4e22fcd1fc1ea3431950ef3e9375551;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git c6ef865f1cd9fe393213dd273fce13e96e4cb249;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 19 May 2026 23:23:45 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6ff8da276997477a9d029ed7b0e9c041a1d2a34c9be620c08e7dd1b634c9f2`  
		Last Modified: Tue, 19 May 2026 23:23:58 GMT  
		Size: 52.4 MB (52415790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c274f02e4c761ea00525462d64dc97ec2751bd6b9c6f92b40b6dccc8e54c23d7`  
		Last Modified: Tue, 19 May 2026 23:23:57 GMT  
		Size: 22.0 MB (21961061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:cccf62a10632f249fac2f98bb8a585281bd5272cb8abc3827e815991875fb34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3050577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882d08f9e63239728e7e62ee46f8c1bf62ecf15b80ce7642ab2bfb48fd41227d`

```dockerfile
```

-	Layers:
	-	`sha256:4d65ff5ddc0e11b6b384bdc3565fb9718c86e66e761af25f4e4bc833f59a53b8`  
		Last Modified: Tue, 19 May 2026 23:23:56 GMT  
		Size: 3.0 MB (3032451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8299394f81ca1ea42871fd90f4c0dad80a953861328a27de46a4347e89bff209`  
		Last Modified: Tue, 19 May 2026 23:23:56 GMT  
		Size: 18.1 KB (18126 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:eae7bf0ba145c84f6858260e0167baf3335b3ad8ffc3424bca2d0ccb5fd56d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90538156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674cf53197e77cfd34a73e4c9a02435d5a4055885425eb6fcbfcc2c0870fbb93`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:00:06 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 20 May 2026 00:00:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4t64     libarchive13t64     libyaml-0-2     libgmp10     libutf8proc3     libossp-uuid16     libssl3t64     ca-certificates     libdb5.3t64     libpcre2-8-0     libgeos-c1t64     libspatialindex8     libspatialindex-c8     libodbc2     libodbccr2     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.13     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:00:06 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:02:33 GMT
RUN set -eux;     SWIPL_VER=10.1.7;     SWIPL_CHECKSUM=68a134693c6626ae30a8a098238b8dd202c2ccbb358a4e0fb6466e231b846b5c;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libutf8proc-dev libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_GUI=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 831482c8f267e002147dc482c4e6509f9e27d97e;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git d1463581484ec794d92700f88cee431b257f33dc;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git ba23ea9aa4e22fcd1fc1ea3431950ef3e9375551;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git c6ef865f1cd9fe393213dd273fce13e96e4cb249;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 20 May 2026 00:02:33 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f76f46bf113929bf69b41d23380c37f7fbb4d666b8a224c273577b1bc588e1`  
		Last Modified: Wed, 20 May 2026 00:02:46 GMT  
		Size: 47.0 MB (46995711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc6858b848144bc4a11bf0c55b9ca90507188d941e9b3c9824213a7db32c76d`  
		Last Modified: Wed, 20 May 2026 00:02:45 GMT  
		Size: 17.3 MB (17336614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:f9ddb304100c05da1033938d289058dd93adbb66d77591a55a63f4e0c6edb840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea7a93206fe2d77a428ea7b385f09267d0df1e0ae72bebfb36b29429df082c4`

```dockerfile
```

-	Layers:
	-	`sha256:bc48779b35dbadee5da093487cb2796a43500f80be91fc15ba8d89cfbc95af89`  
		Last Modified: Wed, 20 May 2026 00:02:44 GMT  
		Size: 3.0 MB (3030504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44d7df19f959c78fc4838bfb0082bc3ebceec72f30a649b7b696e3620c02286f`  
		Last Modified: Wed, 20 May 2026 00:02:44 GMT  
		Size: 18.2 KB (18203 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:dc2b8fa6eb355127aca75b7c8a74fe9d9e68ac3ea51dfac7184f68214a44bfd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103095718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6b4f68644c235436b831fbe8e4a87e8bbf0975976babe9c95da0797b366698`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:21:41 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 19 May 2026 23:21:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4t64     libarchive13t64     libyaml-0-2     libgmp10     libutf8proc3     libossp-uuid16     libssl3t64     ca-certificates     libdb5.3t64     libpcre2-8-0     libgeos-c1t64     libspatialindex8     libspatialindex-c8     libodbc2     libodbccr2     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.13     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:21:41 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:27:29 GMT
RUN set -eux;     SWIPL_VER=10.1.7;     SWIPL_CHECKSUM=68a134693c6626ae30a8a098238b8dd202c2ccbb358a4e0fb6466e231b846b5c;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libutf8proc-dev libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_GUI=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 831482c8f267e002147dc482c4e6509f9e27d97e;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git d1463581484ec794d92700f88cee431b257f33dc;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git ba23ea9aa4e22fcd1fc1ea3431950ef3e9375551;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git c6ef865f1cd9fe393213dd273fce13e96e4cb249;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 19 May 2026 23:27:29 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c64e774316b41e4c7bf559e7c518928ac6d956f2798e43fe52d51a41a214146`  
		Last Modified: Tue, 19 May 2026 23:27:44 GMT  
		Size: 51.7 MB (51676826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4968b347d31526fd6c798962722cb57e8ce83f517285b5c4ccb73143ae8472`  
		Last Modified: Tue, 19 May 2026 23:27:43 GMT  
		Size: 21.3 MB (21276973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:3f1f50a102b0b66f46021aa03bf17ec118a7783da00f6a02616d6a43a097d3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3051016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2900d51dcee052fc0eb498f4dff1456e0428c8c7d8d2a565b08e738a8941d368`

```dockerfile
```

-	Layers:
	-	`sha256:614858c2ab270b094ab95d5aacaed8bda4a9c09b57d5bf1f64d31e7a3a80f754`  
		Last Modified: Tue, 19 May 2026 23:27:42 GMT  
		Size: 3.0 MB (3032794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20af682a59376471019c956cccdc4dfccb165ee41c97e003281c5ac75fcb6c8f`  
		Last Modified: Tue, 19 May 2026 23:27:42 GMT  
		Size: 18.2 KB (18222 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:stable`

```console
$ docker pull swipl@sha256:26cf6a0174374ebb7cf70a356ae7cace36181b25d522fca64354e094f30593fe
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
$ docker pull swipl@sha256:c164a5248a9677ae9a3f6e797afa6095377cab7d0e8bd0d8b420d0558c3ca3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99111287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e459c7118a667623e0089546208533379dd97e811563e3df7ac77a1ca8e4a76`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:18:33 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 19 May 2026 23:18:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:24:55 GMT
RUN set -eux;     SWIPL_VER=10.0.2;     SWIPL_CHECKSUM=e42cc098f7b8a6051c4f79a99b55162d467098aba60f69649bdc7583f0734b57;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git d1463581484ec794d92700f88cee431b257f33dc;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 19 May 2026 23:24:55 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc13a076afde065de391de9cda4c74c42d81d022bda16e5ff64a247fa876f21`  
		Last Modified: Tue, 19 May 2026 23:25:10 GMT  
		Size: 49.2 MB (49238372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b970190cd19c0849f3a49f5d3530fdb6f01d3ef8728946f22c26fdff49616c02`  
		Last Modified: Tue, 19 May 2026 23:25:08 GMT  
		Size: 21.6 MB (21639372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:00046a56ec4e20fac0fb72f444886050d6210814309630a8f52c8180d7221ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952efc366917427f9d7160cbcc0b0f9d6ae348f61efbde1793519accca157cf4`

```dockerfile
```

-	Layers:
	-	`sha256:564827b346a619c36f6f60d8c8cac8dffed1e966ae5631a70e97901669138c2a`  
		Last Modified: Tue, 19 May 2026 23:25:08 GMT  
		Size: 3.3 MB (3326564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d17a7f863a8ed1b5aba04f579701c137eb98947eecf64cc883cdc8fcf41912`  
		Last Modified: Tue, 19 May 2026 23:25:07 GMT  
		Size: 17.9 KB (17886 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:67f7d113bc509a86310239970929de5c61477cfda4bb2017514d49deac30a656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84830307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ee14451a76e628099c36561c12d17aa48c37c535200a12be13950827e94c61`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:01:22 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 20 May 2026 00:01:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:01:22 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:03:55 GMT
RUN set -eux;     SWIPL_VER=10.0.2;     SWIPL_CHECKSUM=e42cc098f7b8a6051c4f79a99b55162d467098aba60f69649bdc7583f0734b57;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git d1463581484ec794d92700f88cee431b257f33dc;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 20 May 2026 00:03:55 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245337099e11728a994e85cbddcbcf2a1c0f9e5420fc6607e06dbfc3e7327522`  
		Last Modified: Wed, 20 May 2026 00:04:07 GMT  
		Size: 43.8 MB (43751910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3511bcaa3591068576d32ca9802f8cab19088bb33c55e6dbea732ce3dcb15153`  
		Last Modified: Wed, 20 May 2026 00:04:06 GMT  
		Size: 17.1 MB (17136754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:c4bb60ee44f12f13ca31ccc71849e68f58d8935513a3524e43ed387286f4632d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfddd5aa39cdede9abfc2aa440ed8465dffda478a6869577f104972d00a6f79e`

```dockerfile
```

-	Layers:
	-	`sha256:d2a2387cedee942d38c592b810ee0041ecf6c4453f606c3d188d00a6da9714aa`  
		Last Modified: Wed, 20 May 2026 00:04:06 GMT  
		Size: 3.3 MB (3325410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cd11ff1380d45f63153618daad1072c214109d2e72a3f754d41071213f2f5f6`  
		Last Modified: Wed, 20 May 2026 00:04:05 GMT  
		Size: 18.0 KB (17963 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:40995f8bf0152a304791f08f9a244f734a9735ba68c4c824c581d4a7bbd607e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96914984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527685fab3f5cba5668d852bddab31b19694a298d21fae18a7aabbab239a58cd`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:21:37 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 19 May 2026 23:21:37 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:21:37 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:27:33 GMT
RUN set -eux;     SWIPL_VER=10.0.2;     SWIPL_CHECKSUM=e42cc098f7b8a6051c4f79a99b55162d467098aba60f69649bdc7583f0734b57;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git d1463581484ec794d92700f88cee431b257f33dc;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 19 May 2026 23:27:33 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0886d6f0c4239984c1aca793add652a343e1c6b33a59a17a1d7676ed3d2076`  
		Last Modified: Tue, 19 May 2026 23:27:48 GMT  
		Size: 47.8 MB (47803276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4b6e132d5e678934d06dd9e655ad84913abcc5c6ea758d6be327154d6abfaf`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 21.0 MB (20996665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:fb331d3366123eef5802a408b00815928e39c16db87b4f9e40ea049305d7ee44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ceab182d7beddfcb95b87427ce50a748a35eba8eb956e190941fcfc8fce422`

```dockerfile
```

-	Layers:
	-	`sha256:8f3046137e85325a38a2b9c6b75180c80710318e41cb83c52fef56b171ffb11b`  
		Last Modified: Tue, 19 May 2026 23:27:46 GMT  
		Size: 3.3 MB (3326904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5382c40793d8d8f594fb48a3cc3333b187ac8aca01bda3f32d6917e9646d188`  
		Last Modified: Tue, 19 May 2026 23:27:46 GMT  
		Size: 18.0 KB (17981 bytes)  
		MIME: application/vnd.in-toto+json
