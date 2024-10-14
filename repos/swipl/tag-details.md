<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:9.2.7`](#swipl927)
-	[`swipl:9.3.13`](#swipl9313)
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

## `swipl:9.3.13`

```console
$ docker pull swipl@sha256:c841bc3515e57181c7a299614d4c09234db61f22953401871cc819a171abb0d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.3.13` - linux; amd64

```console
$ docker pull swipl@sha256:ac1d212f76b54cccb897ec30141b8fb981f6e68a18222d5db9422b4b5d0edf04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97052215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f32e5910cd1b72335e8b9ec53257610d5bd5e982b2407f9902331a3b84a604`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Sat, 12 Oct 2024 13:28:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 12 Oct 2024 13:28:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
ENV LANG=C.UTF-8
# Sat, 12 Oct 2024 13:28:48 GMT
RUN set -eux;     SWIPL_VER=9.3.13;     SWIPL_CHECKSUM=4740456f7b22aab52d81bacb4c8a3370c717ba7996ad93d752b0c6474562a6ce;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a632f750cd76631f54805ca96a6033205d407234b6f1981a712ef0bfe9930d20`  
		Last Modified: Mon, 14 Oct 2024 17:10:59 GMT  
		Size: 49.2 MB (49220756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725d1c9ce1d9a896cd347d8df8b7395e4e240162fcd4830986c12847006ac05c`  
		Last Modified: Mon, 14 Oct 2024 17:10:58 GMT  
		Size: 18.7 MB (18705183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.13` - unknown; unknown

```console
$ docker pull swipl@sha256:dab5e0521a1ece58f414a1e3d5b5db8a7b36e80332b92903aa256d360feaf8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ff48b9479e19da108f96508ca0cdce0691b412399cef4911d8ecfba65ea8fd`

```dockerfile
```

-	Layers:
	-	`sha256:d6a1638925a022de6ff8641a8309d10ddf96e0f8f55b09af4339816ba45d83f2`  
		Last Modified: Mon, 14 Oct 2024 17:10:58 GMT  
		Size: 3.1 MB (3144010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75e78f2d70078cc106151d78b5a7c1b23c42cdf1054fbdd9def57958d915e00f`  
		Last Modified: Mon, 14 Oct 2024 17:10:57 GMT  
		Size: 17.3 KB (17319 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.13` - linux; arm variant v7

```console
$ docker pull swipl@sha256:51af010af292db98a8a21963c54bedbba09bc622bb71c6c3fd8f93e3552a7e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82764918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d0a9d96d2f3112596f33f7e819726d81d9043e13230874f7cfde6031b44fdc`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Sat, 12 Oct 2024 13:28:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 12 Oct 2024 13:28:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
ENV LANG=C.UTF-8
# Sat, 12 Oct 2024 13:28:48 GMT
RUN set -eux;     SWIPL_VER=9.3.13;     SWIPL_CHECKSUM=4740456f7b22aab52d81bacb4c8a3370c717ba7996ad93d752b0c6474562a6ce;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a557349cacd6f101406c33221613d9d89cfecc8fa1c17f5d69c9a51b7152675c`  
		Last Modified: Mon, 14 Oct 2024 17:00:08 GMT  
		Size: 43.7 MB (43723157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57920ee0cbca2789e275e57694f34a6ca64271ed4de2aa80fb7f00fa982d64b8`  
		Last Modified: Mon, 14 Oct 2024 17:00:07 GMT  
		Size: 14.3 MB (14323616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.13` - unknown; unknown

```console
$ docker pull swipl@sha256:54205cc1b55c3b16e7870126b88f63de2201c193507875c6c6ce5cf4930b61bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3163936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23724cd156857f08d7c4c656d5cf12c0cd01f7eac462cf3966841f1f539a5961`

```dockerfile
```

-	Layers:
	-	`sha256:8d78eee17e12b9bdc8335d19b7d73a78fc22d4ad6e92fbfd5ccd76c780a90ad2`  
		Last Modified: Mon, 14 Oct 2024 17:00:07 GMT  
		Size: 3.1 MB (3146532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a1972bad90cf6565c9e3f0cbfa86eb67c0eb2e7bc9138bb8e90e67d6e8e16a`  
		Last Modified: Mon, 14 Oct 2024 17:00:06 GMT  
		Size: 17.4 KB (17404 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.13` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:ae6375c5d6ea85284afeda2ee92b86b87acfbc9969bf579306a1bc26e8b35ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94965938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c786a219445926aa2bc7347c871a138ccb6a6d2905097436fdea204147d97dca`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Sat, 12 Oct 2024 13:28:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 12 Oct 2024 13:28:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
ENV LANG=C.UTF-8
# Sat, 12 Oct 2024 13:28:48 GMT
RUN set -eux;     SWIPL_VER=9.3.13;     SWIPL_CHECKSUM=4740456f7b22aab52d81bacb4c8a3370c717ba7996ad93d752b0c6474562a6ce;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9314a13b7d4f55c1f031a75478f01aabe9818582a4727e80b374d86cc64ec81a`  
		Last Modified: Mon, 14 Oct 2024 17:05:09 GMT  
		Size: 47.7 MB (47713028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77a25bad0c2fc2bb5f9d9f41bfbcd74fae2ef0bc9dc7286c4ad453d1ceb087`  
		Last Modified: Mon, 14 Oct 2024 17:05:08 GMT  
		Size: 18.1 MB (18096541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.13` - unknown; unknown

```console
$ docker pull swipl@sha256:8778b5e5bb93898f060456db9ca3342b7299f89d9ad6ba49056c638e9b9e7e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd13a81813a542eb74decf2c3accbd27966ec1fdd06403b48f58c49e8675a089`

```dockerfile
```

-	Layers:
	-	`sha256:aa7044781a836519fb5da3b90028bf64171c1073933fbc1e361612ab7bb9f806`  
		Last Modified: Mon, 14 Oct 2024 17:05:07 GMT  
		Size: 3.1 MB (3144349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18f826bf9426536ad7662e2714acfeafd68f434ac7d6e1fb776e4526c63a0f8`  
		Last Modified: Mon, 14 Oct 2024 17:05:07 GMT  
		Size: 17.4 KB (17426 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:latest`

```console
$ docker pull swipl@sha256:c841bc3515e57181c7a299614d4c09234db61f22953401871cc819a171abb0d4
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
$ docker pull swipl@sha256:ac1d212f76b54cccb897ec30141b8fb981f6e68a18222d5db9422b4b5d0edf04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97052215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f32e5910cd1b72335e8b9ec53257610d5bd5e982b2407f9902331a3b84a604`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Sat, 12 Oct 2024 13:28:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 12 Oct 2024 13:28:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
ENV LANG=C.UTF-8
# Sat, 12 Oct 2024 13:28:48 GMT
RUN set -eux;     SWIPL_VER=9.3.13;     SWIPL_CHECKSUM=4740456f7b22aab52d81bacb4c8a3370c717ba7996ad93d752b0c6474562a6ce;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a632f750cd76631f54805ca96a6033205d407234b6f1981a712ef0bfe9930d20`  
		Last Modified: Mon, 14 Oct 2024 17:10:59 GMT  
		Size: 49.2 MB (49220756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725d1c9ce1d9a896cd347d8df8b7395e4e240162fcd4830986c12847006ac05c`  
		Last Modified: Mon, 14 Oct 2024 17:10:58 GMT  
		Size: 18.7 MB (18705183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:dab5e0521a1ece58f414a1e3d5b5db8a7b36e80332b92903aa256d360feaf8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ff48b9479e19da108f96508ca0cdce0691b412399cef4911d8ecfba65ea8fd`

```dockerfile
```

-	Layers:
	-	`sha256:d6a1638925a022de6ff8641a8309d10ddf96e0f8f55b09af4339816ba45d83f2`  
		Last Modified: Mon, 14 Oct 2024 17:10:58 GMT  
		Size: 3.1 MB (3144010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75e78f2d70078cc106151d78b5a7c1b23c42cdf1054fbdd9def57958d915e00f`  
		Last Modified: Mon, 14 Oct 2024 17:10:57 GMT  
		Size: 17.3 KB (17319 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:51af010af292db98a8a21963c54bedbba09bc622bb71c6c3fd8f93e3552a7e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82764918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d0a9d96d2f3112596f33f7e819726d81d9043e13230874f7cfde6031b44fdc`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Sat, 12 Oct 2024 13:28:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 12 Oct 2024 13:28:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
ENV LANG=C.UTF-8
# Sat, 12 Oct 2024 13:28:48 GMT
RUN set -eux;     SWIPL_VER=9.3.13;     SWIPL_CHECKSUM=4740456f7b22aab52d81bacb4c8a3370c717ba7996ad93d752b0c6474562a6ce;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a557349cacd6f101406c33221613d9d89cfecc8fa1c17f5d69c9a51b7152675c`  
		Last Modified: Mon, 14 Oct 2024 17:00:08 GMT  
		Size: 43.7 MB (43723157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57920ee0cbca2789e275e57694f34a6ca64271ed4de2aa80fb7f00fa982d64b8`  
		Last Modified: Mon, 14 Oct 2024 17:00:07 GMT  
		Size: 14.3 MB (14323616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:54205cc1b55c3b16e7870126b88f63de2201c193507875c6c6ce5cf4930b61bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3163936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23724cd156857f08d7c4c656d5cf12c0cd01f7eac462cf3966841f1f539a5961`

```dockerfile
```

-	Layers:
	-	`sha256:8d78eee17e12b9bdc8335d19b7d73a78fc22d4ad6e92fbfd5ccd76c780a90ad2`  
		Last Modified: Mon, 14 Oct 2024 17:00:07 GMT  
		Size: 3.1 MB (3146532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a1972bad90cf6565c9e3f0cbfa86eb67c0eb2e7bc9138bb8e90e67d6e8e16a`  
		Last Modified: Mon, 14 Oct 2024 17:00:06 GMT  
		Size: 17.4 KB (17404 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:ae6375c5d6ea85284afeda2ee92b86b87acfbc9969bf579306a1bc26e8b35ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94965938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c786a219445926aa2bc7347c871a138ccb6a6d2905097436fdea204147d97dca`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Sat, 12 Oct 2024 13:28:48 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 12 Oct 2024 13:28:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
ENV LANG=C.UTF-8
# Sat, 12 Oct 2024 13:28:48 GMT
RUN set -eux;     SWIPL_VER=9.3.13;     SWIPL_CHECKSUM=4740456f7b22aab52d81bacb4c8a3370c717ba7996ad93d752b0c6474562a6ce;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git a63f1f5650e44c7d40401ed5a8b689aa1caca635;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Sat, 12 Oct 2024 13:28:48 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9314a13b7d4f55c1f031a75478f01aabe9818582a4727e80b374d86cc64ec81a`  
		Last Modified: Mon, 14 Oct 2024 17:05:09 GMT  
		Size: 47.7 MB (47713028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77a25bad0c2fc2bb5f9d9f41bfbcd74fae2ef0bc9dc7286c4ad453d1ceb087`  
		Last Modified: Mon, 14 Oct 2024 17:05:08 GMT  
		Size: 18.1 MB (18096541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:8778b5e5bb93898f060456db9ca3342b7299f89d9ad6ba49056c638e9b9e7e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd13a81813a542eb74decf2c3accbd27966ec1fdd06403b48f58c49e8675a089`

```dockerfile
```

-	Layers:
	-	`sha256:aa7044781a836519fb5da3b90028bf64171c1073933fbc1e361612ab7bb9f806`  
		Last Modified: Mon, 14 Oct 2024 17:05:07 GMT  
		Size: 3.1 MB (3144349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18f826bf9426536ad7662e2714acfeafd68f434ac7d6e1fb776e4526c63a0f8`  
		Last Modified: Mon, 14 Oct 2024 17:05:07 GMT  
		Size: 17.4 KB (17426 bytes)  
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
