## `swipl:stable`

```console
$ docker pull swipl@sha256:8f8784cb759c230d63cf478452d574bcfab6a3b58afef0b2eefebf6d7fcff008
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
$ docker pull swipl@sha256:0a6bf341527554126301cba364987978118f1fb7f7dac7d423bd781c5235be4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96469156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d59ac21a11b7f814c50b5d2515297a1bbc9f1f285aefdeeb4e64aae98336c66`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 29 Feb 2024 11:46:50 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Thu, 29 Feb 2024 11:46:50 GMT
CMD ["bash"]
# Thu, 29 Feb 2024 11:46:50 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 29 Feb 2024 11:46:50 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 11:46:50 GMT
RUN set -eux;     SWIPL_VER=9.2.2;     SWIPL_CHECKSUM=896fd51196fd3becd574486da75a924f272e8d63332459292b305986cf101fc3;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32836535bb266084fddec8f71490d9b48b54c62a9591557ff80e77c5888afc67`  
		Last Modified: Tue, 12 Mar 2024 02:11:42 GMT  
		Size: 49.2 MB (49202887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42a0f6ff4c8d42fbf278bb12de926fd075a6e3f734e81876012e139b14abfef`  
		Last Modified: Tue, 12 Mar 2024 02:11:41 GMT  
		Size: 18.1 MB (18142088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:2a029bc6e4d7d20f54e9505e05bd63a0ece37e5e79705469d69ca63f87ef31e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2992146764349cd9fc067080f07b16586b22180a6d5231d84735f931cd584d3f`

```dockerfile
```

-	Layers:
	-	`sha256:cbc36ee1c4be59e1d988bcc29aa189b3fb730c618a9332498e1481c5b4335dee`  
		Last Modified: Tue, 12 Mar 2024 02:11:40 GMT  
		Size: 3.1 MB (3112670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:610f6042afab438ed878ed6c191dd5dacf1f0fcec9737be7b09d5b87d34fcf5e`  
		Last Modified: Tue, 12 Mar 2024 02:11:40 GMT  
		Size: 17.3 KB (17267 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:5cba93863b2e44cc243308e1b5d99b3503aa6b39f422bbcfb042547b2f27dc75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82840246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a28dd4904978c279771550e9e2b4e58b12af9f036841a4bda65eb02909f2112`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:07 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Tue, 13 Feb 2024 01:20:07 GMT
CMD ["bash"]
# Thu, 29 Feb 2024 11:46:50 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 29 Feb 2024 11:46:50 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 11:46:50 GMT
RUN set -eux;     SWIPL_VER=9.2.2;     SWIPL_CHECKSUM=896fd51196fd3becd574486da75a924f272e8d63332459292b305986cf101fc3;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b2a27a7cebfa2e92f78b1b26ac7b33c2195ceb4002dd3c783ce92a4e7c1e6e`  
		Last Modified: Fri, 16 Feb 2024 18:58:35 GMT  
		Size: 43.7 MB (43697601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bca1c5e48bc05e4ce402c87ca233f126741b8d2d94c0669e2645df29fb465e6`  
		Last Modified: Thu, 29 Feb 2024 20:50:19 GMT  
		Size: 14.4 MB (14426000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:a97544fef746563672d982e5fa72b9590032bb9672d90ca10b3fe2db3a46bb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53a15609c6fee830a7d7e18d8019f6f913151ccfff6cc697e44b0c272c148b0`

```dockerfile
```

-	Layers:
	-	`sha256:d004a7fc9c4e8b3366a1df4f3e3929aeaa9664ce9440065275eba6edf72266df`  
		Last Modified: Thu, 29 Feb 2024 20:50:17 GMT  
		Size: 3.1 MB (3115192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdee719b850db4c2383b31b63f28de58089e2ec300db35c3f53b12eae4332bbe`  
		Last Modified: Thu, 29 Feb 2024 20:50:17 GMT  
		Size: 17.2 KB (17167 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:2e75b62507075ba4387071d1dbc6de92b776d301ceee2cf518266579e7431893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94433382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c3c7a5883fc0e68860a06de5fb21b8f4468f52aa207003c34a6f9ed16d1a82`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 29 Feb 2024 11:46:50 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Thu, 29 Feb 2024 11:46:50 GMT
CMD ["bash"]
# Thu, 29 Feb 2024 11:46:50 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 29 Feb 2024 11:46:50 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 11:46:50 GMT
RUN set -eux;     SWIPL_VER=9.2.2;     SWIPL_CHECKSUM=896fd51196fd3becd574486da75a924f272e8d63332459292b305986cf101fc3;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5dd20e57d9cca3db1db3470c02d09cf801db309fb7601c6b42d502263b7eb5`  
		Last Modified: Wed, 13 Mar 2024 05:56:30 GMT  
		Size: 47.7 MB (47676271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6db07ae34fc2afce17293c92898f9e05e043882093d37dc513e19caa85c07a`  
		Last Modified: Wed, 13 Mar 2024 06:02:09 GMT  
		Size: 17.6 MB (17600677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:4bbe3755d52cca6e3fb700af3582ca00096bbe4c81f2740e0fc4ada8a9da5e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3130089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ff0f079879303dacd5668424110cae2e737092deda98a563df64347d160e6b`

```dockerfile
```

-	Layers:
	-	`sha256:8acaeb91846bdda580728f20742c5f4b7cf1f5b72ec7f5a554961f175f299c28`  
		Last Modified: Wed, 13 Mar 2024 06:02:09 GMT  
		Size: 3.1 MB (3112983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5aad7939c8241cca947c0ce953dbd7dfe8934905ddc8477f8823b3d88ca76c7`  
		Last Modified: Wed, 13 Mar 2024 06:02:09 GMT  
		Size: 17.1 KB (17106 bytes)  
		MIME: application/vnd.in-toto+json
