<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:9.2.0`](#swipl920)
-	[`swipl:9.3.0`](#swipl930)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:9.2.0`

```console
$ docker pull swipl@sha256:845a317bb8cc1999c7c2d4ec737d80796fc4bdcd5d52a844eedcd1ac00ffc514
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.2.0` - linux; amd64

```console
$ docker pull swipl@sha256:641fc144ac9dcf77794eae3f61de93c7bd7f1f86fb37b3875ee1d5e1561b4a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96477798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6661a19a45d9b5cc22b246f27d7f5cc4539c7fc349749474b4537e19ef35bdd`
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
RUN set -eux;     SWIPL_VER=9.2.0;     SWIPL_CHECKSUM=10d90b15734d14d0d7972dc11a3584defd300d65a9f0b1185821af8c3896da5e;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 31 Jan 2024 17:20:27 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5f23999b1ec9d38f089af5920963594e9e5292c1dc780130ab1af4ecbe8957`  
		Last Modified: Thu, 08 Feb 2024 19:02:09 GMT  
		Size: 49.2 MB (49204595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac4e182876fe22e519402be2fa67cc3b674e0f9e070a1770e390ab239ae16f7`  
		Last Modified: Thu, 08 Feb 2024 19:02:08 GMT  
		Size: 18.1 MB (18122738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.0` - unknown; unknown

```console
$ docker pull swipl@sha256:75856a2fc3201fca1847805cd87b4f350324ebe5f15c0c941ba93390f96c43bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e03c28db48ba8d3132a387148a14411975baed20f8a939b0c69fc6485b6eb4`

```dockerfile
```

-	Layers:
	-	`sha256:85b4666afa499a64069dce207d57e93a960054435f08adab3d7993ec379ecedd`  
		Last Modified: Thu, 08 Feb 2024 19:02:08 GMT  
		Size: 2.7 MB (2725192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a36312094f69136ec095c3c2a80ab3862d9619150932317630378cba5e87eb1`  
		Last Modified: Thu, 08 Feb 2024 19:02:08 GMT  
		Size: 17.3 KB (17267 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.0` - linux; arm variant v7

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

### `swipl:9.2.0` - unknown; unknown

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

### `swipl:9.2.0` - linux; arm64 variant v8

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

### `swipl:9.2.0` - unknown; unknown

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

## `swipl:9.3.0`

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

### `swipl:9.3.0` - linux; amd64

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

### `swipl:9.3.0` - unknown; unknown

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

### `swipl:9.3.0` - linux; arm variant v7

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

### `swipl:9.3.0` - unknown; unknown

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

### `swipl:9.3.0` - linux; arm64 variant v8

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

### `swipl:9.3.0` - unknown; unknown

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

## `swipl:stable`

```console
$ docker pull swipl@sha256:845a317bb8cc1999c7c2d4ec737d80796fc4bdcd5d52a844eedcd1ac00ffc514
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
$ docker pull swipl@sha256:641fc144ac9dcf77794eae3f61de93c7bd7f1f86fb37b3875ee1d5e1561b4a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96477798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6661a19a45d9b5cc22b246f27d7f5cc4539c7fc349749474b4537e19ef35bdd`
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
RUN set -eux;     SWIPL_VER=9.2.0;     SWIPL_CHECKSUM=10d90b15734d14d0d7972dc11a3584defd300d65a9f0b1185821af8c3896da5e;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Wed, 31 Jan 2024 17:20:27 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5f23999b1ec9d38f089af5920963594e9e5292c1dc780130ab1af4ecbe8957`  
		Last Modified: Thu, 08 Feb 2024 19:02:09 GMT  
		Size: 49.2 MB (49204595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac4e182876fe22e519402be2fa67cc3b674e0f9e070a1770e390ab239ae16f7`  
		Last Modified: Thu, 08 Feb 2024 19:02:08 GMT  
		Size: 18.1 MB (18122738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:75856a2fc3201fca1847805cd87b4f350324ebe5f15c0c941ba93390f96c43bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e03c28db48ba8d3132a387148a14411975baed20f8a939b0c69fc6485b6eb4`

```dockerfile
```

-	Layers:
	-	`sha256:85b4666afa499a64069dce207d57e93a960054435f08adab3d7993ec379ecedd`  
		Last Modified: Thu, 08 Feb 2024 19:02:08 GMT  
		Size: 2.7 MB (2725192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a36312094f69136ec095c3c2a80ab3862d9619150932317630378cba5e87eb1`  
		Last Modified: Thu, 08 Feb 2024 19:02:08 GMT  
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
