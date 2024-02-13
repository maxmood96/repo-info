## `swipl:stable`

```console
$ docker pull swipl@sha256:1e7225c6cee1a063316b28a76396be706679bb8e0efaa8f26e0c62a45034ccd6
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
$ docker pull swipl@sha256:0a7bc793371ed4dcd07a015c1a335745a54277cc8f097b0f82ce23a034600ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96450544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c2f34e47fdde3a931b1a432a46afbe43b60a06f640eb9d5a9b7c3e68a2e3a6`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 31 Jan 2024 17:20:27 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 31 Jan 2024 17:20:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 17:20:27 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 31 Jan 2024 17:20:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 17:20:27 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jan 2024 17:20:27 GMT
RUN set -eux;     SWIPL_VER=9.2.0;     SWIPL_CHECKSUM=10d90b15734d14d0d7972dc11a3584defd300d65a9f0b1185821af8c3896da5e;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 31 Jan 2024 17:20:27 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48dbdb970a5c766f345379eb6176634611c5ceb653ae8d053a1c62d100d69ce5`  
		Last Modified: Tue, 13 Feb 2024 02:06:34 GMT  
		Size: 49.2 MB (49202877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3778e4563fa63126a7098fcf25abd5742355fc0115faa71f0d93752b72d06c8`  
		Last Modified: Tue, 13 Feb 2024 02:06:33 GMT  
		Size: 18.1 MB (18123576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:7c7765a2602bd97fd443db0f754d63eaa17b47205f70582367329bb71b044815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d52a5e57d1401f97173a7cea3f5360406f4a95350a02d0aea71c15aea944b5`

```dockerfile
```

-	Layers:
	-	`sha256:a9607f56e28ea4af2af4c7b8d49bd7cadd9d10cbca09ab851974a228a3ceffe1`  
		Last Modified: Tue, 13 Feb 2024 02:06:33 GMT  
		Size: 2.7 MB (2725240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce72e6af58343329242347fd638cb10b3345b50f21f1661c17ba290444c06053`  
		Last Modified: Tue, 13 Feb 2024 02:06:33 GMT  
		Size: 17.3 KB (17267 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:51f6ed87e0db5c62c927b849eeb60b354fe0dac13d705e9aad12255c506084d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82837359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc11c757dcef6629d1b629f7e41c73a2bb94fcef5052cfe1fb8f4f4d2acfd80`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 31 Jan 2024 17:20:27 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 17:20:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 17:20:27 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 31 Jan 2024 17:20:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 17:20:27 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jan 2024 17:20:27 GMT
RUN set -eux;     SWIPL_VER=9.2.0;     SWIPL_CHECKSUM=10d90b15734d14d0d7972dc11a3584defd300d65a9f0b1185821af8c3896da5e;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 31 Jan 2024 17:20:27 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f169f2e91eae16013bff378005bd2ef8314a4dd96bf792ee4b730666c0b7ed1`  
		Last Modified: Fri, 09 Feb 2024 09:42:01 GMT  
		Size: 43.7 MB (43697635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45457212abe563a67519c448a8c0b177be8c4f128d66fa7bf635fbace439219`  
		Last Modified: Fri, 09 Feb 2024 10:55:55 GMT  
		Size: 14.4 MB (14398159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:a635d955042d4e979eb7dacd730cd0f7a867fa6eaef3fa4ecca4f507d59ba58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2744987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a52afbbae3191d47ed38c4ea7e71cbc382b2ccc8de05f2c28eb60e762f0326`

```dockerfile
```

-	Layers:
	-	`sha256:3c966d721d263b355a07fac05a147faf1b18718e028d55493bc5948ff0a97dd7`  
		Last Modified: Fri, 09 Feb 2024 10:55:54 GMT  
		Size: 2.7 MB (2727820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c9aaf3712cff2a1ee9c7a5fbf0d6090efc9837831c427649989c9446b50a70`  
		Last Modified: Fri, 09 Feb 2024 10:55:54 GMT  
		Size: 17.2 KB (17167 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:3621d7115caff23a98ad77fd7d377211bc4e40fc9fcb043d879cf6f8c138bdac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94439585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67361d97f6a16ce6c8847f35c61cfd37d3736d069bd25fef22a61e7960968469`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 31 Jan 2024 17:20:27 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 17:20:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 17:20:27 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 31 Jan 2024 17:20:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 17:20:27 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jan 2024 17:20:27 GMT
RUN set -eux;     SWIPL_VER=9.2.0;     SWIPL_CHECKSUM=10d90b15734d14d0d7972dc11a3584defd300d65a9f0b1185821af8c3896da5e;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 31 Jan 2024 17:20:27 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908fca5bef8a4e554e74cc61f9ab2b48bc38acaad5357f6c2141d53b46a65284`  
		Last Modified: Thu, 08 Feb 2024 19:44:01 GMT  
		Size: 47.7 MB (47681868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ce6184dd9d08c2d89f2bd29e2a5d93f4a0b1eece6aa9ea44ead2d94be418d1`  
		Last Modified: Thu, 08 Feb 2024 20:00:59 GMT  
		Size: 17.6 MB (17576885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:fa2ec0cb77abb84293c97193557f5b1c4a852722de0de6cc93b4d61314a8ecee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60d7508557529ccadc808827869f8a65863d6c4c00d7ff6205bcce0d08f6452`

```dockerfile
```

-	Layers:
	-	`sha256:8bc7d921817ae908b6a24429058391191606c4419692c794c6068db8bf80785d`  
		Last Modified: Thu, 08 Feb 2024 20:00:59 GMT  
		Size: 2.7 MB (2725611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b9d715332f39978966476c733c253205ea2a482652cb7fb75d980bdcb234bac`  
		Last Modified: Thu, 08 Feb 2024 20:00:58 GMT  
		Size: 17.1 KB (17106 bytes)  
		MIME: application/vnd.in-toto+json
