<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:9.2.7`](#swipl927)
-	[`swipl:9.3.11`](#swipl9311)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:9.2.7`

```console
$ docker pull swipl@sha256:404057425c1825723ea19f1571a834bb837979d854aee7f34c1263e22ffae2a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.2.7` - linux; amd64

```console
$ docker pull swipl@sha256:399d4bf25598f1bb660f790a67a5d5a0f712ed543df1dcd0f938a36c1a7324ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96883613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a13b41e31c4c2a4f7aed0b86d661cb74e729222fe44dda3b4469069a636661f`
-	Default Command: `["swipl"]`

```dockerfile
# Sun, 08 Sep 2024 08:35:01 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d3c56cbb305fc9b08ae3ec862821e67a88519aff04e00a12b9e23a0133cfa`  
		Last Modified: Fri, 27 Sep 2024 06:28:13 GMT  
		Size: 49.2 MB (49221386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b15ad4409e9ffab98148ee1456be31a987166b74e4b1d507b351d7958b81b0`  
		Last Modified: Fri, 27 Sep 2024 06:28:12 GMT  
		Size: 18.5 MB (18535951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.7` - unknown; unknown

```console
$ docker pull swipl@sha256:8c1344e4c183fdb2df42a76c60c67cc28f9f1c3d16462dc185e38b48e53501b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cfeca2ed24c07ba39434782e707f7b4cea7f90548203eccc58ee30306b94a1`

```dockerfile
```

-	Layers:
	-	`sha256:ed5c5df645542daadc7fbb412bad2b66bdf87c4e75169bb162c949a899c08384`  
		Last Modified: Fri, 27 Sep 2024 06:28:12 GMT  
		Size: 3.1 MB (3144006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e0b94326a2037e898aaed8aeb1a35fa1a022a8c6cbd6c88f20fb14d54b9826`  
		Last Modified: Fri, 27 Sep 2024 06:28:12 GMT  
		Size: 17.3 KB (17294 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.7` - linux; arm variant v7

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

### `swipl:9.2.7` - unknown; unknown

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

### `swipl:9.2.7` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:26fbe60d1420ce3a157368ea4519141a8120995394eef8cd66f4cf324141a2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94807981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a53c47a17612bcadd0afea706ed5f40cd6db579e8e144f2850315f5fc1a75c`
-	Default Command: `["swipl"]`

```dockerfile
# Sun, 08 Sep 2024 08:35:01 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04be04db0f19489d1a2e0da09b7d8d2de707ee700e26000abcee5d02fd0df4bb`  
		Last Modified: Fri, 27 Sep 2024 23:46:59 GMT  
		Size: 47.7 MB (47713641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208f713269b79427ec7c2b96171913419e39fa1314e45dd7747ae7a20846680a`  
		Last Modified: Fri, 27 Sep 2024 23:53:22 GMT  
		Size: 17.9 MB (17937971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.7` - unknown; unknown

```console
$ docker pull swipl@sha256:379bbc4a063fc6b476def5d428bcb4f80dc40bd4790aada328062c78cc544677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ecb1f9d9a7e4e4af76806110d4e78136283d9ed27581366bf848e811ec8e04`

```dockerfile
```

-	Layers:
	-	`sha256:67112c63ba0d716c1fe17e7c1e6cc637caab52a902ebfd998e62a906d70c66f6`  
		Last Modified: Fri, 27 Sep 2024 23:53:22 GMT  
		Size: 3.1 MB (3144345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7123eaf64c9663b226ccf8d4660426477027bc95b086e49d93dcc9162ac41ee`  
		Last Modified: Fri, 27 Sep 2024 23:53:21 GMT  
		Size: 17.6 KB (17580 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:9.3.11`

```console
$ docker pull swipl@sha256:3795310d9c33cd03f5215403c46e9fc9943ede2898b3b4c45640c663acc72dfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.3.11` - linux; amd64

```console
$ docker pull swipl@sha256:f789ca0ffe5c659b89a3544cd48bd9e06f6a4821909ab2d938786fa539806c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97023100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0777a14981e84cd676578770b091449ba5d9985feb2aaeb1ad31995f6fc1459d`
-	Default Command: `["swipl"]`

```dockerfile
# Sun, 08 Sep 2024 08:35:01 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["bash"]
# Sun, 08 Sep 2024 08:35:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sun, 08 Sep 2024 08:35:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 08:35:01 GMT
RUN set -eux;     SWIPL_VER=9.3.11;     SWIPL_CHECKSUM=b8bffac671ee031ee34d033c168fed0a6f4ea0a906e2a13f5a19f00b59cd4b55;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1deec53db446ab1709ef3aa348656dba6b9dc509b13f867952a832ff22777a`  
		Last Modified: Fri, 27 Sep 2024 06:29:32 GMT  
		Size: 49.2 MB (49221421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aae806d14b17be1cf23518674a1f5bf906babdce758eba51caae703f5814a8`  
		Last Modified: Fri, 27 Sep 2024 06:29:31 GMT  
		Size: 18.7 MB (18675403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.11` - unknown; unknown

```console
$ docker pull swipl@sha256:fe5d3f699a02942512bc8dae5156241c566359f1960c461b43d0859dc1077735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b62cfea7380055f1ca2170440f23a9ea3d685e9d1c8a5f1377e2e84261ccc2b`

```dockerfile
```

-	Layers:
	-	`sha256:b931cbeaf4536f79ba729f06b90a6d0a61bfa150848e425079bc08f9393102f3`  
		Last Modified: Fri, 27 Sep 2024 06:29:31 GMT  
		Size: 3.1 MB (3144010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:732231b17e5a71cc9c681a9f31c415c16212ac782e75c5ade7b810a844401b4c`  
		Last Modified: Fri, 27 Sep 2024 06:29:30 GMT  
		Size: 17.3 KB (17299 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.11` - linux; arm variant v7

```console
$ docker pull swipl@sha256:0ce869d3b60e1f4ec28b6eeeaeae674d2ab0f7814fe9b9120139c75e1f35d1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82738087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad3aac2c6692ec8aebb750947f6c191d3b8efd305c894ceb0314408c123edfa`
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
RUN set -eux;     SWIPL_VER=9.3.11;     SWIPL_CHECKSUM=b8bffac671ee031ee34d033c168fed0a6f4ea0a906e2a13f5a19f00b59cd4b55;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
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
	-	`sha256:43a551053fc0e4035d9613521d16b45478eec4314eec7f5d3610e6c08bb2a335`  
		Last Modified: Fri, 27 Sep 2024 18:46:49 GMT  
		Size: 14.3 MB (14296141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.11` - unknown; unknown

```console
$ docker pull swipl@sha256:c5a04391b1ce65cc79766054723b4d9b8a72cd5a81fd95340cd2cd59fcf6c7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3163898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14996b6f2d0f9fc226dc7ba3d65b3b62d6874cba200763a0f64f0aef4c362aa1`

```dockerfile
```

-	Layers:
	-	`sha256:cce116daf4fccefaf7d041551b8731fdd4d0afe40235886d7c09fdc527f7ad18`  
		Last Modified: Fri, 27 Sep 2024 18:46:49 GMT  
		Size: 3.1 MB (3146532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6c9ddfde98d6c0fa052a5b3764e5f326ca3586bb0a1ba78c24812ca5c6da779`  
		Last Modified: Fri, 27 Sep 2024 18:46:48 GMT  
		Size: 17.4 KB (17366 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.11` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:96d7f7bd8ed4bbb48d8e12f872efee0fb350493c3ca6b35adf735ef671fd9b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94931752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3102e99096d4a17624fb4d2f188df07cf96fbae5cbcadced1f4ba6020a2b693b`
-	Default Command: `["swipl"]`

```dockerfile
# Sun, 08 Sep 2024 08:35:01 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["bash"]
# Sun, 08 Sep 2024 08:35:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sun, 08 Sep 2024 08:35:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 08:35:01 GMT
RUN set -eux;     SWIPL_VER=9.3.11;     SWIPL_CHECKSUM=b8bffac671ee031ee34d033c168fed0a6f4ea0a906e2a13f5a19f00b59cd4b55;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04be04db0f19489d1a2e0da09b7d8d2de707ee700e26000abcee5d02fd0df4bb`  
		Last Modified: Fri, 27 Sep 2024 23:46:59 GMT  
		Size: 47.7 MB (47713641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c408468d04662284a3ebd37bb6e409907125e77e46ade000e23c095fa76c63af`  
		Last Modified: Fri, 27 Sep 2024 23:46:58 GMT  
		Size: 18.1 MB (18061742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.11` - unknown; unknown

```console
$ docker pull swipl@sha256:e32a9d80d6ca9637ddc52bbae3b47bdc76d39eb2e6905a5a7ceba30dd465644a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d591e5c69236198566629e8396459631487a5041c7bb88e6110b66b459f09e9`

```dockerfile
```

-	Layers:
	-	`sha256:20175c78fb32b2e1b300caf0219a0ffd886151df5be08289543ad3298bbac2d1`  
		Last Modified: Fri, 27 Sep 2024 23:46:58 GMT  
		Size: 3.1 MB (3144349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f280cd7dd5656465aa72c9a9ba77338595d846f470a7c4c9986e9c60cd02f91`  
		Last Modified: Fri, 27 Sep 2024 23:46:57 GMT  
		Size: 17.6 KB (17584 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:latest`

```console
$ docker pull swipl@sha256:3795310d9c33cd03f5215403c46e9fc9943ede2898b3b4c45640c663acc72dfa
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
$ docker pull swipl@sha256:f789ca0ffe5c659b89a3544cd48bd9e06f6a4821909ab2d938786fa539806c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97023100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0777a14981e84cd676578770b091449ba5d9985feb2aaeb1ad31995f6fc1459d`
-	Default Command: `["swipl"]`

```dockerfile
# Sun, 08 Sep 2024 08:35:01 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["bash"]
# Sun, 08 Sep 2024 08:35:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sun, 08 Sep 2024 08:35:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 08:35:01 GMT
RUN set -eux;     SWIPL_VER=9.3.11;     SWIPL_CHECKSUM=b8bffac671ee031ee34d033c168fed0a6f4ea0a906e2a13f5a19f00b59cd4b55;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1deec53db446ab1709ef3aa348656dba6b9dc509b13f867952a832ff22777a`  
		Last Modified: Fri, 27 Sep 2024 06:29:32 GMT  
		Size: 49.2 MB (49221421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aae806d14b17be1cf23518674a1f5bf906babdce758eba51caae703f5814a8`  
		Last Modified: Fri, 27 Sep 2024 06:29:31 GMT  
		Size: 18.7 MB (18675403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:fe5d3f699a02942512bc8dae5156241c566359f1960c461b43d0859dc1077735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b62cfea7380055f1ca2170440f23a9ea3d685e9d1c8a5f1377e2e84261ccc2b`

```dockerfile
```

-	Layers:
	-	`sha256:b931cbeaf4536f79ba729f06b90a6d0a61bfa150848e425079bc08f9393102f3`  
		Last Modified: Fri, 27 Sep 2024 06:29:31 GMT  
		Size: 3.1 MB (3144010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:732231b17e5a71cc9c681a9f31c415c16212ac782e75c5ade7b810a844401b4c`  
		Last Modified: Fri, 27 Sep 2024 06:29:30 GMT  
		Size: 17.3 KB (17299 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:0ce869d3b60e1f4ec28b6eeeaeae674d2ab0f7814fe9b9120139c75e1f35d1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82738087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad3aac2c6692ec8aebb750947f6c191d3b8efd305c894ceb0314408c123edfa`
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
RUN set -eux;     SWIPL_VER=9.3.11;     SWIPL_CHECKSUM=b8bffac671ee031ee34d033c168fed0a6f4ea0a906e2a13f5a19f00b59cd4b55;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
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
	-	`sha256:43a551053fc0e4035d9613521d16b45478eec4314eec7f5d3610e6c08bb2a335`  
		Last Modified: Fri, 27 Sep 2024 18:46:49 GMT  
		Size: 14.3 MB (14296141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:c5a04391b1ce65cc79766054723b4d9b8a72cd5a81fd95340cd2cd59fcf6c7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3163898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14996b6f2d0f9fc226dc7ba3d65b3b62d6874cba200763a0f64f0aef4c362aa1`

```dockerfile
```

-	Layers:
	-	`sha256:cce116daf4fccefaf7d041551b8731fdd4d0afe40235886d7c09fdc527f7ad18`  
		Last Modified: Fri, 27 Sep 2024 18:46:49 GMT  
		Size: 3.1 MB (3146532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6c9ddfde98d6c0fa052a5b3764e5f326ca3586bb0a1ba78c24812ca5c6da779`  
		Last Modified: Fri, 27 Sep 2024 18:46:48 GMT  
		Size: 17.4 KB (17366 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:96d7f7bd8ed4bbb48d8e12f872efee0fb350493c3ca6b35adf735ef671fd9b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94931752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3102e99096d4a17624fb4d2f188df07cf96fbae5cbcadced1f4ba6020a2b693b`
-	Default Command: `["swipl"]`

```dockerfile
# Sun, 08 Sep 2024 08:35:01 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["bash"]
# Sun, 08 Sep 2024 08:35:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sun, 08 Sep 2024 08:35:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 08:35:01 GMT
RUN set -eux;     SWIPL_VER=9.3.11;     SWIPL_CHECKSUM=b8bffac671ee031ee34d033c168fed0a6f4ea0a906e2a13f5a19f00b59cd4b55;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sun, 08 Sep 2024 08:35:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04be04db0f19489d1a2e0da09b7d8d2de707ee700e26000abcee5d02fd0df4bb`  
		Last Modified: Fri, 27 Sep 2024 23:46:59 GMT  
		Size: 47.7 MB (47713641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c408468d04662284a3ebd37bb6e409907125e77e46ade000e23c095fa76c63af`  
		Last Modified: Fri, 27 Sep 2024 23:46:58 GMT  
		Size: 18.1 MB (18061742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:e32a9d80d6ca9637ddc52bbae3b47bdc76d39eb2e6905a5a7ceba30dd465644a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d591e5c69236198566629e8396459631487a5041c7bb88e6110b66b459f09e9`

```dockerfile
```

-	Layers:
	-	`sha256:20175c78fb32b2e1b300caf0219a0ffd886151df5be08289543ad3298bbac2d1`  
		Last Modified: Fri, 27 Sep 2024 23:46:58 GMT  
		Size: 3.1 MB (3144349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f280cd7dd5656465aa72c9a9ba77338595d846f470a7c4c9986e9c60cd02f91`  
		Last Modified: Fri, 27 Sep 2024 23:46:57 GMT  
		Size: 17.6 KB (17584 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:stable`

```console
$ docker pull swipl@sha256:404057425c1825723ea19f1571a834bb837979d854aee7f34c1263e22ffae2a3
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
$ docker pull swipl@sha256:399d4bf25598f1bb660f790a67a5d5a0f712ed543df1dcd0f938a36c1a7324ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96883613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a13b41e31c4c2a4f7aed0b86d661cb74e729222fe44dda3b4469069a636661f`
-	Default Command: `["swipl"]`

```dockerfile
# Sun, 08 Sep 2024 08:35:01 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d3c56cbb305fc9b08ae3ec862821e67a88519aff04e00a12b9e23a0133cfa`  
		Last Modified: Fri, 27 Sep 2024 06:28:13 GMT  
		Size: 49.2 MB (49221386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b15ad4409e9ffab98148ee1456be31a987166b74e4b1d507b351d7958b81b0`  
		Last Modified: Fri, 27 Sep 2024 06:28:12 GMT  
		Size: 18.5 MB (18535951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:8c1344e4c183fdb2df42a76c60c67cc28f9f1c3d16462dc185e38b48e53501b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cfeca2ed24c07ba39434782e707f7b4cea7f90548203eccc58ee30306b94a1`

```dockerfile
```

-	Layers:
	-	`sha256:ed5c5df645542daadc7fbb412bad2b66bdf87c4e75169bb162c949a899c08384`  
		Last Modified: Fri, 27 Sep 2024 06:28:12 GMT  
		Size: 3.1 MB (3144006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e0b94326a2037e898aaed8aeb1a35fa1a022a8c6cbd6c88f20fb14d54b9826`  
		Last Modified: Fri, 27 Sep 2024 06:28:12 GMT  
		Size: 17.3 KB (17294 bytes)  
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
$ docker pull swipl@sha256:26fbe60d1420ce3a157368ea4519141a8120995394eef8cd66f4cf324141a2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94807981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a53c47a17612bcadd0afea706ed5f40cd6db579e8e144f2850315f5fc1a75c`
-	Default Command: `["swipl"]`

```dockerfile
# Sun, 08 Sep 2024 08:35:01 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04be04db0f19489d1a2e0da09b7d8d2de707ee700e26000abcee5d02fd0df4bb`  
		Last Modified: Fri, 27 Sep 2024 23:46:59 GMT  
		Size: 47.7 MB (47713641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208f713269b79427ec7c2b96171913419e39fa1314e45dd7747ae7a20846680a`  
		Last Modified: Fri, 27 Sep 2024 23:53:22 GMT  
		Size: 17.9 MB (17937971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:379bbc4a063fc6b476def5d428bcb4f80dc40bd4790aada328062c78cc544677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ecb1f9d9a7e4e4af76806110d4e78136283d9ed27581366bf848e811ec8e04`

```dockerfile
```

-	Layers:
	-	`sha256:67112c63ba0d716c1fe17e7c1e6cc637caab52a902ebfd998e62a906d70c66f6`  
		Last Modified: Fri, 27 Sep 2024 23:53:22 GMT  
		Size: 3.1 MB (3144345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7123eaf64c9663b226ccf8d4660426477027bc95b086e49d93dcc9162ac41ee`  
		Last Modified: Fri, 27 Sep 2024 23:53:21 GMT  
		Size: 17.6 KB (17580 bytes)  
		MIME: application/vnd.in-toto+json
