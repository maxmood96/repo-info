<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:9.2.2`](#swipl922)
-	[`swipl:9.3.2`](#swipl932)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:9.2.2`

```console
$ docker pull swipl@sha256:0e4a42478c23f10bb80c1c258162b95ab41a32ae6d30822c759c0d26cf5d7f76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.2.2` - linux; amd64

```console
$ docker pull swipl@sha256:368f940fe90ffab84bb1c8f2803054504ab5506709969f7d30434865a1d35648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96471872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b288f3ce883cc15a8ef73963cfbf86ea27f564468b440cb9a1be1b36e2ddbeb4`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1814e9a2e520c359c4ee964ad3874ce3e411d79071d85aeb558f6dc47d3ac47`  
		Last Modified: Thu, 29 Feb 2024 20:00:54 GMT  
		Size: 49.2 MB (49202835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eeb27bc9361029f7b78aae9f2f73ca67ffdd7e8eb6aa75bf58b8b5de1a73b89`  
		Last Modified: Thu, 29 Feb 2024 20:00:53 GMT  
		Size: 18.1 MB (18144946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.2` - unknown; unknown

```console
$ docker pull swipl@sha256:f862ef30bf6f98e066ad34bc1ab0b94c705e904ad26b299d22c81a827d2a3c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136edd601d6534ac356a296c00f031f9f1c9eec416387f0a057bfa6b1141e0a0`

```dockerfile
```

-	Layers:
	-	`sha256:b125062c1072b124538ffdfca2e3fe96c1b89e7ac8ef49a5449df00479ccbf2b`  
		Last Modified: Thu, 29 Feb 2024 20:00:53 GMT  
		Size: 3.1 MB (3112670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cecb88851293d201611552e8247ada216f89a64ed79230b21a8c920cbc9ad2c9`  
		Last Modified: Thu, 29 Feb 2024 20:00:52 GMT  
		Size: 17.3 KB (17265 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.2.2` - linux; arm variant v7

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

### `swipl:9.2.2` - unknown; unknown

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

### `swipl:9.2.2` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:addd325ff230958115f5769f8017229190d70520fc8fd25a19516ec3779167d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94432536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daba9b7fd691f8da4c78db9fdc19dc3a3a011bac2e247c1cd009776265d815d`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
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
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd47474c3366ea4fb7156808ecf87fb0ea66e8adaa8ddf5847ad3fe85371928`  
		Last Modified: Wed, 14 Feb 2024 09:40:43 GMT  
		Size: 47.7 MB (47677037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c62ffc61be3d60fa8d6adeb500b01808a7b24934c511902c5f584a49c3955fb`  
		Last Modified: Thu, 29 Feb 2024 20:12:18 GMT  
		Size: 17.6 MB (17599136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.2.2` - unknown; unknown

```console
$ docker pull swipl@sha256:8807a32bf36ea0fa8823b1aed9770d5441168d509a58a162f902940cc3b2a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3130089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a40a1b9854c3a05d9dc1c58f7c9f5fcaf91dff4e2ed7924e3e2e49aa4961f6d`

```dockerfile
```

-	Layers:
	-	`sha256:871777bd718f4d6df5b0d05c8ebdbf04ae467a2540055436397dcc0341c30dda`  
		Last Modified: Thu, 29 Feb 2024 20:12:18 GMT  
		Size: 3.1 MB (3112983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a65b15534d8bc9def17e54b42c3c6e18f910cf679b0c3f83d2b56fa948ee6f`  
		Last Modified: Thu, 29 Feb 2024 20:12:18 GMT  
		Size: 17.1 KB (17106 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:9.3.2`

```console
$ docker pull swipl@sha256:2bedea00d8e4317ecc13455a753654dabc3d58bb97ffba32d383bf6b9538b187
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:9.3.2` - linux; amd64

```console
$ docker pull swipl@sha256:c5267f6d224fbbf1aa9f8b6a6ff393a102e7cb5e7a0b56d6a08fa05064d69324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96466421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3056b9c2921be9cef4ac7f03ca532b99988476bf88da76975a19b3050667d62`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Thu, 29 Feb 2024 11:46:50 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 29 Feb 2024 11:46:50 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 11:46:50 GMT
RUN set -eux;     SWIPL_VER=9.3.2;     SWIPL_CHECKSUM=c329123b4f63aa8d1566f4097af58412588d4e7ad16a5fd743f97b4be6733410;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164989dd25518418e8c875d036361dc383d0372bb72eabf05388bdb9ba1c8a34`  
		Last Modified: Thu, 29 Feb 2024 20:00:56 GMT  
		Size: 49.2 MB (49202789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10260a607d5f5c2a9db0a7521e95dccad816ffdaee02f979208dfe48794ba1e2`  
		Last Modified: Thu, 29 Feb 2024 20:00:56 GMT  
		Size: 18.1 MB (18139541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.2` - unknown; unknown

```console
$ docker pull swipl@sha256:a09aff507773e46443b1bebdfe545f5c8a5a9b6462b5112dddbe72375c6bc319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e2f11fb6f23c2dc35ba811720eb37e885b0c8c31fd028d51acad94875dad03`

```dockerfile
```

-	Layers:
	-	`sha256:81235a801b533320ad401685c8f9f6cd33c1f516b70a4d516095f54512ceff00`  
		Last Modified: Thu, 29 Feb 2024 20:00:55 GMT  
		Size: 3.1 MB (3112670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51d79d4748c88118e0c17b2700befed5025750750359bdf3aac1a52b44ab01bb`  
		Last Modified: Thu, 29 Feb 2024 20:00:55 GMT  
		Size: 17.3 KB (17266 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.2` - linux; arm variant v7

```console
$ docker pull swipl@sha256:67b367eeeed0f43201e9fa305bcaeb27a4b10f84a50eb7b178b2c2827edafd41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82838723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ce8b18045a9f085837bc9d3fdde413ee828df2f9ed78eff0ae1a172b750b49`
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
RUN set -eux;     SWIPL_VER=9.3.2;     SWIPL_CHECKSUM=c329123b4f63aa8d1566f4097af58412588d4e7ad16a5fd743f97b4be6733410;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
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
	-	`sha256:04d1aae3dbf83801665fca0230905200f2c85aaf6c5280069f3b93846b3fb051`  
		Last Modified: Thu, 29 Feb 2024 19:58:56 GMT  
		Size: 14.4 MB (14424477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.2` - unknown; unknown

```console
$ docker pull swipl@sha256:d82c2c0523b2446af67c8d283b777b79bfc78214beadf54aafaf873a3d60cb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1cecdd2e3931ea983be4bae4fae413dadffa882778f2c49f1f927ef87e3323`

```dockerfile
```

-	Layers:
	-	`sha256:f3004a893703c5b6a48768aa06a005026284e87e60b28c7ae57f290e1b2deffd`  
		Last Modified: Thu, 29 Feb 2024 19:58:56 GMT  
		Size: 3.1 MB (3115192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a23c94b3cedef128496fc599a96fc725f9a2e0daf85cb0262e18c51f5961940`  
		Last Modified: Thu, 29 Feb 2024 19:58:55 GMT  
		Size: 17.2 KB (17166 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:9.3.2` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:a56b2e7476abfd4f6c582da974e8499c0a1a94a1573220e9595316bee6c843ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94433318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456854e9afa23abce268e7e9d6d0f1fef03395e0bef90426f0af2ab897046e76`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Thu, 29 Feb 2024 11:46:50 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 29 Feb 2024 11:46:50 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 11:46:50 GMT
RUN set -eux;     SWIPL_VER=9.3.2;     SWIPL_CHECKSUM=c329123b4f63aa8d1566f4097af58412588d4e7ad16a5fd743f97b4be6733410;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd47474c3366ea4fb7156808ecf87fb0ea66e8adaa8ddf5847ad3fe85371928`  
		Last Modified: Wed, 14 Feb 2024 09:40:43 GMT  
		Size: 47.7 MB (47677037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591a00594d52234555d3cda2155a82ad48a91f1201d484f38c427b93d024d440`  
		Last Modified: Thu, 29 Feb 2024 20:06:22 GMT  
		Size: 17.6 MB (17599918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:9.3.2` - unknown; unknown

```console
$ docker pull swipl@sha256:4e2d8229ddb50012f9eb6e07dc70285490cd53688e965e344f8e2f45d0f823a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3130088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393bcbb839b9edbf6b75d2631bdc849d21883a6e6b25472335fb52f1c3791a33`

```dockerfile
```

-	Layers:
	-	`sha256:c90e8297c0361650bd35416f930195e25ffba71c66a1081f028b8f9840699079`  
		Last Modified: Thu, 29 Feb 2024 20:06:22 GMT  
		Size: 3.1 MB (3112983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:036c3d74be0e1328ee8efec32ee0c639f56c8881ac73dc1f08e15177108c1ad3`  
		Last Modified: Thu, 29 Feb 2024 20:06:21 GMT  
		Size: 17.1 KB (17105 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:latest`

```console
$ docker pull swipl@sha256:2bedea00d8e4317ecc13455a753654dabc3d58bb97ffba32d383bf6b9538b187
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
$ docker pull swipl@sha256:c5267f6d224fbbf1aa9f8b6a6ff393a102e7cb5e7a0b56d6a08fa05064d69324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96466421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3056b9c2921be9cef4ac7f03ca532b99988476bf88da76975a19b3050667d62`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Thu, 29 Feb 2024 11:46:50 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 29 Feb 2024 11:46:50 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 11:46:50 GMT
RUN set -eux;     SWIPL_VER=9.3.2;     SWIPL_CHECKSUM=c329123b4f63aa8d1566f4097af58412588d4e7ad16a5fd743f97b4be6733410;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164989dd25518418e8c875d036361dc383d0372bb72eabf05388bdb9ba1c8a34`  
		Last Modified: Thu, 29 Feb 2024 20:00:56 GMT  
		Size: 49.2 MB (49202789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10260a607d5f5c2a9db0a7521e95dccad816ffdaee02f979208dfe48794ba1e2`  
		Last Modified: Thu, 29 Feb 2024 20:00:56 GMT  
		Size: 18.1 MB (18139541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:a09aff507773e46443b1bebdfe545f5c8a5a9b6462b5112dddbe72375c6bc319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e2f11fb6f23c2dc35ba811720eb37e885b0c8c31fd028d51acad94875dad03`

```dockerfile
```

-	Layers:
	-	`sha256:81235a801b533320ad401685c8f9f6cd33c1f516b70a4d516095f54512ceff00`  
		Last Modified: Thu, 29 Feb 2024 20:00:55 GMT  
		Size: 3.1 MB (3112670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51d79d4748c88118e0c17b2700befed5025750750359bdf3aac1a52b44ab01bb`  
		Last Modified: Thu, 29 Feb 2024 20:00:55 GMT  
		Size: 17.3 KB (17266 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:67b367eeeed0f43201e9fa305bcaeb27a4b10f84a50eb7b178b2c2827edafd41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82838723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ce8b18045a9f085837bc9d3fdde413ee828df2f9ed78eff0ae1a172b750b49`
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
RUN set -eux;     SWIPL_VER=9.3.2;     SWIPL_CHECKSUM=c329123b4f63aa8d1566f4097af58412588d4e7ad16a5fd743f97b4be6733410;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
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
	-	`sha256:04d1aae3dbf83801665fca0230905200f2c85aaf6c5280069f3b93846b3fb051`  
		Last Modified: Thu, 29 Feb 2024 19:58:56 GMT  
		Size: 14.4 MB (14424477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:d82c2c0523b2446af67c8d283b777b79bfc78214beadf54aafaf873a3d60cb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1cecdd2e3931ea983be4bae4fae413dadffa882778f2c49f1f927ef87e3323`

```dockerfile
```

-	Layers:
	-	`sha256:f3004a893703c5b6a48768aa06a005026284e87e60b28c7ae57f290e1b2deffd`  
		Last Modified: Thu, 29 Feb 2024 19:58:56 GMT  
		Size: 3.1 MB (3115192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a23c94b3cedef128496fc599a96fc725f9a2e0daf85cb0262e18c51f5961940`  
		Last Modified: Thu, 29 Feb 2024 19:58:55 GMT  
		Size: 17.2 KB (17166 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:a56b2e7476abfd4f6c582da974e8499c0a1a94a1573220e9595316bee6c843ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94433318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456854e9afa23abce268e7e9d6d0f1fef03395e0bef90426f0af2ab897046e76`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Thu, 29 Feb 2024 11:46:50 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 29 Feb 2024 11:46:50 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 11:46:50 GMT
RUN set -eux;     SWIPL_VER=9.3.2;     SWIPL_CHECKSUM=c329123b4f63aa8d1566f4097af58412588d4e7ad16a5fd743f97b4be6733410;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 3cf540598adc646eafd4d439f5446236a8587677;     install_addin hdt https://github.com/JanWielemaker/hdt.git 2923cb69f4a558cdc1866b033e1d69dab20aedd9;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git e35854942009ad2d06d6e21854c96e49c28d8b1e;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Thu, 29 Feb 2024 11:46:50 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd47474c3366ea4fb7156808ecf87fb0ea66e8adaa8ddf5847ad3fe85371928`  
		Last Modified: Wed, 14 Feb 2024 09:40:43 GMT  
		Size: 47.7 MB (47677037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591a00594d52234555d3cda2155a82ad48a91f1201d484f38c427b93d024d440`  
		Last Modified: Thu, 29 Feb 2024 20:06:22 GMT  
		Size: 17.6 MB (17599918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:4e2d8229ddb50012f9eb6e07dc70285490cd53688e965e344f8e2f45d0f823a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3130088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393bcbb839b9edbf6b75d2631bdc849d21883a6e6b25472335fb52f1c3791a33`

```dockerfile
```

-	Layers:
	-	`sha256:c90e8297c0361650bd35416f930195e25ffba71c66a1081f028b8f9840699079`  
		Last Modified: Thu, 29 Feb 2024 20:06:22 GMT  
		Size: 3.1 MB (3112983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:036c3d74be0e1328ee8efec32ee0c639f56c8881ac73dc1f08e15177108c1ad3`  
		Last Modified: Thu, 29 Feb 2024 20:06:21 GMT  
		Size: 17.1 KB (17105 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:stable`

```console
$ docker pull swipl@sha256:0e4a42478c23f10bb80c1c258162b95ab41a32ae6d30822c759c0d26cf5d7f76
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
$ docker pull swipl@sha256:368f940fe90ffab84bb1c8f2803054504ab5506709969f7d30434865a1d35648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96471872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b288f3ce883cc15a8ef73963cfbf86ea27f564468b440cb9a1be1b36e2ddbeb4`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1814e9a2e520c359c4ee964ad3874ce3e411d79071d85aeb558f6dc47d3ac47`  
		Last Modified: Thu, 29 Feb 2024 20:00:54 GMT  
		Size: 49.2 MB (49202835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eeb27bc9361029f7b78aae9f2f73ca67ffdd7e8eb6aa75bf58b8b5de1a73b89`  
		Last Modified: Thu, 29 Feb 2024 20:00:53 GMT  
		Size: 18.1 MB (18144946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:f862ef30bf6f98e066ad34bc1ab0b94c705e904ad26b299d22c81a827d2a3c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136edd601d6534ac356a296c00f031f9f1c9eec416387f0a057bfa6b1141e0a0`

```dockerfile
```

-	Layers:
	-	`sha256:b125062c1072b124538ffdfca2e3fe96c1b89e7ac8ef49a5449df00479ccbf2b`  
		Last Modified: Thu, 29 Feb 2024 20:00:53 GMT  
		Size: 3.1 MB (3112670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cecb88851293d201611552e8247ada216f89a64ed79230b21a8c920cbc9ad2c9`  
		Last Modified: Thu, 29 Feb 2024 20:00:52 GMT  
		Size: 17.3 KB (17265 bytes)  
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
$ docker pull swipl@sha256:addd325ff230958115f5769f8017229190d70520fc8fd25a19516ec3779167d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94432536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daba9b7fd691f8da4c78db9fdc19dc3a3a011bac2e247c1cd009776265d815d`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
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
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd47474c3366ea4fb7156808ecf87fb0ea66e8adaa8ddf5847ad3fe85371928`  
		Last Modified: Wed, 14 Feb 2024 09:40:43 GMT  
		Size: 47.7 MB (47677037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c62ffc61be3d60fa8d6adeb500b01808a7b24934c511902c5f584a49c3955fb`  
		Last Modified: Thu, 29 Feb 2024 20:12:18 GMT  
		Size: 17.6 MB (17599136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:8807a32bf36ea0fa8823b1aed9770d5441168d509a58a162f902940cc3b2a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3130089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a40a1b9854c3a05d9dc1c58f7c9f5fcaf91dff4e2ed7924e3e2e49aa4961f6d`

```dockerfile
```

-	Layers:
	-	`sha256:871777bd718f4d6df5b0d05c8ebdbf04ae467a2540055436397dcc0341c30dda`  
		Last Modified: Thu, 29 Feb 2024 20:12:18 GMT  
		Size: 3.1 MB (3112983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a65b15534d8bc9def17e54b42c3c6e18f910cf679b0c3f83d2b56fa948ee6f`  
		Last Modified: Thu, 29 Feb 2024 20:12:18 GMT  
		Size: 17.1 KB (17106 bytes)  
		MIME: application/vnd.in-toto+json
