## `swipl:latest`

```console
$ docker pull swipl@sha256:8df259e89f19241ba2032dfc8bd1915db370057a4668856871dc4c9b24392e7b
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
$ docker pull swipl@sha256:2fc5dbd0dc5d96834f937cd602f4b9673cbbc91f967b29bc6a5e1fbeec9184f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98028661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2133c3f5ea84c442725438d356dd266934f5d47d3cbe33784b8855bce231f534`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 01 Sep 2025 15:19:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 01 Sep 2025 15:19:10 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Mon, 01 Sep 2025 15:19:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 15:19:10 GMT
ENV LANG=C.UTF-8
# Mon, 01 Sep 2025 15:19:10 GMT
RUN set -eux;     SWIPL_VER=9.3.29;     SWIPL_CHECKSUM=afa2f9a24440d149b9fcc92e16e35ff9d7b89aeb9f8c6e9780fb617d5b2430ee;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Mon, 01 Sep 2025 15:19:10 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578715f3e6efdd281996ab7f8d6d651af1cda04e72d0fbd7e5c4850054da8c03`  
		Last Modified: Tue, 09 Sep 2025 03:37:23 GMT  
		Size: 49.2 MB (49226131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76c187d579cf4cb4c3916d45b4c0061fe8588534e803a435ad7ac68349fb274`  
		Last Modified: Tue, 09 Sep 2025 02:02:44 GMT  
		Size: 20.6 MB (20574184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:fdf98eb816070ec0bbe392c479689d963c3d6a2dd6e010fda03565bd43d91a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b27e46848bf942e14a823264a6be67451b007dd09690e3f55cbbd369895e72`

```dockerfile
```

-	Layers:
	-	`sha256:061cd14fb8b64b9dca717f480687e9638ad031bb7cf4a6bab4f446c046c6144c`  
		Last Modified: Mon, 08 Sep 2025 23:12:40 GMT  
		Size: 3.3 MB (3326536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbc9d28e246bfc3a02985faf21ddb7d8ad84f2d988820648e6fec8fcf3e8abe9`  
		Last Modified: Mon, 08 Sep 2025 23:12:41 GMT  
		Size: 17.5 KB (17511 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:16a5d89cbf7c9d529bbdb7d74818352b1bf60f02fcd96e3a9f93795f91053951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83894223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d082514bd1d456ee7399ae3a1b8c7074f748d60c15254fe625c1390bf20e02`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 01 Sep 2025 15:19:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Mon, 01 Sep 2025 15:19:10 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Mon, 01 Sep 2025 15:19:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 15:19:10 GMT
ENV LANG=C.UTF-8
# Mon, 01 Sep 2025 15:19:10 GMT
RUN set -eux;     SWIPL_VER=9.3.29;     SWIPL_CHECKSUM=afa2f9a24440d149b9fcc92e16e35ff9d7b89aeb9f8c6e9780fb617d5b2430ee;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Mon, 01 Sep 2025 15:19:10 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:e747f8ef7f1d9a41c99bfb53889f7b8de3504300740a326627fc7522904708cc`  
		Last Modified: Mon, 08 Sep 2025 21:14:21 GMT  
		Size: 23.9 MB (23933904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37639e976963411964a72af8327adc20f542249c1640950b8f67620c4e1bc9a`  
		Last Modified: Tue, 09 Sep 2025 18:10:50 GMT  
		Size: 43.8 MB (43767032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0f62e8d552b89bc0cf7d500db767e4af371107599a2c373219fa889e48755b`  
		Last Modified: Tue, 09 Sep 2025 18:10:44 GMT  
		Size: 16.2 MB (16193287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:d69c0c8baa7e75b73ad6d027d1e9d149dc1c21d9ba67e696ac295b3fc06cdfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3342969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43ba769449758ddf9c1691b437d7015b10d90b53c8d6b1137eb9397d1efb761`

```dockerfile
```

-	Layers:
	-	`sha256:af32c15418471f766091c311e05f232800e6e23e514fc4005598970c569bf124`  
		Last Modified: Mon, 08 Sep 2025 23:12:46 GMT  
		Size: 3.3 MB (3325382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31ef27013d8e06172c4f8cc50e705f772ea658b6586f47bbb5f77eea03d90fd`  
		Last Modified: Mon, 08 Sep 2025 23:12:46 GMT  
		Size: 17.6 KB (17587 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:142b724e135a11b98a1d87301d2b425d234803a9f2eef424eab1f46344b7ccbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95869122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1f3641ca7dbca87fddbf578b137a57774c26467c876eab3885d639ae4d81a3`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 01 Sep 2025 15:19:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 01 Sep 2025 15:19:10 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Mon, 01 Sep 2025 15:19:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 15:19:10 GMT
ENV LANG=C.UTF-8
# Mon, 01 Sep 2025 15:19:10 GMT
RUN set -eux;     SWIPL_VER=9.3.29;     SWIPL_CHECKSUM=afa2f9a24440d149b9fcc92e16e35ff9d7b89aeb9f8c6e9780fb617d5b2430ee;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Mon, 01 Sep 2025 15:19:10 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234a7903150b994d00569893b99d13aad101a1616133b2179aac0fa297ebe4c7`  
		Last Modified: Mon, 08 Sep 2025 22:30:53 GMT  
		Size: 47.8 MB (47808012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2b4146bf5b97fdfc82ab607d551810d50e7d66137337d181ca94626827c92d`  
		Last Modified: Mon, 08 Sep 2025 22:30:57 GMT  
		Size: 20.0 MB (19959011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:6930b5e6f018fda579407047ec74e48dc6e7e31c98e0760f887c63a031a3e03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2a043dc560cdac6cf7026d981aa0d4ebcb90d2d3e01168af5358b7b49302e3`

```dockerfile
```

-	Layers:
	-	`sha256:f4e1d6c6e79caf044b65a033e60d72ab28e923c7b8b0b2f97aa30e5e6a4d8948`  
		Last Modified: Mon, 08 Sep 2025 23:12:51 GMT  
		Size: 3.3 MB (3326876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b528de9ba6c4fec92397013166985df3e1eaf8fd44173a245cd26b4a444791e`  
		Last Modified: Mon, 08 Sep 2025 23:12:52 GMT  
		Size: 17.6 KB (17605 bytes)  
		MIME: application/vnd.in-toto+json
