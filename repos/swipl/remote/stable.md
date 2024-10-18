## `swipl:stable`

```console
$ docker pull swipl@sha256:b0420b8b4c4e33ae80f382fb8129f425778cee9c3283e57bd35e4057998defed
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
$ docker pull swipl@sha256:e33072191af9862d96e61f7cf0676fb5cfd544f4eb2313427c02445d0dd97f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96883315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af58ef2976963a36bb8600f254239956239be1f96704354a564b552add6bbb4e`
-	Default Command: `["swipl"]`

```dockerfile
# Sat, 12 Oct 2024 13:28:48 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 12 Oct 2024 13:28:48 GMT
CMD ["bash"]
# Sat, 12 Oct 2024 13:28:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 12 Oct 2024 13:28:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
ENV LANG=C.UTF-8
# Sat, 12 Oct 2024 13:28:48 GMT
RUN set -eux;     SWIPL_VER=9.2.7;     SWIPL_CHECKSUM=fd4126f047e0784112741a874e2f7f8c68b5edd6426ded621df355c62d18c96f;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 831482c8f267e002147dc482c4e6509f9e27d97e;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024f6f92f5aab2a8257de6d5ae6fed100b60f4a251588fd0cc9cb4987845395e`  
		Last Modified: Thu, 17 Oct 2024 01:43:31 GMT  
		Size: 49.2 MB (49220467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e853424fab8c43c9329270531c33d99edf0216b0eb935a564c05e739ef1b6`  
		Last Modified: Thu, 17 Oct 2024 01:43:30 GMT  
		Size: 18.5 MB (18536559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:30ff0a71e2cb5a351151cb2960da9938ff502b44e2a5cde5a62b5b213578474d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221255a162a5d0eb81b90ed02c9f31cf501b92b4474e128b94bcdc6023b4d0cb`

```dockerfile
```

-	Layers:
	-	`sha256:6a0fe568d4225380456d2dbddc55cb9dc0bb2328ea0e41b9d8bf80cd86333d84`  
		Last Modified: Thu, 17 Oct 2024 01:43:30 GMT  
		Size: 3.1 MB (3144006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f934306aceb1469e11358f924ff10dd77b4d0b4e8d2718824857b1ee21b478dd`  
		Last Modified: Thu, 17 Oct 2024 01:43:29 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:6a30ed7d8e3aca64bd0200bbe7ea5f43b75189e9eed2a6750ff5484163443ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82542037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3b612f61c190cb0ac1786067a5a0df23a5c0e29710eac3788357a8e0106621`
-	Default Command: `["swipl"]`

```dockerfile
# Sun, 08 Sep 2024 08:35:01 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["bash"]
# Sun, 08 Sep 2024 08:35:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sun, 08 Sep 2024 08:35:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 08:35:01 GMT
RUN set -eux;     SWIPL_VER=9.2.7;     SWIPL_CHECKSUM=fd4126f047e0784112741a874e2f7f8c68b5edd6426ded621df355c62d18c96f;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 831482c8f267e002147dc482c4e6509f9e27d97e;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8d771fa51d762ca800a343818d5089f10d021da236680cc8107ca03281d773`  
		Last Modified: Fri, 27 Sep 2024 18:46:50 GMT  
		Size: 43.7 MB (43723801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67dacbc6474460889de723d9555230cc20c6a19d2cced207ca05192a6dc4703`  
		Last Modified: Fri, 27 Sep 2024 18:49:26 GMT  
		Size: 14.1 MB (14100091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:64cc8b386073a716897780845fcf666bfbfb1af2f5696d7caf60fcac2e17ff2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3163890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85751c47abe2ba0f985f9186e33606d40dbf8742116e2b333921cf669b8cc8ab`

```dockerfile
```

-	Layers:
	-	`sha256:f98bc0e5645cd429d5f23c0393c7a613d069746b43e2c90ec9301d4854f95af0`  
		Last Modified: Fri, 27 Sep 2024 18:49:25 GMT  
		Size: 3.1 MB (3146528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198b6ee780ce35b06e5e182cc0fb29056e0b8700303100459553ff8c548825f1`  
		Last Modified: Fri, 27 Sep 2024 18:49:25 GMT  
		Size: 17.4 KB (17362 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:f9a444342c196cfb302f464ae29a7d290a2e4fc6a9681d591ee0e24f256eaa4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94806965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff80cf5a4fa31dbff5e42520a8d14715794ea5d297a1290770b8aca5b1265642`
-	Default Command: `["swipl"]`

```dockerfile
# Sat, 12 Oct 2024 13:28:48 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 12 Oct 2024 13:28:48 GMT
CMD ["bash"]
# Sat, 12 Oct 2024 13:28:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 12 Oct 2024 13:28:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
ENV LANG=C.UTF-8
# Sat, 12 Oct 2024 13:28:48 GMT
RUN set -eux;     SWIPL_VER=9.2.7;     SWIPL_CHECKSUM=fd4126f047e0784112741a874e2f7f8c68b5edd6426ded621df355c62d18c96f;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 831482c8f267e002147dc482c4e6509f9e27d97e;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580843dae774c35056112d034bbdef9e3e8d54020402f7e2b6d716a8d6d2fe1f`  
		Last Modified: Thu, 17 Oct 2024 21:15:02 GMT  
		Size: 47.7 MB (47712926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e1dc07b122361da917b6e8341d1684cff8bfee600a1b50052ab0532b305115`  
		Last Modified: Thu, 17 Oct 2024 21:21:29 GMT  
		Size: 17.9 MB (17937698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:87dd2b859711156d45af75ee68264cc4894467b866f7b0e9637fd020a9c14ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613b36ea9c900a6460b4a53f4cc323fc7ba7e07f5a14b62c8a11ebe1e5482003`

```dockerfile
```

-	Layers:
	-	`sha256:813509a98c5a72e67cbaeb20e119516033e34957cae4df6ecdb2024496799d1f`  
		Last Modified: Thu, 17 Oct 2024 21:21:29 GMT  
		Size: 3.1 MB (3144345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:678db6360995cc6bbcd4ad950cf64a8165a5dd012f00e338e4732b42badfe3a2`  
		Last Modified: Thu, 17 Oct 2024 21:21:29 GMT  
		Size: 17.4 KB (17421 bytes)  
		MIME: application/vnd.in-toto+json
