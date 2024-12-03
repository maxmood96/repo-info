<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:9.2.8`](#swipl928)
-	[`swipl:9.3.16`](#swipl9316)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:9.2.8`

```console
$ docker pull swipl@sha256:9dc59e189a176cd54da83aca7331d9158c93846e37fbf072a7c7fd2f5d85bd17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.2.8` - linux; amd64

```console
$ docker pull swipl@sha256:9d88196372ae372366c3521e128ce53d294ce9d18c4212d2f71dceaba4f93481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96896551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d36b32fd16c03219714ae384c3f80c0c6856019d2d3b111554e8d608be4b3dc`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.2.8;     SWIPL_CHECKSUM=b331637a57c913c49edcfcb10ddcf6c031278ce93d2411d54542778531abb5c7;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03630e44222222e34a9b723b7ebdddaf0d55bbedbfda113c1cef30bbe06dbafe`  
		Last Modified: Tue, 12 Nov 2024 02:24:23 GMT  
		Size: 49.2 MB (49222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618ebb0d6203ef8afe7f315237fa04971cbecbfffe362caca2c375b2850cbfc1`  
		Last Modified: Tue, 12 Nov 2024 02:24:23 GMT  
		Size: 18.5 MB (18545882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.8` - unknown; unknown

```console
$ docker pull swipl@sha256:0e34b6884630329fbb2fdd982ddf1b3143ff7abbd46ecc0a13b1d16c02291562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3184740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2344c1a670c92b8e1a6258d684c204502bdc2902fae5f77de76d0d19bd672b77`

```dockerfile
```

-	Layers:
	-	`sha256:a31ecbc89b4dbdb7b4afedddda43a7bd363fb838af0ed8d6a03d18e5a83fe44a`  
		Last Modified: Tue, 12 Nov 2024 02:24:22 GMT  
		Size: 3.2 MB (3167233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2136514aad85ed501329dd609915e59b537ae41178e61efa73e1c541975ac6c9`  
		Last Modified: Tue, 12 Nov 2024 02:24:22 GMT  
		Size: 17.5 KB (17507 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.8` - linux; arm variant v7

```console
$ docker pull swipl@sha256:39e0c511b6588a112609acf7228031dce6412cd4c863a439819070684521d453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82551347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732a2ce37028b30735dd8dc8df77493163b96c7f872ac69f758eafa3c5ddcc14`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.2.8;     SWIPL_CHECKSUM=b331637a57c913c49edcfcb10ddcf6c031278ce93d2411d54542778531abb5c7;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5c21fa4169213eb4e571405f837875ed102be8e3d768c9af90bff7c9ccd3e0`  
		Last Modified: Tue, 12 Nov 2024 15:35:09 GMT  
		Size: 43.7 MB (43717482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7063cac71067db6a15373f76d8f0a1928fdf860afe6bcce182849b8b5df12e7`  
		Last Modified: Tue, 12 Nov 2024 15:38:46 GMT  
		Size: 14.1 MB (14114956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.8` - unknown; unknown

```console
$ docker pull swipl@sha256:7bc6be22081abf215d35b97b68989efdf7bdd5c04e300337e4106e9b668ea7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3183683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f1919e4f284f3f93a025eb5478916774bd544882ecdc5f013927f72b24e803`

```dockerfile
```

-	Layers:
	-	`sha256:c9db1eb29b243b33e6c076ce21c31140feafb9ec00c73d55547b7d8484ffc940`  
		Last Modified: Tue, 12 Nov 2024 15:38:46 GMT  
		Size: 3.2 MB (3166105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b873c4d4c175e724b6a8056d8dcde3eb229d4a9754372213d1cd0459a636cc1d`  
		Last Modified: Tue, 12 Nov 2024 15:38:45 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.8` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:c1dffbdd621d26db2705382efde17b701fc47c9f8cfaf615d5f97c1d639333cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94804611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84634ddb9071f382a213df9fd7c54243fc9438497747e24612a3d5f5dc6f9a5`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.2.8;     SWIPL_CHECKSUM=b331637a57c913c49edcfcb10ddcf6c031278ce93d2411d54542778531abb5c7;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a12bec5040e38e2a3fd6e76bc71d86a43b628b60cdfc3433840178d7ec515f3`  
		Last Modified: Tue, 12 Nov 2024 10:36:50 GMT  
		Size: 47.7 MB (47706414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f5f075eccffb4f018fcd03ed02d3fce251b3c6fdc8226d71899f6d9dadba8c`  
		Last Modified: Tue, 12 Nov 2024 10:43:20 GMT  
		Size: 17.9 MB (17940841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.8` - unknown; unknown

```console
$ docker pull swipl@sha256:cfcade3ab5f2e2ca9e5ec823c3472e96d15333beb541c2658bbbfab01af19fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102b4fb9dd32a29dc9ba98c58a1072478960babae012be47cca0c460098489f6`

```dockerfile
```

-	Layers:
	-	`sha256:55230ba367c34935362fdc38866c31ebcca5a1b1333916c4a92c2f772723dffc`  
		Last Modified: Tue, 12 Nov 2024 10:43:19 GMT  
		Size: 3.2 MB (3167572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e57fb79dcff598660520b1e0cbbc8c7bdf2424143a5b7383db60ff3ff1181b92`  
		Last Modified: Tue, 12 Nov 2024 10:43:18 GMT  
		Size: 17.6 KB (17602 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:9.3.16`

```console
$ docker pull swipl@sha256:02542931bfe2275cbe09f02694fcd9f60e38253e96c9671f798c79cffbd9c9ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.3.16` - linux; amd64

```console
$ docker pull swipl@sha256:5cc2dfdf3149f120a94f84892e498371451964b51814a72b21886355c424f50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97063456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b7e0ba60bcd19e0e013b3886f4411c0d30abf8c610d7f924b805f797ca628c`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 02 Dec 2024 15:14:22 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Mon, 02 Dec 2024 15:14:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 15:14:22 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 15:14:22 GMT
RUN set -eux;     SWIPL_VER=9.3.16;     SWIPL_CHECKSUM=24bb77a90259be48729861193865a7c46ce1b0234ff846e8bdb4990c36eed12a;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Mon, 02 Dec 2024 15:14:22 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55586f55e0bdb905f296b3426fa6174624343932f9447c138956ef3f98e9f134`  
		Last Modified: Mon, 02 Dec 2024 20:37:08 GMT  
		Size: 49.2 MB (49222706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824c188e300b68b43d363d6954505de410fd0d3dd17d7aa4d24b69342a31a4c1`  
		Last Modified: Mon, 02 Dec 2024 20:37:07 GMT  
		Size: 18.7 MB (18712755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.16` - unknown; unknown

```console
$ docker pull swipl@sha256:d97993504b6923173061c050e57bd064999891c732f46b4def0a0ea77ba7cb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3184752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7331ff1247fe078c3d48bb453d0a4fd76b8ce169af9c1b478d25ad6a110ca434`

```dockerfile
```

-	Layers:
	-	`sha256:d580066746958116c521fd3b26a1079122a11180ba4b13a9c99ef68b79c12b21`  
		Last Modified: Mon, 02 Dec 2024 20:37:07 GMT  
		Size: 3.2 MB (3167241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d169d49af9d8a4daf6dc05202e44f3019d164b948025e233d5092f5ac207bda0`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 17.5 KB (17511 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.16` - linux; arm variant v7

```console
$ docker pull swipl@sha256:bbad6e71362808d76fb1b47a4b44872bcdd02ebfbc73c71d603c327107d7d1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82773455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357288401bc4d7563834c7e5ed60b71fc388adcde05b65742d913fe2dde5920b`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 02 Dec 2024 15:14:22 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Mon, 02 Dec 2024 15:14:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 15:14:22 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 15:14:22 GMT
RUN set -eux;     SWIPL_VER=9.3.16;     SWIPL_CHECKSUM=24bb77a90259be48729861193865a7c46ce1b0234ff846e8bdb4990c36eed12a;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Mon, 02 Dec 2024 15:14:22 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da7007a03cac73be2169fa5ca584038434fa5be4b2634a843ee8cf6297ccb4f`  
		Last Modified: Mon, 02 Dec 2024 20:26:01 GMT  
		Size: 43.7 MB (43717250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc98a095a66d9b3cdbcd4d868448ad0fe5f37ce1d3245abbd5e723915726f831`  
		Last Modified: Mon, 02 Dec 2024 20:26:00 GMT  
		Size: 14.3 MB (14337296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.16` - unknown; unknown

```console
$ docker pull swipl@sha256:e208dda9a6552c4598a19b610a97665eae23908f3f402df7c6cb1068b397490a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3183696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c663a8f73ec08991a6f75b26bb156831e64d6c31db849fee51d6d667e0da6988`

```dockerfile
```

-	Layers:
	-	`sha256:17bfff15568cb518c054abfdffbb2385a6a9d052bdca0c448017afa5d8a5912f`  
		Last Modified: Mon, 02 Dec 2024 20:25:59 GMT  
		Size: 3.2 MB (3166113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b637f63ad7e3972754db3b93918536f8064dfbb23706e24100c9f93c936827`  
		Last Modified: Mon, 02 Dec 2024 20:25:59 GMT  
		Size: 17.6 KB (17583 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.16` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:b5ccf81798fc83dd98fa968aa7149fcab8e3e41880c12597d2d2dd21428c8a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94973559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed36853f90b18e1195bcee9459d7ec1d475626bbc92a66fb84a6bdbed8f4b185`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 02 Dec 2024 15:14:22 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Mon, 02 Dec 2024 15:14:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 15:14:22 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 15:14:22 GMT
RUN set -eux;     SWIPL_VER=9.3.16;     SWIPL_CHECKSUM=24bb77a90259be48729861193865a7c46ce1b0234ff846e8bdb4990c36eed12a;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Mon, 02 Dec 2024 15:14:22 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423ad570809959e63c4b39536d11123e354a4b90ba07500bba9a10b2faa11315`  
		Last Modified: Mon, 02 Dec 2024 20:31:15 GMT  
		Size: 47.7 MB (47706424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a99b9b205350d179a41dbc9982ebddf26fe27895724cfe8be82f7d540062e4`  
		Last Modified: Mon, 02 Dec 2024 20:31:12 GMT  
		Size: 18.1 MB (18109779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.16` - unknown; unknown

```console
$ docker pull swipl@sha256:a20d899c047c7ea3d9d61bab46b7e70d43079626f2febeef7891a72727645295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c473b2f34367682bbcc69bd7f9323165c42dede75f13ec99551dd029d0e3f960`

```dockerfile
```

-	Layers:
	-	`sha256:0145ed83b655b658f7d0a82b882670c36f347126d26da52b99012b750fedfa23`  
		Last Modified: Mon, 02 Dec 2024 20:31:11 GMT  
		Size: 3.2 MB (3167580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15326420b9cebb08cc1594321f027b786bfcd33faa2331b0cc0537f8bc8b3908`  
		Last Modified: Mon, 02 Dec 2024 20:31:11 GMT  
		Size: 17.6 KB (17606 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:latest`

```console
$ docker pull swipl@sha256:02542931bfe2275cbe09f02694fcd9f60e38253e96c9671f798c79cffbd9c9ad
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
$ docker pull swipl@sha256:5cc2dfdf3149f120a94f84892e498371451964b51814a72b21886355c424f50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97063456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b7e0ba60bcd19e0e013b3886f4411c0d30abf8c610d7f924b805f797ca628c`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 02 Dec 2024 15:14:22 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Mon, 02 Dec 2024 15:14:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 15:14:22 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 15:14:22 GMT
RUN set -eux;     SWIPL_VER=9.3.16;     SWIPL_CHECKSUM=24bb77a90259be48729861193865a7c46ce1b0234ff846e8bdb4990c36eed12a;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Mon, 02 Dec 2024 15:14:22 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55586f55e0bdb905f296b3426fa6174624343932f9447c138956ef3f98e9f134`  
		Last Modified: Mon, 02 Dec 2024 20:37:08 GMT  
		Size: 49.2 MB (49222706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824c188e300b68b43d363d6954505de410fd0d3dd17d7aa4d24b69342a31a4c1`  
		Last Modified: Mon, 02 Dec 2024 20:37:07 GMT  
		Size: 18.7 MB (18712755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:d97993504b6923173061c050e57bd064999891c732f46b4def0a0ea77ba7cb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3184752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7331ff1247fe078c3d48bb453d0a4fd76b8ce169af9c1b478d25ad6a110ca434`

```dockerfile
```

-	Layers:
	-	`sha256:d580066746958116c521fd3b26a1079122a11180ba4b13a9c99ef68b79c12b21`  
		Last Modified: Mon, 02 Dec 2024 20:37:07 GMT  
		Size: 3.2 MB (3167241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d169d49af9d8a4daf6dc05202e44f3019d164b948025e233d5092f5ac207bda0`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 17.5 KB (17511 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:bbad6e71362808d76fb1b47a4b44872bcdd02ebfbc73c71d603c327107d7d1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82773455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357288401bc4d7563834c7e5ed60b71fc388adcde05b65742d913fe2dde5920b`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 02 Dec 2024 15:14:22 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Mon, 02 Dec 2024 15:14:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 15:14:22 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 15:14:22 GMT
RUN set -eux;     SWIPL_VER=9.3.16;     SWIPL_CHECKSUM=24bb77a90259be48729861193865a7c46ce1b0234ff846e8bdb4990c36eed12a;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Mon, 02 Dec 2024 15:14:22 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da7007a03cac73be2169fa5ca584038434fa5be4b2634a843ee8cf6297ccb4f`  
		Last Modified: Mon, 02 Dec 2024 20:26:01 GMT  
		Size: 43.7 MB (43717250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc98a095a66d9b3cdbcd4d868448ad0fe5f37ce1d3245abbd5e723915726f831`  
		Last Modified: Mon, 02 Dec 2024 20:26:00 GMT  
		Size: 14.3 MB (14337296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:e208dda9a6552c4598a19b610a97665eae23908f3f402df7c6cb1068b397490a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3183696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c663a8f73ec08991a6f75b26bb156831e64d6c31db849fee51d6d667e0da6988`

```dockerfile
```

-	Layers:
	-	`sha256:17bfff15568cb518c054abfdffbb2385a6a9d052bdca0c448017afa5d8a5912f`  
		Last Modified: Mon, 02 Dec 2024 20:25:59 GMT  
		Size: 3.2 MB (3166113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b637f63ad7e3972754db3b93918536f8064dfbb23706e24100c9f93c936827`  
		Last Modified: Mon, 02 Dec 2024 20:25:59 GMT  
		Size: 17.6 KB (17583 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:b5ccf81798fc83dd98fa968aa7149fcab8e3e41880c12597d2d2dd21428c8a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94973559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed36853f90b18e1195bcee9459d7ec1d475626bbc92a66fb84a6bdbed8f4b185`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 02 Dec 2024 15:14:22 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Mon, 02 Dec 2024 15:14:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 15:14:22 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 15:14:22 GMT
RUN set -eux;     SWIPL_VER=9.3.16;     SWIPL_CHECKSUM=24bb77a90259be48729861193865a7c46ce1b0234ff846e8bdb4990c36eed12a;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Mon, 02 Dec 2024 15:14:22 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423ad570809959e63c4b39536d11123e354a4b90ba07500bba9a10b2faa11315`  
		Last Modified: Mon, 02 Dec 2024 20:31:15 GMT  
		Size: 47.7 MB (47706424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a99b9b205350d179a41dbc9982ebddf26fe27895724cfe8be82f7d540062e4`  
		Last Modified: Mon, 02 Dec 2024 20:31:12 GMT  
		Size: 18.1 MB (18109779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:a20d899c047c7ea3d9d61bab46b7e70d43079626f2febeef7891a72727645295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c473b2f34367682bbcc69bd7f9323165c42dede75f13ec99551dd029d0e3f960`

```dockerfile
```

-	Layers:
	-	`sha256:0145ed83b655b658f7d0a82b882670c36f347126d26da52b99012b750fedfa23`  
		Last Modified: Mon, 02 Dec 2024 20:31:11 GMT  
		Size: 3.2 MB (3167580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15326420b9cebb08cc1594321f027b786bfcd33faa2331b0cc0537f8bc8b3908`  
		Last Modified: Mon, 02 Dec 2024 20:31:11 GMT  
		Size: 17.6 KB (17606 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:stable`

```console
$ docker pull swipl@sha256:9dc59e189a176cd54da83aca7331d9158c93846e37fbf072a7c7fd2f5d85bd17
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
$ docker pull swipl@sha256:9d88196372ae372366c3521e128ce53d294ce9d18c4212d2f71dceaba4f93481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96896551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d36b32fd16c03219714ae384c3f80c0c6856019d2d3b111554e8d608be4b3dc`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.2.8;     SWIPL_CHECKSUM=b331637a57c913c49edcfcb10ddcf6c031278ce93d2411d54542778531abb5c7;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03630e44222222e34a9b723b7ebdddaf0d55bbedbfda113c1cef30bbe06dbafe`  
		Last Modified: Tue, 12 Nov 2024 02:24:23 GMT  
		Size: 49.2 MB (49222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618ebb0d6203ef8afe7f315237fa04971cbecbfffe362caca2c375b2850cbfc1`  
		Last Modified: Tue, 12 Nov 2024 02:24:23 GMT  
		Size: 18.5 MB (18545882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:0e34b6884630329fbb2fdd982ddf1b3143ff7abbd46ecc0a13b1d16c02291562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3184740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2344c1a670c92b8e1a6258d684c204502bdc2902fae5f77de76d0d19bd672b77`

```dockerfile
```

-	Layers:
	-	`sha256:a31ecbc89b4dbdb7b4afedddda43a7bd363fb838af0ed8d6a03d18e5a83fe44a`  
		Last Modified: Tue, 12 Nov 2024 02:24:22 GMT  
		Size: 3.2 MB (3167233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2136514aad85ed501329dd609915e59b537ae41178e61efa73e1c541975ac6c9`  
		Last Modified: Tue, 12 Nov 2024 02:24:22 GMT  
		Size: 17.5 KB (17507 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:39e0c511b6588a112609acf7228031dce6412cd4c863a439819070684521d453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82551347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732a2ce37028b30735dd8dc8df77493163b96c7f872ac69f758eafa3c5ddcc14`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.2.8;     SWIPL_CHECKSUM=b331637a57c913c49edcfcb10ddcf6c031278ce93d2411d54542778531abb5c7;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5c21fa4169213eb4e571405f837875ed102be8e3d768c9af90bff7c9ccd3e0`  
		Last Modified: Tue, 12 Nov 2024 15:35:09 GMT  
		Size: 43.7 MB (43717482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7063cac71067db6a15373f76d8f0a1928fdf860afe6bcce182849b8b5df12e7`  
		Last Modified: Tue, 12 Nov 2024 15:38:46 GMT  
		Size: 14.1 MB (14114956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:7bc6be22081abf215d35b97b68989efdf7bdd5c04e300337e4106e9b668ea7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3183683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f1919e4f284f3f93a025eb5478916774bd544882ecdc5f013927f72b24e803`

```dockerfile
```

-	Layers:
	-	`sha256:c9db1eb29b243b33e6c076ce21c31140feafb9ec00c73d55547b7d8484ffc940`  
		Last Modified: Tue, 12 Nov 2024 15:38:46 GMT  
		Size: 3.2 MB (3166105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b873c4d4c175e724b6a8056d8dcde3eb229d4a9754372213d1cd0459a636cc1d`  
		Last Modified: Tue, 12 Nov 2024 15:38:45 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:c1dffbdd621d26db2705382efde17b701fc47c9f8cfaf615d5f97c1d639333cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94804611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84634ddb9071f382a213df9fd7c54243fc9438497747e24612a3d5f5dc6f9a5`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 31 Oct 2024 13:50:48 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["bash"]
# Thu, 31 Oct 2024 13:50:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 31 Oct 2024 13:50:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2024 13:50:48 GMT
RUN set -eux;     SWIPL_VER=9.2.8;     SWIPL_CHECKSUM=b331637a57c913c49edcfcb10ddcf6c031278ce93d2411d54542778531abb5c7;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 31 Oct 2024 13:50:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a12bec5040e38e2a3fd6e76bc71d86a43b628b60cdfc3433840178d7ec515f3`  
		Last Modified: Tue, 12 Nov 2024 10:36:50 GMT  
		Size: 47.7 MB (47706414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f5f075eccffb4f018fcd03ed02d3fce251b3c6fdc8226d71899f6d9dadba8c`  
		Last Modified: Tue, 12 Nov 2024 10:43:20 GMT  
		Size: 17.9 MB (17940841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:cfcade3ab5f2e2ca9e5ec823c3472e96d15333beb541c2658bbbfab01af19fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102b4fb9dd32a29dc9ba98c58a1072478960babae012be47cca0c460098489f6`

```dockerfile
```

-	Layers:
	-	`sha256:55230ba367c34935362fdc38866c31ebcca5a1b1333916c4a92c2f772723dffc`  
		Last Modified: Tue, 12 Nov 2024 10:43:19 GMT  
		Size: 3.2 MB (3167572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e57fb79dcff598660520b1e0cbbc8c7bdf2424143a5b7383db60ff3ff1181b92`  
		Last Modified: Tue, 12 Nov 2024 10:43:18 GMT  
		Size: 17.6 KB (17602 bytes)  
		MIME: application/vnd.in-toto+json
