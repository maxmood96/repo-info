## `swipl:latest`

```console
$ docker pull swipl@sha256:0a05e58dd72b2ff17617936a8e3725caf33b3be60e587093c037a9392de654a5
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
$ docker pull swipl@sha256:4df87cc00d039f9d0e6bad765678d4ec5d607bc8a7f34dd87a23109ff95c9243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96479344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446647e868f86fd7941ab3a158ec32ba9b55a6785e50ba32516af967af4e5be7`
-	Default Command: `["swipl"]`

```dockerfile
# Wed, 31 Jan 2024 17:20:27 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 17:20:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 17:20:27 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 31 Jan 2024 17:20:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 17:20:27 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jan 2024 17:20:27 GMT
RUN set -eux;     SWIPL_VER=9.3.0;     SWIPL_CHECKSUM=65620c74927002431fcf5baa34e1fe7ef7264381d72d274efc5f00c1c69cdd23;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 31 Jan 2024 17:20:27 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44a6572fb29abcdca707da1e4e3c14945d5c5fe5b3ad08acdefddf14cad9a54`  
		Last Modified: Thu, 08 Feb 2024 19:02:11 GMT  
		Size: 49.2 MB (49204526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe2a0967f8e89d5e47e94b605697a071c4bf2d0d1fd772909ebb3843a0fee0f`  
		Last Modified: Thu, 08 Feb 2024 19:02:10 GMT  
		Size: 18.1 MB (18124353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:895d7a699ce22f3c796a0daccd0a5cfee933a73515f5dc6dd0b8ddfa526be58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54afa55d9478b0ed23069e8840faadef8f64b6623c7fee4d8461662dc7e485f`

```dockerfile
```

-	Layers:
	-	`sha256:ddb9446f964e72720704037f34ad27682f523087c9bddb7037b0a14027495b54`  
		Last Modified: Thu, 08 Feb 2024 19:02:09 GMT  
		Size: 2.7 MB (2725192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1439c9c1a26ec3df8aca2686842195b72832b203452facdb48b8b5535cf52cd8`  
		Last Modified: Thu, 08 Feb 2024 19:02:09 GMT  
		Size: 17.3 KB (17266 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:a69bcc64f8a64b10ec92bf184a5c6624d3bf5357c228c4d46c929ef0605dff0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82837556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdb2341969d3d2b06b09e7757455f535750b136732eff53ead894b1059164f3`
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
RUN set -eux;     SWIPL_VER=9.3.0;     SWIPL_CHECKSUM=65620c74927002431fcf5baa34e1fe7ef7264381d72d274efc5f00c1c69cdd23;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
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
	-	`sha256:1031764b17f140ff368a97ef9f3875de98b7c060b64c925ed68f0cfd238ecefd`  
		Last Modified: Fri, 09 Feb 2024 09:42:00 GMT  
		Size: 14.4 MB (14398356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:46e2b7781014d26346a9bb1d2b1d4b8088f2823d78e647e5fe4b83377c1ec974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2744985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939334f811724a17bd2e829bd60a3dd9eb5490f54323ca013c16311255cd9598`

```dockerfile
```

-	Layers:
	-	`sha256:e6c9095bdb014b4a82df61eab6e0325baedc37e958a74e09ea987e13f8569e64`  
		Last Modified: Fri, 09 Feb 2024 09:41:59 GMT  
		Size: 2.7 MB (2727820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67bf435865e2c6576eabb122fe8191461fb44130ca8a322e24be1133135961c9`  
		Last Modified: Fri, 09 Feb 2024 09:41:59 GMT  
		Size: 17.2 KB (17165 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:86243247d89b0c9bf2108d953aa2dba3cabc6a5339ad2cc4cb958bd5a8c2efc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94436654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e85e382e15be441ef738ca5e084d7c34c544f2d13dce47b42e7c7a7c61271f8`
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
RUN set -eux;     SWIPL_VER=9.3.0;     SWIPL_CHECKSUM=65620c74927002431fcf5baa34e1fe7ef7264381d72d274efc5f00c1c69cdd23;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
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
	-	`sha256:7c3d0f2b98734223d78ddcccbf0776151dc4db637e41951a59f9e2e2699bf234`  
		Last Modified: Thu, 08 Feb 2024 19:44:00 GMT  
		Size: 17.6 MB (17573954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:8a64ff2af927a60bdd0f45690a85bf2155c9828de791b8b933a8458a1d0cf03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f168ba54a94953185bbbffb536c054849cf8715a1ac2cd5155e18273ddc1be7`

```dockerfile
```

-	Layers:
	-	`sha256:953160ff9689dedd8bf80b07600c6c6cf66db8fcc17b27c19bafa6bf44836046`  
		Last Modified: Thu, 08 Feb 2024 19:43:59 GMT  
		Size: 2.7 MB (2725611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b192407a9e1ef2d4787b0aff3a57686e2d94ca7a9a7c81aad150ef45c2791e87`  
		Last Modified: Thu, 08 Feb 2024 19:43:59 GMT  
		Size: 17.1 KB (17105 bytes)  
		MIME: application/vnd.in-toto+json
