## `swipl:latest`

```console
$ docker pull swipl@sha256:6c4670efc92adbd89b06a376d4e03859446ac293e15ee49591f063042067aa73
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
$ docker pull swipl@sha256:fa392e90e0360874b1eb2cc50fb37a53fc5a9a4e3146e600f3989b737cee3808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96167547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa515b119bb26fab3af9b9fb8c0ba2361f3fe687709b6d24c73021954a866701`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 07 Jan 2025 09:48:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 07 Jan 2025 09:48:06 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 07 Jan 2025 09:48:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 09:48:06 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jan 2025 09:48:06 GMT
RUN set -eux;     SWIPL_VER=9.3.18;     SWIPL_CHECKSUM=8302de3a9e204bccd8e1c1211737572a67c511d1713d13abf7a726abfb181ac3;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 07 Jan 2025 09:48:06 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14261c79b9569979757060ec11e9c50a02356815ec5a66fa7366e97b593ddb75`  
		Last Modified: Tue, 14 Jan 2025 02:30:29 GMT  
		Size: 49.2 MB (49219240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081ca1840c2dd4f019a7c09a67aa581c1660f0f5526640fe6b64c990768897cb`  
		Last Modified: Tue, 14 Jan 2025 22:04:30 GMT  
		Size: 18.7 MB (18735890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:26bfffa5649d597f169e2abd0bccb9ae27f0d3f60482bed9f4940f33f14e223e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d320625fd04c74463f2b12914f80aa9cdb1d872f987ac863ff813af2dfaf2a22`

```dockerfile
```

-	Layers:
	-	`sha256:77e01258e3e0ce51a0223a6dd26faa3292366eed1b3de999cd1bbb6b68627d40`  
		Last Modified: Tue, 14 Jan 2025 02:30:28 GMT  
		Size: 3.2 MB (3162042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:470ba5dfe5f8397a570624ea2aa8fdcfad844d66599b9aa7a4f4af791db0a190`  
		Last Modified: Tue, 14 Jan 2025 02:30:27 GMT  
		Size: 17.5 KB (17511 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:d8613ee7d99119726b3a68ad9399d7f533a7584bcbc310ec64d9b87b06ad2e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81999609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2ab7181e8780e7c3c7e6c535dd5643d4ae574a1fe7860e9997511c847150e4`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 07 Jan 2025 09:48:06 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Tue, 07 Jan 2025 09:48:06 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 07 Jan 2025 09:48:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 09:48:06 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jan 2025 09:48:06 GMT
RUN set -eux;     SWIPL_VER=9.3.18;     SWIPL_CHECKSUM=8302de3a9e204bccd8e1c1211737572a67c511d1713d13abf7a726abfb181ac3;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 07 Jan 2025 09:48:06 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 20:33:55 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef350de1da4302db8ac04a639a80a3e858d3f1250a069a30c1bc3753d7f8c6aa`  
		Last Modified: Tue, 14 Jan 2025 08:45:58 GMT  
		Size: 43.7 MB (43734017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a5d9234f569c4d5a070198819d96b9c8049b3ed570dc5eb6c5ac919d741574`  
		Last Modified: Tue, 14 Jan 2025 08:45:57 GMT  
		Size: 14.4 MB (14350992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:3f4d9fcadeec2eb5da8368ce35085dddd8d335ce976436f8bc26fbc7e0b43cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbb2e371ccb1218986279bd2b549f3fa5ea595757c1446ebab1787fa86e4ba3`

```dockerfile
```

-	Layers:
	-	`sha256:a6bea81d6a4e0a352b93e9f0b6d09195a785b661305cda8190a4ef5debbf8d56`  
		Last Modified: Tue, 14 Jan 2025 08:45:57 GMT  
		Size: 3.2 MB (3160888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a787b3e1dd22548ea49b76c5f5e45c53c6f9177ef5276892202c93ba9de464`  
		Last Modified: Tue, 14 Jan 2025 08:45:56 GMT  
		Size: 17.6 KB (17584 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:7181b830dd9a750c8d1b1aceec9c014e822a7315497e7a9962cd497b53186a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93885825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f0f8f9ecfbe558036fd9b40cf567429c4e3b79fcb6a13605a04c0e6564f15`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 07 Jan 2025 09:48:06 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 07 Jan 2025 09:48:06 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 07 Jan 2025 09:48:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 09:48:06 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jan 2025 09:48:06 GMT
RUN set -eux;     SWIPL_VER=9.3.18;     SWIPL_CHECKSUM=8302de3a9e204bccd8e1c1211737572a67c511d1713d13abf7a726abfb181ac3;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 07 Jan 2025 09:48:06 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773165c618aabebccd8ab5ade4eafa7d447b020a3340cfb15c6a93bf2b33704e`  
		Last Modified: Tue, 14 Jan 2025 06:45:19 GMT  
		Size: 47.7 MB (47713632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fa2116fbe2c9dd2dc90f1942548d5d2b073d9eb0b5b9b487182aa8d81f3419`  
		Last Modified: Tue, 14 Jan 2025 06:45:18 GMT  
		Size: 18.1 MB (18131162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:ec39f57acb341ccdf7a02242135ca7e4f001e5931fb36bb51a6561f089727730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c418ee0dd0fb726cb3d84f6eecf65010381a499914095e4c321a97269ba1f6`

```dockerfile
```

-	Layers:
	-	`sha256:193be509bdd2012a0796fdcea0d90220a5fd220727b3381c39dff5c057af475c`  
		Last Modified: Tue, 14 Jan 2025 06:45:18 GMT  
		Size: 3.2 MB (3162382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79595b0a0c15dd96ce4b05c8e1ae359c718677b3a77cb2e141914141fd1be12a`  
		Last Modified: Tue, 14 Jan 2025 06:45:17 GMT  
		Size: 17.6 KB (17606 bytes)  
		MIME: application/vnd.in-toto+json
