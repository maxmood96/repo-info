<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:10.0.0`](#swipl1000)
-	[`swipl:10.1.1`](#swipl1011)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:10.0.0`

```console
$ docker pull swipl@sha256:2fbfa6ab197287b77579695919d9e5073658848d36bc001e3f9c172980140429
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:10.0.0` - linux; amd64

```console
$ docker pull swipl@sha256:3d41cca8a4bbd04866c232e5fa7354906da29b0e92c6579a585d32a6341fdf83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (99037661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a079936df346a05dcd3fd58b0aa15dc79671a3d8a769edb9b555501463a6448d`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:04:49 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 13 Jan 2026 02:04:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:04:49 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:10:28 GMT
RUN set -eux;     SWIPL_VER=10.0.0;     SWIPL_CHECKSUM=98c552c48fc8b44dcd4440abbfed632cceb75055fde267be12f340bea8106590;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 13 Jan 2026 02:10:28 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d4a500e7c159216d0255d51e65c7a3d7f7583da3cb59767dfa982b3c358d79`  
		Last Modified: Tue, 13 Jan 2026 02:10:55 GMT  
		Size: 49.2 MB (49233569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfeed3d1fc3fb2331b34ad59314b91bd51f7e37ad7a1d3758c68d3103baf654`  
		Last Modified: Tue, 13 Jan 2026 02:10:41 GMT  
		Size: 21.6 MB (21575520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:10.0.0` - unknown; unknown

```console
$ docker pull swipl@sha256:cfea77910bcc992aa3014c92e8b752a84ffe04744aaabee380bd8383672034c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee40c7de57ca1f64402b63ecf36f939827753136daafbe37247d18fe04d04b8`

```dockerfile
```

-	Layers:
	-	`sha256:141e0a8db4576b895e1a5e28d8ac8d7fd39ae84428979355f7de9705fe277da5`  
		Last Modified: Tue, 13 Jan 2026 06:18:20 GMT  
		Size: 3.3 MB (3326546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d9970bda97549f72faa431201a7544b0ffd0a6b88e90cf6f662789058bccca0`  
		Last Modified: Tue, 13 Jan 2026 02:10:40 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:10.0.0` - linux; arm variant v7

```console
$ docker pull swipl@sha256:b50b33a60fbb2246c58cdacc15913e173a2512d66b2410be2a6dd194aeb7bb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84793270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d352b9d5d63f650491673c42b49acb50a40b234d72f516c16714869fed3b16`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:53:30 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 13 Jan 2026 02:53:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:55:56 GMT
RUN set -eux;     SWIPL_VER=10.0.0;     SWIPL_CHECKSUM=98c552c48fc8b44dcd4440abbfed632cceb75055fde267be12f340bea8106590;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 13 Jan 2026 02:55:56 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:08 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fd3c1445a3e9539d2c77fe330609287fd474d11fd62a69056b87485e2bc17a`  
		Last Modified: Tue, 13 Jan 2026 02:56:19 GMT  
		Size: 43.8 MB (43774996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269a5bdeb284ec0a13ffd0f7894090a07b4d690226b8288ed07efb19af36cc5c`  
		Last Modified: Tue, 13 Jan 2026 02:56:17 GMT  
		Size: 17.1 MB (17084156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:10.0.0` - unknown; unknown

```console
$ docker pull swipl@sha256:429d729381b3b8bbedb24718a880be83a09ba1d5ef406ca1c4a39140438e0d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed61e1e414887c5c7853afacb02ec19e953e3f43fe4d842dd2f8a6dd678cb4`

```dockerfile
```

-	Layers:
	-	`sha256:1fa81d053276433201c679748f8057a4ccb862057a7796fecc8eea18eb8b3380`  
		Last Modified: Tue, 13 Jan 2026 06:18:26 GMT  
		Size: 3.3 MB (3325392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a82a4d912e5a579b0a018d2b17983ceb0dccbbdcfe1ceb3076f17a17c90ee32b`  
		Last Modified: Tue, 13 Jan 2026 02:56:07 GMT  
		Size: 17.9 KB (17926 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:10.0.0` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:6653a8505c776ec2d092a3101b36ad9c507074838a6073db7d43316816e8af84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96851349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0463163ede51e909e12a2777c82830dfdb690ea523e87f17791b0e890c12af3f`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:11:41 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 13 Jan 2026 02:11:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:41 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:17:32 GMT
RUN set -eux;     SWIPL_VER=10.0.0;     SWIPL_CHECKSUM=98c552c48fc8b44dcd4440abbfed632cceb75055fde267be12f340bea8106590;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 13 Jan 2026 02:17:32 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5d70c69b1863467d69bf22e31e861d5d5333f2985bc08f48ba33d4a281506`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 47.8 MB (47803694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79150db235ed75bd78dc5bec7b0aaaaecd7b14db434547b8f0b7055e50c86a3`  
		Last Modified: Tue, 13 Jan 2026 02:17:53 GMT  
		Size: 20.9 MB (20939766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:10.0.0` - unknown; unknown

```console
$ docker pull swipl@sha256:9dce5c0ed0dcfd4c20ccb6398f152d148e5543af5552b952ede7e0acccdff9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad24dd3ff8fe89c9aa132876d2a973e34fdd51af32969d4ea40512efded38a9`

```dockerfile
```

-	Layers:
	-	`sha256:4b9038f1c885dc81fbfb43879ba27a9a8d05261eab4ac790638d7581ec908ec6`  
		Last Modified: Tue, 13 Jan 2026 06:18:31 GMT  
		Size: 3.3 MB (3326886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:719679368b28b4e5f537a594dbe51bc2026f652df20c97c61005f1b20fa611a7`  
		Last Modified: Tue, 13 Jan 2026 02:17:44 GMT  
		Size: 17.9 KB (17943 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:10.1.1`

```console
$ docker pull swipl@sha256:b9714b6c636ed9074b3fc4f5a18c94bf1249fd5b2e293b019cdbd1a5b64cf256
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swipl:10.1.1` - linux; amd64

```console
$ docker pull swipl@sha256:835eab5ffcbb2c8c04f31a2b4510d46e96e6b96988059644b0e9c94db27ba31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (99039133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc8674acc4f553338897730cbc89046df3a0dadee295dc4c2d7552aaf1cf51a`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:04:40 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 13 Jan 2026 02:04:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:04:40 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:10:44 GMT
RUN set -eux;     SWIPL_VER=10.1.1;     SWIPL_CHECKSUM=4bbb31f684749bbe3af2e75d726e5453ea26a656d6b2b1299f5633d5f37af851;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 13 Jan 2026 02:10:44 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035f025c80ef6b065d4c762ec9c32fb45394d26d31739263be1463f375de2aca`  
		Last Modified: Tue, 13 Jan 2026 02:11:08 GMT  
		Size: 49.2 MB (49233670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aa30f116119298de99068a43307f4ee64819841e81bcbe39f9da1b8baa0f53`  
		Last Modified: Tue, 13 Jan 2026 02:11:06 GMT  
		Size: 21.6 MB (21576891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:10.1.1` - unknown; unknown

```console
$ docker pull swipl@sha256:4e3f51e045fd795e3f4f1c76cec26e5546e29c86969fd2d9efcbc383cf83df42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701e3339403bd2c26c6dffd94cd4a16fb8c5b5a7f9876a36a40528fe9e4f39b7`

```dockerfile
```

-	Layers:
	-	`sha256:9989fe650e2045b77c8637dddcfa970dcec83c07d08486ee074d67739c81bcf3`  
		Last Modified: Tue, 13 Jan 2026 02:10:56 GMT  
		Size: 3.3 MB (3326546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d26df3146dc7eef9b154a2a023ae7aafb38ab9b9a993b3efd41b49ef7f09c9c`  
		Last Modified: Tue, 13 Jan 2026 06:18:31 GMT  
		Size: 17.9 KB (17885 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:10.1.1` - linux; arm variant v7

```console
$ docker pull swipl@sha256:a674d14bf5f4969c3b2d79df37602485d836cd78f404c31fcaf9b85f6f323ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84795309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950a5468e3e2b49d8bc9f2748bb354ffa5ee86cf1dbd904e30b460b767cc49d6`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:51:27 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 13 Jan 2026 02:51:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:51:27 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:53:58 GMT
RUN set -eux;     SWIPL_VER=10.1.1;     SWIPL_CHECKSUM=4bbb31f684749bbe3af2e75d726e5453ea26a656d6b2b1299f5633d5f37af851;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 13 Jan 2026 02:53:58 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:08 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74b45259d6f11c48476fb7c80161ebbdee21dcc25a72a9f43fc7a1e6a66d55f`  
		Last Modified: Tue, 13 Jan 2026 02:54:19 GMT  
		Size: 43.8 MB (43775250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6693d992cc7628d34e0771daeb4f09bc59143cbda547e2fac67f40468711fa2`  
		Last Modified: Tue, 13 Jan 2026 02:54:20 GMT  
		Size: 17.1 MB (17085941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:10.1.1` - unknown; unknown

```console
$ docker pull swipl@sha256:c60cf691dff4e31e04894564163d9f8a47ad0261504bb38a786dc2469fc7ad53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77e99caaea83ae53c0842e12ba7cd5276791211fffdfeab3b8d5ad14af9ae3a`

```dockerfile
```

-	Layers:
	-	`sha256:ec668061734a199ad9dfc31fbf56c2a20aef744596cca200a099fddfac5d484a`  
		Last Modified: Tue, 13 Jan 2026 06:18:35 GMT  
		Size: 3.3 MB (3325392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba94d1330bc2b37bd5f95301bdbe27291fe6132ef8b40a2356906f6dc2d0c9c`  
		Last Modified: Tue, 13 Jan 2026 06:18:37 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:10.1.1` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:24223213858f66e338999c299487508ba8bea111fa2ac44a71486187348bef8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96856828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440f988bd313abdf78b90914596eae407e454fc0e3d4a7d5d0636b6d6e97045f`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:10:37 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 13 Jan 2026 02:10:37 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:10:37 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:16:26 GMT
RUN set -eux;     SWIPL_VER=10.1.1;     SWIPL_CHECKSUM=4bbb31f684749bbe3af2e75d726e5453ea26a656d6b2b1299f5633d5f37af851;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 13 Jan 2026 02:16:26 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b7297d877e71a5e3e9331d06ce82ff04ffcdf4eb71b42d3c785bb0c7001345`  
		Last Modified: Tue, 13 Jan 2026 02:16:51 GMT  
		Size: 47.8 MB (47803707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739d4e673cacc1e654b5eb8fa3e80400e182c61adfbae0f6f591e278e051777a`  
		Last Modified: Tue, 13 Jan 2026 02:16:47 GMT  
		Size: 20.9 MB (20945232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:10.1.1` - unknown; unknown

```console
$ docker pull swipl@sha256:1dd1b84cd17d25f67116ffb168e76322d6c017ac0f5b6ca583ed032abb73f300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da300b9cad508b320e597850f4a3c998a15e2cfe0c170b821d9a0da44a7489f3`

```dockerfile
```

-	Layers:
	-	`sha256:a49db3c0a54992686e91f27a9ee652f4e9fc396aac499d549d55e7b1ddac6bd3`  
		Last Modified: Tue, 13 Jan 2026 06:18:41 GMT  
		Size: 3.3 MB (3326886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef0af8543e761cad8d83f108791200cc378d4065bd70a54b2aa44e5687fb8e31`  
		Last Modified: Tue, 13 Jan 2026 06:18:42 GMT  
		Size: 18.0 KB (17980 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:latest`

```console
$ docker pull swipl@sha256:b9714b6c636ed9074b3fc4f5a18c94bf1249fd5b2e293b019cdbd1a5b64cf256
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
$ docker pull swipl@sha256:835eab5ffcbb2c8c04f31a2b4510d46e96e6b96988059644b0e9c94db27ba31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (99039133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc8674acc4f553338897730cbc89046df3a0dadee295dc4c2d7552aaf1cf51a`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:04:40 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 13 Jan 2026 02:04:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:04:40 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:10:44 GMT
RUN set -eux;     SWIPL_VER=10.1.1;     SWIPL_CHECKSUM=4bbb31f684749bbe3af2e75d726e5453ea26a656d6b2b1299f5633d5f37af851;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 13 Jan 2026 02:10:44 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035f025c80ef6b065d4c762ec9c32fb45394d26d31739263be1463f375de2aca`  
		Last Modified: Tue, 13 Jan 2026 02:11:08 GMT  
		Size: 49.2 MB (49233670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aa30f116119298de99068a43307f4ee64819841e81bcbe39f9da1b8baa0f53`  
		Last Modified: Tue, 13 Jan 2026 02:11:06 GMT  
		Size: 21.6 MB (21576891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:4e3f51e045fd795e3f4f1c76cec26e5546e29c86969fd2d9efcbc383cf83df42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701e3339403bd2c26c6dffd94cd4a16fb8c5b5a7f9876a36a40528fe9e4f39b7`

```dockerfile
```

-	Layers:
	-	`sha256:9989fe650e2045b77c8637dddcfa970dcec83c07d08486ee074d67739c81bcf3`  
		Last Modified: Tue, 13 Jan 2026 02:10:56 GMT  
		Size: 3.3 MB (3326546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d26df3146dc7eef9b154a2a023ae7aafb38ab9b9a993b3efd41b49ef7f09c9c`  
		Last Modified: Tue, 13 Jan 2026 06:18:31 GMT  
		Size: 17.9 KB (17885 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:a674d14bf5f4969c3b2d79df37602485d836cd78f404c31fcaf9b85f6f323ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84795309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950a5468e3e2b49d8bc9f2748bb354ffa5ee86cf1dbd904e30b460b767cc49d6`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:51:27 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 13 Jan 2026 02:51:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:51:27 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:53:58 GMT
RUN set -eux;     SWIPL_VER=10.1.1;     SWIPL_CHECKSUM=4bbb31f684749bbe3af2e75d726e5453ea26a656d6b2b1299f5633d5f37af851;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 13 Jan 2026 02:53:58 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:08 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74b45259d6f11c48476fb7c80161ebbdee21dcc25a72a9f43fc7a1e6a66d55f`  
		Last Modified: Tue, 13 Jan 2026 02:54:19 GMT  
		Size: 43.8 MB (43775250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6693d992cc7628d34e0771daeb4f09bc59143cbda547e2fac67f40468711fa2`  
		Last Modified: Tue, 13 Jan 2026 02:54:20 GMT  
		Size: 17.1 MB (17085941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:c60cf691dff4e31e04894564163d9f8a47ad0261504bb38a786dc2469fc7ad53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77e99caaea83ae53c0842e12ba7cd5276791211fffdfeab3b8d5ad14af9ae3a`

```dockerfile
```

-	Layers:
	-	`sha256:ec668061734a199ad9dfc31fbf56c2a20aef744596cca200a099fddfac5d484a`  
		Last Modified: Tue, 13 Jan 2026 06:18:35 GMT  
		Size: 3.3 MB (3325392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba94d1330bc2b37bd5f95301bdbe27291fe6132ef8b40a2356906f6dc2d0c9c`  
		Last Modified: Tue, 13 Jan 2026 06:18:37 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:24223213858f66e338999c299487508ba8bea111fa2ac44a71486187348bef8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96856828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440f988bd313abdf78b90914596eae407e454fc0e3d4a7d5d0636b6d6e97045f`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:10:37 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 13 Jan 2026 02:10:37 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:10:37 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:16:26 GMT
RUN set -eux;     SWIPL_VER=10.1.1;     SWIPL_CHECKSUM=4bbb31f684749bbe3af2e75d726e5453ea26a656d6b2b1299f5633d5f37af851;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 13 Jan 2026 02:16:26 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b7297d877e71a5e3e9331d06ce82ff04ffcdf4eb71b42d3c785bb0c7001345`  
		Last Modified: Tue, 13 Jan 2026 02:16:51 GMT  
		Size: 47.8 MB (47803707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739d4e673cacc1e654b5eb8fa3e80400e182c61adfbae0f6f591e278e051777a`  
		Last Modified: Tue, 13 Jan 2026 02:16:47 GMT  
		Size: 20.9 MB (20945232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:latest` - unknown; unknown

```console
$ docker pull swipl@sha256:1dd1b84cd17d25f67116ffb168e76322d6c017ac0f5b6ca583ed032abb73f300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da300b9cad508b320e597850f4a3c998a15e2cfe0c170b821d9a0da44a7489f3`

```dockerfile
```

-	Layers:
	-	`sha256:a49db3c0a54992686e91f27a9ee652f4e9fc396aac499d549d55e7b1ddac6bd3`  
		Last Modified: Tue, 13 Jan 2026 06:18:41 GMT  
		Size: 3.3 MB (3326886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef0af8543e761cad8d83f108791200cc378d4065bd70a54b2aa44e5687fb8e31`  
		Last Modified: Tue, 13 Jan 2026 06:18:42 GMT  
		Size: 18.0 KB (17980 bytes)  
		MIME: application/vnd.in-toto+json

## `swipl:stable`

```console
$ docker pull swipl@sha256:2fbfa6ab197287b77579695919d9e5073658848d36bc001e3f9c172980140429
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
$ docker pull swipl@sha256:3d41cca8a4bbd04866c232e5fa7354906da29b0e92c6579a585d32a6341fdf83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (99037661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a079936df346a05dcd3fd58b0aa15dc79671a3d8a769edb9b555501463a6448d`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:04:49 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 13 Jan 2026 02:04:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:04:49 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:10:28 GMT
RUN set -eux;     SWIPL_VER=10.0.0;     SWIPL_CHECKSUM=98c552c48fc8b44dcd4440abbfed632cceb75055fde267be12f340bea8106590;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 13 Jan 2026 02:10:28 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d4a500e7c159216d0255d51e65c7a3d7f7583da3cb59767dfa982b3c358d79`  
		Last Modified: Tue, 13 Jan 2026 02:10:55 GMT  
		Size: 49.2 MB (49233569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfeed3d1fc3fb2331b34ad59314b91bd51f7e37ad7a1d3758c68d3103baf654`  
		Last Modified: Tue, 13 Jan 2026 02:10:41 GMT  
		Size: 21.6 MB (21575520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:cfea77910bcc992aa3014c92e8b752a84ffe04744aaabee380bd8383672034c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee40c7de57ca1f64402b63ecf36f939827753136daafbe37247d18fe04d04b8`

```dockerfile
```

-	Layers:
	-	`sha256:141e0a8db4576b895e1a5e28d8ac8d7fd39ae84428979355f7de9705fe277da5`  
		Last Modified: Tue, 13 Jan 2026 06:18:20 GMT  
		Size: 3.3 MB (3326546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d9970bda97549f72faa431201a7544b0ffd0a6b88e90cf6f662789058bccca0`  
		Last Modified: Tue, 13 Jan 2026 02:10:40 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:b50b33a60fbb2246c58cdacc15913e173a2512d66b2410be2a6dd194aeb7bb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84793270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d352b9d5d63f650491673c42b49acb50a40b234d72f516c16714869fed3b16`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:53:30 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 13 Jan 2026 02:53:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:55:56 GMT
RUN set -eux;     SWIPL_VER=10.0.0;     SWIPL_CHECKSUM=98c552c48fc8b44dcd4440abbfed632cceb75055fde267be12f340bea8106590;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 13 Jan 2026 02:55:56 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:08 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fd3c1445a3e9539d2c77fe330609287fd474d11fd62a69056b87485e2bc17a`  
		Last Modified: Tue, 13 Jan 2026 02:56:19 GMT  
		Size: 43.8 MB (43774996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269a5bdeb284ec0a13ffd0f7894090a07b4d690226b8288ed07efb19af36cc5c`  
		Last Modified: Tue, 13 Jan 2026 02:56:17 GMT  
		Size: 17.1 MB (17084156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:429d729381b3b8bbedb24718a880be83a09ba1d5ef406ca1c4a39140438e0d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed61e1e414887c5c7853afacb02ec19e953e3f43fe4d842dd2f8a6dd678cb4`

```dockerfile
```

-	Layers:
	-	`sha256:1fa81d053276433201c679748f8057a4ccb862057a7796fecc8eea18eb8b3380`  
		Last Modified: Tue, 13 Jan 2026 06:18:26 GMT  
		Size: 3.3 MB (3325392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a82a4d912e5a579b0a018d2b17983ceb0dccbbdcfe1ceb3076f17a17c90ee32b`  
		Last Modified: Tue, 13 Jan 2026 02:56:07 GMT  
		Size: 17.9 KB (17926 bytes)  
		MIME: application/vnd.in-toto+json

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:6653a8505c776ec2d092a3101b36ad9c507074838a6073db7d43316816e8af84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96851349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0463163ede51e909e12a2777c82830dfdb690ea523e87f17791b0e890c12af3f`
-	Default Command: `["swipl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:11:41 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 13 Jan 2026 02:11:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-0-2     libgmp10     libossp-uuid16     libssl3     ca-certificates     libdb5.3     libpcre2-8-0     libedit2     libgeos3.11.1     libspatialindex6     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient-dev-compat     libsqlite3-0     libserd-0-0     python3     libpython3.11     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:41 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:17:32 GMT
RUN set -eux;     SWIPL_VER=10.0.0;     SWIPL_CHECKSUM=98c552c48fc8b44dcd4440abbfed632cceb75055fde267be12f340bea8106590;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git pkg-config m4 libtool automake autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre2-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libyaml-dev libgoogle-perftools-dev libpython3-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=PGO           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     echo ":- multifile prolog:build_environment/2." > env.pl;     echo "prolog:build_environment('PORTABLE', '1')." >> env.pl;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt env.pl;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 95aba2a5c156b831cf2bcfd387f65a9b470280e4;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 2b232e7fd445a380e1731b5a5a38c6e6dfe5ad7d;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin hdt https://github.com/JanWielemaker/hdt.git 7f2221747ea751a20ad0d7b95aebfd2c99649c1f;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git bdf8962264d65dd8ef6eedf5f00ff0c0f6c52c2f;     apt-get purge -y --auto-remove $BUILD_DEPS # buildkit
# Tue, 13 Jan 2026 02:17:32 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5d70c69b1863467d69bf22e31e861d5d5333f2985bc08f48ba33d4a281506`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 47.8 MB (47803694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79150db235ed75bd78dc5bec7b0aaaaecd7b14db434547b8f0b7055e50c86a3`  
		Last Modified: Tue, 13 Jan 2026 02:17:53 GMT  
		Size: 20.9 MB (20939766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swipl:stable` - unknown; unknown

```console
$ docker pull swipl@sha256:9dce5c0ed0dcfd4c20ccb6398f152d148e5543af5552b952ede7e0acccdff9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad24dd3ff8fe89c9aa132876d2a973e34fdd51af32969d4ea40512efded38a9`

```dockerfile
```

-	Layers:
	-	`sha256:4b9038f1c885dc81fbfb43879ba27a9a8d05261eab4ac790638d7581ec908ec6`  
		Last Modified: Tue, 13 Jan 2026 06:18:31 GMT  
		Size: 3.3 MB (3326886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:719679368b28b4e5f537a594dbe51bc2026f652df20c97c61005f1b20fa611a7`  
		Last Modified: Tue, 13 Jan 2026 02:17:44 GMT  
		Size: 17.9 KB (17943 bytes)  
		MIME: application/vnd.in-toto+json
