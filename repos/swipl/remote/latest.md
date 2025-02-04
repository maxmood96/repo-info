## `swipl:latest`

```console
$ docker pull swipl@sha256:c854ec99f266f9f592daa3ba783e191adddda564504dd64c69af18d870b15774
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
$ docker pull swipl@sha256:594cd35623723d284be82b81b722ce530fa9c65266e66f82554c39dccb1b616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96167207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629fda81fd3ec18988a7e6bdd443199792da2dc3b0c34810f7a3b73bc5d1ec75`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 07 Jan 2025 09:48:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9282b047df2578dc4e7761898dd9a5ca3aa4b131e0fe7db9b809c970d5340c28`  
		Last Modified: Tue, 04 Feb 2025 04:36:28 GMT  
		Size: 49.2 MB (49219240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426f7cabf21369690f0ac0798f214e5de2e997fb3e0edeccd667fd5d2e3947c8`  
		Last Modified: Tue, 04 Feb 2025 04:36:27 GMT  
		Size: 18.7 MB (18735664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:f6dba4bc986b49e322943f70c3916e0ca8efea22f695388641baca714466680a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839c8903640594c9d18ba7b75e70a219d73ba3a3a87ae07aeb6a2727ae027a15`

```dockerfile
```

-	Layers:
	-	`sha256:38ad9b492e2288b6908cf9c141d2627a73250faec69bb410808879f8fffe60ca`  
		Last Modified: Tue, 04 Feb 2025 04:36:30 GMT  
		Size: 3.2 MB (3157140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed852924e6e0352070fda802b3cf9ca74780b17cefd9c92998a822bde81024e`  
		Last Modified: Tue, 04 Feb 2025 04:36:26 GMT  
		Size: 17.5 KB (17511 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:fd46395784e9cc670ac949024ddcbbf306fa4ab63bd0f115c10cb4166c6ff41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81998724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9172aa05fc232391cd664cad40161af75198942a7845f73a155bd370982c65d`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 07 Jan 2025 09:48:06 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
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
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3517d371abafb3298696e91e85cd4a3db7f8a004e64a174c4d4733eaf77bba`  
		Last Modified: Tue, 04 Feb 2025 10:29:46 GMT  
		Size: 43.7 MB (43734261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec32db8096e842e36f1c9d05b9b61bd20267917f125a474150b6314c2ed2b64`  
		Last Modified: Tue, 04 Feb 2025 10:29:45 GMT  
		Size: 14.3 MB (14349927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:33083ddc3ed91d0c5c28a8312392be72f3f2f9d5554154e0be565f923bf0a2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dca2e72a6a64423ab9cf38198b9e941cf90aec3c53b694241b3b2087eb3d600`

```dockerfile
```

-	Layers:
	-	`sha256:29eb638ecc4c2605575e43b06173e277a322239befa5af481a2a5192f7ce9f69`  
		Last Modified: Tue, 04 Feb 2025 10:29:44 GMT  
		Size: 3.2 MB (3160888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57db51c6cc176d416edd3fd3fe4061ed5f03c937e2d5441f9498dfbf1e4accf`  
		Last Modified: Tue, 04 Feb 2025 10:29:44 GMT  
		Size: 17.6 KB (17584 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:76206eaeaf71aff0889d0c24898d8acec936c08eebf46bd417357cd84c300ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93885836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5957217a3e8ba283f17f3906da58500afd194d4a5e96bdd4ce6f4fdfbf19ee16`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 07 Jan 2025 09:48:06 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af56b7985b3095908fa758d5bc4193d7fae55070fdae45fa434920a30d3b7d9`  
		Last Modified: Tue, 04 Feb 2025 08:43:14 GMT  
		Size: 47.7 MB (47713570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1797736aaeaae298bb44d7aeb106d3fe8092d86221cae4f8c6b993e5fd1dc743`  
		Last Modified: Tue, 04 Feb 2025 08:43:14 GMT  
		Size: 18.1 MB (18131385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:27fed47c264a738991c99c6602efc61756c434f2ad7474c3ea14d7d4cb478ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b012015c6f1519a66ae034aee05844d87d4a823821af651b284d28e2deb0b3`

```dockerfile
```

-	Layers:
	-	`sha256:bb12b9bcfc1c801cf3c7b1cbe9ad4a3cfbcbdb9d72dd7e207abb1f0a044a2919`  
		Last Modified: Tue, 04 Feb 2025 08:43:13 GMT  
		Size: 3.2 MB (3162382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:696fff753176e1ef6442933afcd1abde56652387d2f84ae355884ef3bd7b9a60`  
		Last Modified: Tue, 04 Feb 2025 08:43:13 GMT  
		Size: 17.6 KB (17605 bytes)  
		MIME: application/vnd.in-toto+json
