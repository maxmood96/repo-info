<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.13`](#varnish6013)
-	[`varnish:7`](#varnish7)
-	[`varnish:7-alpine`](#varnish7-alpine)
-	[`varnish:7.5`](#varnish75)
-	[`varnish:7.5-alpine`](#varnish75-alpine)
-	[`varnish:7.5.0`](#varnish750)
-	[`varnish:7.5.0-alpine`](#varnish750-alpine)
-	[`varnish:7.6`](#varnish76)
-	[`varnish:7.6-alpine`](#varnish76-alpine)
-	[`varnish:7.6.1`](#varnish761)
-	[`varnish:7.6.1-alpine`](#varnish761-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:7a9d331853d515b045394b58509a39a3a9f739b88b42dfcd4082afd01c842d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:fda835e89501b3bfcdf7d465340c8b204ca9776ab551e811470e7312b2e99557
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137061519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60db612975912a663a1afc429ed8408e13ceffd856b92f86a133a0c24874b885`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 19:26:03 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 11 Nov 2024 19:26:04 GMT
ARG VARNISH_VERSION=6.0.13
# Mon, 11 Nov 2024 19:26:04 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Mon, 11 Nov 2024 19:26:04 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:27:56 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 11 Nov 2024 19:27:57 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:27:57 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:27:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:27:57 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:27:57 GMT
CMD []
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05966a0c665906794ab09e261101843fb5c1946a37a8c9f94db87bf549d07cf2`  
		Last Modified: Mon, 11 Nov 2024 19:29:30 GMT  
		Size: 107.9 MB (107934514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d590f21368f44a2a0ebd18308949d102dbf743e768c96f3400819bd6684c5da`  
		Last Modified: Mon, 11 Nov 2024 19:29:15 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d7abf2045f401927745a85aaa8a94e711e6885d638e084c8e478570db113a5e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105572118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c035b821cc4a214def698275b58aa9b2581c5ab2146ebb88848edd384d87d162`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 19:06:17 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 11 Nov 2024 19:06:17 GMT
ARG VARNISH_VERSION=6.0.13
# Mon, 11 Nov 2024 19:06:17 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Mon, 11 Nov 2024 19:06:17 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:08:06 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 11 Nov 2024 19:08:08 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:08:08 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:08:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:08:08 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:08:08 GMT
CMD []
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99b753c14f33f1802a71bfa07320696185ee0f185274e88a4b71caf01b5094d`  
		Last Modified: Mon, 11 Nov 2024 19:09:19 GMT  
		Size: 80.9 MB (80853201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c20ff8699d72c6c6aebbfcf4010484d1465c6bad8ffd6f2db47eca38558d769`  
		Last Modified: Mon, 11 Nov 2024 19:09:07 GMT  
		Size: 720.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:6f1af1221e7ee8a04b3fb0e3991ffe092f96a596d3290e2b4865d429438af794
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89962518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2457629dfbc9692b85ed2c1e01b356229137c975953652f73605e95c6379373f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 05:03:26 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Thu, 17 Oct 2024 05:03:26 GMT
ARG VARNISH_VERSION=6.0.13
# Thu, 17 Oct 2024 05:03:26 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Thu, 17 Oct 2024 05:03:26 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 05:04:54 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 17 Oct 2024 05:04:54 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 05:04:54 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:04:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 05:04:54 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 05:04:54 GMT
CMD []
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ffa19fe0da90c936e292635fee1beda4f024fd427bea366b745c939d0372c0`  
		Last Modified: Thu, 17 Oct 2024 05:06:02 GMT  
		Size: 59.9 MB (59886046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b614fa5710849988446d38aa6d216330b1fe9c0e81c4f0de9da7d8437ce5d1bf`  
		Last Modified: Thu, 17 Oct 2024 05:05:56 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:2e7f7fbcb5e9f5828cc258fafdd263a7a03036101c463771858a2c401dec0d1c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97133295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e95963497935e8a245ce7ef275e65611eefa1822de42ef90a163c2ed9501596`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:39:19 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Thu, 17 Oct 2024 00:39:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:30:12 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Thu, 17 Oct 2024 06:30:13 GMT
ARG VARNISH_VERSION=6.0.13
# Thu, 17 Oct 2024 06:30:13 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Thu, 17 Oct 2024 06:30:13 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 06:32:20 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 17 Oct 2024 06:32:20 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 06:32:20 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:32:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 06:32:21 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 06:32:21 GMT
CMD []
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1692d1a37679dcc33d7c210823d4a8285f5a731f674b2d905c226bbfd229f9b2`  
		Last Modified: Thu, 17 Oct 2024 06:33:58 GMT  
		Size: 64.7 MB (64718749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8326c5577321e2d7c296f00eb279fc6ec2262d56a0174bac8cf7937dd396ea1b`  
		Last Modified: Thu, 17 Oct 2024 06:33:46 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:2c8f1d0368a69bc5c2ee47b9d94f0bdcf9d118fbbde53f423561900c4dc3858b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141302279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5736a990cf4e26bd0a1bc3fe3ec7b0802ec358817f77ec0c2e156ead2389fc76`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 19:23:58 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 11 Nov 2024 19:23:58 GMT
ARG VARNISH_VERSION=6.0.13
# Mon, 11 Nov 2024 19:23:58 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Mon, 11 Nov 2024 19:23:58 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:26:46 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 11 Nov 2024 19:26:50 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:26:50 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:26:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:26:51 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:26:51 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024faa4175d8beb860272554bc0e100344a0c97b054fc77c1c40a922d76c59`  
		Last Modified: Mon, 11 Nov 2024 19:28:34 GMT  
		Size: 108.2 MB (108179358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10630b3b7197b4a3a286d5733c694832216644d75fa86c19b976da37325476ce`  
		Last Modified: Mon, 11 Nov 2024 19:28:17 GMT  
		Size: 720.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:32841bc0f7503dfd6c456ad94c8f78007b3100045965cadbe18f456099ac8abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76258728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded5fdd03ff15a069138878b85906a9196b3fc3ba8c26fafc22d244e44a35304`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 04 Sep 2024 21:43:26 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Wed, 04 Sep 2024 21:43:27 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:09:00 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Thu, 05 Sep 2024 00:09:00 GMT
ARG VARNISH_VERSION=6.0.13
# Thu, 05 Sep 2024 00:09:01 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Thu, 05 Sep 2024 00:09:01 GMT
ENV VARNISH_SIZE=100M
# Thu, 05 Sep 2024 00:10:22 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 05 Sep 2024 00:10:23 GMT
WORKDIR /etc/varnish
# Thu, 05 Sep 2024 00:10:23 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Thu, 05 Sep 2024 00:10:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 05 Sep 2024 00:10:23 GMT
EXPOSE 80 8443
# Thu, 05 Sep 2024 00:10:23 GMT
CMD []
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea184e408ee8a3bda0cdce477eb9806a10f7582bd36e0d18c1a36e645d4a8524`  
		Last Modified: Thu, 05 Sep 2024 00:17:59 GMT  
		Size: 46.6 MB (46594565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce81c8f7a8af9c632886d9382a8489c48b529c3a16f50cd485b6cd0cc3a2a19`  
		Last Modified: Thu, 05 Sep 2024 00:17:53 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.13`

```console
$ docker pull varnish@sha256:7a9d331853d515b045394b58509a39a3a9f739b88b42dfcd4082afd01c842d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.0.13` - linux; amd64

```console
$ docker pull varnish@sha256:fda835e89501b3bfcdf7d465340c8b204ca9776ab551e811470e7312b2e99557
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137061519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60db612975912a663a1afc429ed8408e13ceffd856b92f86a133a0c24874b885`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 19:26:03 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 11 Nov 2024 19:26:04 GMT
ARG VARNISH_VERSION=6.0.13
# Mon, 11 Nov 2024 19:26:04 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Mon, 11 Nov 2024 19:26:04 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:27:56 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 11 Nov 2024 19:27:57 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:27:57 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:27:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:27:57 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:27:57 GMT
CMD []
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05966a0c665906794ab09e261101843fb5c1946a37a8c9f94db87bf549d07cf2`  
		Last Modified: Mon, 11 Nov 2024 19:29:30 GMT  
		Size: 107.9 MB (107934514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d590f21368f44a2a0ebd18308949d102dbf743e768c96f3400819bd6684c5da`  
		Last Modified: Mon, 11 Nov 2024 19:29:15 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d7abf2045f401927745a85aaa8a94e711e6885d638e084c8e478570db113a5e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105572118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c035b821cc4a214def698275b58aa9b2581c5ab2146ebb88848edd384d87d162`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 19:06:17 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 11 Nov 2024 19:06:17 GMT
ARG VARNISH_VERSION=6.0.13
# Mon, 11 Nov 2024 19:06:17 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Mon, 11 Nov 2024 19:06:17 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:08:06 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 11 Nov 2024 19:08:08 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:08:08 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:08:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:08:08 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:08:08 GMT
CMD []
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99b753c14f33f1802a71bfa07320696185ee0f185274e88a4b71caf01b5094d`  
		Last Modified: Mon, 11 Nov 2024 19:09:19 GMT  
		Size: 80.9 MB (80853201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c20ff8699d72c6c6aebbfcf4010484d1465c6bad8ffd6f2db47eca38558d769`  
		Last Modified: Mon, 11 Nov 2024 19:09:07 GMT  
		Size: 720.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:6f1af1221e7ee8a04b3fb0e3991ffe092f96a596d3290e2b4865d429438af794
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89962518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2457629dfbc9692b85ed2c1e01b356229137c975953652f73605e95c6379373f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 05:03:26 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Thu, 17 Oct 2024 05:03:26 GMT
ARG VARNISH_VERSION=6.0.13
# Thu, 17 Oct 2024 05:03:26 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Thu, 17 Oct 2024 05:03:26 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 05:04:54 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 17 Oct 2024 05:04:54 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 05:04:54 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:04:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 05:04:54 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 05:04:54 GMT
CMD []
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ffa19fe0da90c936e292635fee1beda4f024fd427bea366b745c939d0372c0`  
		Last Modified: Thu, 17 Oct 2024 05:06:02 GMT  
		Size: 59.9 MB (59886046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b614fa5710849988446d38aa6d216330b1fe9c0e81c4f0de9da7d8437ce5d1bf`  
		Last Modified: Thu, 17 Oct 2024 05:05:56 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; 386

```console
$ docker pull varnish@sha256:2e7f7fbcb5e9f5828cc258fafdd263a7a03036101c463771858a2c401dec0d1c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97133295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e95963497935e8a245ce7ef275e65611eefa1822de42ef90a163c2ed9501596`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:39:19 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Thu, 17 Oct 2024 00:39:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:30:12 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Thu, 17 Oct 2024 06:30:13 GMT
ARG VARNISH_VERSION=6.0.13
# Thu, 17 Oct 2024 06:30:13 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Thu, 17 Oct 2024 06:30:13 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 06:32:20 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 17 Oct 2024 06:32:20 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 06:32:20 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:32:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 06:32:21 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 06:32:21 GMT
CMD []
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1692d1a37679dcc33d7c210823d4a8285f5a731f674b2d905c226bbfd229f9b2`  
		Last Modified: Thu, 17 Oct 2024 06:33:58 GMT  
		Size: 64.7 MB (64718749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8326c5577321e2d7c296f00eb279fc6ec2262d56a0174bac8cf7937dd396ea1b`  
		Last Modified: Thu, 17 Oct 2024 06:33:46 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; ppc64le

```console
$ docker pull varnish@sha256:2c8f1d0368a69bc5c2ee47b9d94f0bdcf9d118fbbde53f423561900c4dc3858b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141302279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5736a990cf4e26bd0a1bc3fe3ec7b0802ec358817f77ec0c2e156ead2389fc76`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 19:23:58 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 11 Nov 2024 19:23:58 GMT
ARG VARNISH_VERSION=6.0.13
# Mon, 11 Nov 2024 19:23:58 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Mon, 11 Nov 2024 19:23:58 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:26:46 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 11 Nov 2024 19:26:50 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:26:50 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:26:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:26:51 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:26:51 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024faa4175d8beb860272554bc0e100344a0c97b054fc77c1c40a922d76c59`  
		Last Modified: Mon, 11 Nov 2024 19:28:34 GMT  
		Size: 108.2 MB (108179358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10630b3b7197b4a3a286d5733c694832216644d75fa86c19b976da37325476ce`  
		Last Modified: Mon, 11 Nov 2024 19:28:17 GMT  
		Size: 720.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; s390x

```console
$ docker pull varnish@sha256:32841bc0f7503dfd6c456ad94c8f78007b3100045965cadbe18f456099ac8abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76258728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded5fdd03ff15a069138878b85906a9196b3fc3ba8c26fafc22d244e44a35304`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 04 Sep 2024 21:43:26 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Wed, 04 Sep 2024 21:43:27 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:09:00 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Thu, 05 Sep 2024 00:09:00 GMT
ARG VARNISH_VERSION=6.0.13
# Thu, 05 Sep 2024 00:09:01 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Thu, 05 Sep 2024 00:09:01 GMT
ENV VARNISH_SIZE=100M
# Thu, 05 Sep 2024 00:10:22 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 05 Sep 2024 00:10:23 GMT
WORKDIR /etc/varnish
# Thu, 05 Sep 2024 00:10:23 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Thu, 05 Sep 2024 00:10:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 05 Sep 2024 00:10:23 GMT
EXPOSE 80 8443
# Thu, 05 Sep 2024 00:10:23 GMT
CMD []
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea184e408ee8a3bda0cdce477eb9806a10f7582bd36e0d18c1a36e645d4a8524`  
		Last Modified: Thu, 05 Sep 2024 00:17:59 GMT  
		Size: 46.6 MB (46594565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce81c8f7a8af9c632886d9382a8489c48b529c3a16f50cd485b6cd0cc3a2a19`  
		Last Modified: Thu, 05 Sep 2024 00:17:53 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7`

```console
$ docker pull varnish@sha256:aa7a267d1f81c5a25afe8f8bf9564afaf2283ed881875c522368d1c851ee5eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7` - linux; amd64

```console
$ docker pull varnish@sha256:473a365a47b3924acfff098e50b11b5a7dddf85eb6410510d7603a79ae5b9819
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143571464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf901dfb1ff62a3354df282815f622b5f9d80f2d9cbf79d5f631e79880aa75b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:47:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:21:40 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:21:41 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:21:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:21:41 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:24:29 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:24:30 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:24:30 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:24:30 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:24:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:24:30 GMT
USER varnish
# Mon, 11 Nov 2024 19:24:30 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:24:30 GMT
CMD []
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b6c27a0e656bd6126f9e6864704320981ac160f96a8e7aa60d87d0c90d555`  
		Last Modified: Mon, 11 Nov 2024 19:28:40 GMT  
		Size: 114.4 MB (114443164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ef812aabddccb1e640bb3e0fd84f2131fdf18c8fd16e2c4fa001b90345913d`  
		Last Modified: Mon, 11 Nov 2024 19:28:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7c214d545fb51bddfc72672ec4b485c790f25944231f99ad88df647ea1633e`  
		Last Modified: Mon, 11 Nov 2024 19:28:25 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:09fa967a3734e998bc40c821f2aaac9f662b19cc4d8128f4f7539a8f415e51bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111902796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c89d50e0512cf945fe5387283919dde94dc64e4e14506a2cc299b2947ff945c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:14:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:01:42 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:01:42 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:01:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:04:26 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:04:27 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:04:27 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:04:27 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:04:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:04:27 GMT
USER varnish
# Mon, 11 Nov 2024 19:04:27 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:04:28 GMT
CMD []
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45340662fa888cd2c956a219eee55d85c9884e74ed7c2c8b190c75c4c228fe93`  
		Last Modified: Mon, 11 Nov 2024 19:08:35 GMT  
		Size: 87.2 MB (87182589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2968e51bc5ec1ae7f50010dc5bb6bfa6571d6aef19c94f1f1e5e16c8632941`  
		Last Modified: Mon, 11 Nov 2024 19:08:22 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7aea8f0dc8796615b1fd29856d0553a50ebede0636ec71fba5514f6204aef21`  
		Last Modified: Mon, 11 Nov 2024 19:08:22 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f48619e02046c9af13f268a07bede3a7a78b680cb9c2112bcce994f3ab460b61
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129471374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2132f890084490ffc3b73e9c39b61060b16910b199c70ed53b181afb9e40db43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:58:36 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 04:58:36 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 04:58:37 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 04:58:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 04:58:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 04:58:37 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 04:58:37 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 05:00:52 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 05:00:53 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 05:00:54 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:00:54 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 05:00:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 05:00:54 GMT
USER varnish
# Thu, 17 Oct 2024 05:00:54 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 05:00:54 GMT
CMD []
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920f519bf05c04d947f910172f37dce9ca0bbf963f1627fa0433bcc0e4bf1506`  
		Last Modified: Thu, 17 Oct 2024 05:05:24 GMT  
		Size: 100.3 MB (100313021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a3f7e29289fec2dd6bf4fecf9367acb76ede80ed1cc8f300448dd91c0646a7`  
		Last Modified: Thu, 17 Oct 2024 05:05:13 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c1228ae30d329a4960da1af63d6e65f94295d2cf8e2c80f5957214bcd5f3f4`  
		Last Modified: Thu, 17 Oct 2024 05:05:13 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7` - linux; 386

```console
$ docker pull varnish@sha256:085f6d78fedf3d4656ea01f15687a83332d7fc4aaa9d80499d8a2553e59a4a1a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132117281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413a0a3cc64a13bf910924c242db8cec758743d582affb345a093f71475faf7b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:22:53 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 06:22:53 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 06:22:53 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 06:22:53 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 06:22:53 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 06:22:54 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 06:22:54 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 06:22:54 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 06:22:54 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 06:22:54 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 06:22:54 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 06:22:54 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 06:26:22 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 06:26:24 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 06:26:24 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:26:24 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 06:26:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 06:26:24 GMT
USER varnish
# Thu, 17 Oct 2024 06:26:24 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 06:26:24 GMT
CMD []
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c1974f89470975cedfe396e8b7531b9e7622560780bf5374bbef539f470e4b`  
		Last Modified: Thu, 17 Oct 2024 06:33:05 GMT  
		Size: 102.0 MB (101971003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437837e9ea2fa4bd8003ec0b24a7a4258714d01ecc009241dd79167b04d3acf3`  
		Last Modified: Thu, 17 Oct 2024 06:32:45 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cc9f9a19b333c1983c27fe7183d0d3d6499d005ab11eae2040034bd9a58610`  
		Last Modified: Thu, 17 Oct 2024 06:32:45 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7` - linux; ppc64le

```console
$ docker pull varnish@sha256:34ab4663d420d85b80bd205c1e48a318bc28d68be25c4d1c75202e7b9c49ea11
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147923000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbc72bc9a11e86e971b4b2fdaa161a6da96e170b9a4e18e9c05c639cf069eb1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:21:04 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:18:03 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:18:03 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:18:05 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:18:05 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:18:06 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:21:53 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:21:57 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:21:57 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:21:58 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:21:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:21:59 GMT
USER varnish
# Mon, 11 Nov 2024 19:21:59 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:21:59 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc660fddb560ae891f20fc8c92bc7fc6b2df2d316ae49eeabca76f342356985d`  
		Last Modified: Mon, 11 Nov 2024 19:27:38 GMT  
		Size: 114.8 MB (114798788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18cf87e0e197131e69ae697e540008a63b9fbfccaf3f3b08d75c444d232a6eb`  
		Last Modified: Mon, 11 Nov 2024 19:27:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcbdc78514c3748ff4fbb278dca8a900d7f3313053e6cf770a0b24826498af0`  
		Last Modified: Mon, 11 Nov 2024 19:27:19 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7` - linux; s390x

```console
$ docker pull varnish@sha256:a6ec5d891316fa5d9a7de24ce870da964ef4c2fa4ee44b395f7d67170fde681d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112580334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236aaceab22f4762ec0de9bbfcef5865a636024ce50e501f67041974f02a6dc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:52:07 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:52:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:52:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:54:39 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:54:42 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:54:42 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:54:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:54:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:54:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:54:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:54:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40600a7c357ca6c02d49abca4f445d2a67e0f817e8924a4bbc3dbc0ab1c07a8c`  
		Last Modified: Thu, 17 Oct 2024 03:58:35 GMT  
		Size: 85.1 MB (85088239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9308896b060d89adc522b31775c270cc70aed098d14753b9f0d1d1adf9b33b`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715abd33b2fc67e17eeb2b082afb3c4d1233b5432aac4c5f07735d030f32a7cc`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7-alpine`

```console
$ docker pull varnish@sha256:8c75fc43cd73af27c0a0eae8836a8e89a6a6dfea3cb83569a573408a45f4f832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:f9a6ed1122a1272818ab4e56c5a81d9908b7ae5a7dc9c2df159a078d5195e7c6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75570805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ece2b8e0df29e6b825718cdb19ac0f897d6f8adc5a3c57905bb535daf6198f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:23:25 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:24:34 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:24:34 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:24:35 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:24:35 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:24:35 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:24:36 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:25:50 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:25:51 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:25:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:25:51 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:25:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:25:51 GMT
USER varnish
# Mon, 11 Nov 2024 19:25:51 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:25:52 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc27487cc250bc592fd70c8ac0a2278844de02e2bca5233887217853ac3561d`  
		Last Modified: Mon, 11 Nov 2024 19:29:01 GMT  
		Size: 72.1 MB (72149072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35948d6f1cc5ca4ab5bbee5f71dc552987d57a05fdccda3bb876e3ba249ec614`  
		Last Modified: Mon, 11 Nov 2024 19:28:52 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa217e907f0770ee2c4275dff2abd111342e46e4285ff7073da5b0a46a6f684b`  
		Last Modified: Mon, 11 Nov 2024 19:28:52 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:f111b003e4b88290cf74e60cf41a645d6831dbc65edf999a1a5bbfe8aac3478f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59334516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eef60ae264c3363c2700356ad1884fb9597ee1977dbc7b9e27ea7f59fd7fc81`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 22:00:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:04:36 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:04:36 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:06:01 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:06:02 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:06:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:06:02 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:06:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:06:02 GMT
USER varnish
# Mon, 11 Nov 2024 19:06:02 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:06:02 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac3ec7de75010c1a0c40ceef5f10d53d02ebf108b070595259b0535ce8ecd0a`  
		Last Modified: Mon, 11 Nov 2024 19:08:54 GMT  
		Size: 56.4 MB (56404825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe5e61d33a8b011b6c04e813585ce227edabf073beee9b1d12bcd9b7429cded`  
		Last Modified: Mon, 11 Nov 2024 19:08:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebeebcf04b930bc64fbcca40c39626e1ebc5a464323245fa4752b91acebf3c2`  
		Last Modified: Mon, 11 Nov 2024 19:08:47 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfe1aee4c184e7663ae040322c0c31b35cd0b8d728f3865de30a67122a3b6f0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70044444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21780c1110170fc966cb4748ff00e2f7a188c43db1b48811bfecc073ecb4c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:43:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:43:49 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:43:49 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:43:49 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:43:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:43:49 GMT
USER varnish
# Tue, 17 Sep 2024 21:43:49 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:43:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28ba5a4402255fdab74468444d26ba5a450bb3bf85308c8bfa037ff0d2e4481`  
		Last Modified: Tue, 17 Sep 2024 21:44:39 GMT  
		Size: 66.7 MB (66683314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c872d5a9b252a340d0656fdcf4b6e90d931d11f137f0b44b4444ff273873a2`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2c1c538a2d3a1c5c004361f6a4b125a2483e3a3dc1816c7ea8775f6c7c7f9`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:3da50e3f81938d063b7849dd4d8f83dc09552bc13b68a0788b2bdaeb5e8966be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75354425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30579799344622ba130f6df5e174e986f75c31937b2056a74c7c6fb36422fccb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:44:36 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:44:37 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:44:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:44:37 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:44:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:44:37 GMT
USER varnish
# Tue, 17 Sep 2024 21:44:37 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:44:37 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cf3a67921019e12988f9ad85476068512edd6a81f7f1f8ff550e83621a3d5b`  
		Last Modified: Tue, 17 Sep 2024 21:45:52 GMT  
		Size: 72.1 MB (72098793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084453347407e41595c52dccc0c96066e579395b163b8855f44de0467535b488`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f056ae9a1c7699ea5fdc01d3dc561774699e1aa2129eb8e22bbd0390ccb475`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:da96bbb111d4301ba75841431f7625c4ed522962484bb173e79ffac68f85b861
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72947419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87adb260a8c333d5d831c17bafc9110886aeee1e61fdd0b145f1969168919a80`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:21:40 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:22:13 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:22:13 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:22:15 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:23:38 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:23:40 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:23:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:23:41 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:23:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:23:41 GMT
USER varnish
# Mon, 11 Nov 2024 19:23:42 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:23:42 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768b370a9245d801ab4973b219ec9c4855ea1f4320ac1872b444612038dd8add`  
		Last Modified: Mon, 11 Nov 2024 19:28:01 GMT  
		Size: 69.6 MB (69580930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1c2ee11b85b8737f3ca520a37b96fd08d1adf2cd7243ec08896624e216b893`  
		Last Modified: Mon, 11 Nov 2024 19:27:51 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a23933ee6f4218c9ea1c559a2ffb10ee4b6cf6fc0f733cedac0c7228eea7a3`  
		Last Modified: Mon, 11 Nov 2024 19:27:51 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:db93041e4e4775e3d4159fa1b5b7c65545a3c0dbdc12de978cded0fc36515740
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65242016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af743e848584bd94e6cf9c19729927521a094bfc5207e0be3a21a8aef0830a4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:46:31 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:46:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:46:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:47:54 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:47:56 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:47:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:47:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:47:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:47:57 GMT
USER varnish
# Tue, 17 Sep 2024 21:47:57 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:47:57 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6d1365d833d5e91a3423b89a361a19152c440c149cd7d12c26e57e64b3069`  
		Last Modified: Tue, 17 Sep 2024 21:49:17 GMT  
		Size: 62.0 MB (61986636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75daf6d5dfbb1c97cf59aa4a63c806056b36c721839e21899802891464a067a6`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85307912e9b6db6d28beb66a825b1bbaaafe821d0bc5b7156ff36f607b7b94c2`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5`

```console
$ docker pull varnish@sha256:1630336e4aedf961c898ef01c13b99d3cda3b737660367410358559f24762bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.5` - linux; amd64

```console
$ docker pull varnish@sha256:4099ad9731a73b34541194e4490e3bc14e360e2522efb25ba30a2da6cc94894e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134865011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363cc58de3151a01aa94dccd83d502a2396e53450fd2a5f6b27f64b103dc843e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:50:44 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 04:50:44 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 04:50:44 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 04:50:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 04:50:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 04:50:45 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 04:53:18 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 04:53:19 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 04:53:19 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 04:53:19 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 04:53:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 04:53:20 GMT
USER varnish
# Thu, 17 Oct 2024 04:53:20 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 04:53:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ffbda90d6eab4093d088f5885aa38fd128bfe320d22f2951c372c2f67e3571`  
		Last Modified: Thu, 17 Oct 2024 04:56:09 GMT  
		Size: 105.7 MB (105736712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9623dcc07f3b385327c67ed943229adab5e9b2ea28f68163ac7f2cac1065f454`  
		Last Modified: Thu, 17 Oct 2024 04:55:55 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bb41e92330d176f97215235065761e1728e30826d39aea25b21bdc997430ec`  
		Last Modified: Thu, 17 Oct 2024 04:55:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; arm variant v7

```console
$ docker pull varnish@sha256:494279659aa62c069005aa8bd25cf183bb4968411c422ff1dce5d89ff6e16c24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105119244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6812a7a4bd88f6b261bfdd893abbaef8d92e956a62db3ba44798f5b3a855a79`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:17:22 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 06:17:22 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 06:17:22 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 06:17:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 06:17:23 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 06:19:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 06:19:51 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 06:19:52 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:19:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 06:19:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 06:19:52 GMT
USER varnish
# Thu, 17 Oct 2024 06:19:53 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 06:19:53 GMT
CMD []
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad3b48ea8d1b7cb39b019859fcab406e3584dd27e6f0fc8bb5af23a66fdf8f`  
		Last Modified: Thu, 17 Oct 2024 06:22:56 GMT  
		Size: 80.4 MB (80399037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d543d6d81d053da02cdcb5ed1a7e2b55e75313153335bb5afb96daa63468b3db`  
		Last Modified: Thu, 17 Oct 2024 06:22:43 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8879f1a68f9a03673fd50e901c151fe6ead69c10a3b236b1ec6474cd05922d63`  
		Last Modified: Thu, 17 Oct 2024 06:22:43 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ab6f5772f86a2a2b514c68488b1a7f7b795a4e044b7b620fd27a4684b5631ea3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129345086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6df37591b236482441fd618ef265ac12071d90d62cdb176e1e63d5600bf058b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 05:01:01 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 05:01:01 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 05:01:01 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 05:01:02 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 05:01:02 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 05:03:13 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 05:03:15 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 05:03:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:03:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 05:03:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 05:03:15 GMT
USER varnish
# Thu, 17 Oct 2024 05:03:15 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 05:03:15 GMT
CMD []
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85195e87a1f736d399209c1a2b91f39f4aea8b83515ab0e35a407306b0bd7c2`  
		Last Modified: Thu, 17 Oct 2024 05:05:47 GMT  
		Size: 100.2 MB (100186734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c532f6c8497e85f990231c0248e5ee7c66459f10f00ae97c90c8616bcf8b42c`  
		Last Modified: Thu, 17 Oct 2024 05:05:36 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac32a9ce62e5e32c859dab01b71bd3851d06d622c9618814eb6abeef214e22d5`  
		Last Modified: Thu, 17 Oct 2024 05:05:36 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; 386

```console
$ docker pull varnish@sha256:8cecc1c037409ff774426f9a7e9d2d439299259a999af6458e055e3ca73bd479
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132017498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a679115dba88f398f66a08162bedb11c07a58e7f0a513d5592d6f794a5b6363a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:26:33 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 06:26:33 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 06:26:33 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 06:26:33 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 06:26:33 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 06:26:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 06:26:34 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 06:26:34 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 06:26:34 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 06:26:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 06:26:34 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 06:29:53 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 06:29:55 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 06:29:55 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:29:55 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 06:29:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 06:29:55 GMT
USER varnish
# Thu, 17 Oct 2024 06:29:56 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 06:29:56 GMT
CMD []
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b23ee4714739cc950bca22358090e4514e9f6f2834e9ac3583d0098726c79d`  
		Last Modified: Thu, 17 Oct 2024 06:33:37 GMT  
		Size: 101.9 MB (101871221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e06a39a6add609cf4d500e5bcaa2456f14a4246d73561e5be47d64a6ce966e`  
		Last Modified: Thu, 17 Oct 2024 06:33:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b5182473e3894fd11b9a6659d4a725595373bd609f1dfbd986925beff61606`  
		Last Modified: Thu, 17 Oct 2024 06:33:17 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; ppc64le

```console
$ docker pull varnish@sha256:9da2339b7c4f5fbc3df9e284868c821c81d77f309b54db2bbc764e534516ca4d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137797884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc79a1b5a152d76ce01bae93f78e6d7ae09ac0a63dbb45ac5ce6d4eb9c825a5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:25:01 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 03:25:02 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 03:25:03 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 03:25:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 03:25:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:25:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:25:03 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:28:37 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:28:40 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:28:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:28:41 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:28:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:28:41 GMT
USER varnish
# Thu, 17 Oct 2024 03:28:41 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:28:42 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991d76c211cf2a830615bad768d92d195caf1d6e2619b51c8eb761e653788f31`  
		Last Modified: Thu, 17 Oct 2024 03:29:58 GMT  
		Size: 104.7 MB (104673673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0aca5c509ba6f97231d47b9babaa090d823353b46b4a935003063b5ba0c3ea`  
		Last Modified: Thu, 17 Oct 2024 03:29:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9936b87d11cac7008368bb672920d65fc0b57fa32deee7ea18bc08d46e3ca0`  
		Last Modified: Thu, 17 Oct 2024 03:29:41 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; s390x

```console
$ docker pull varnish@sha256:3b34914b870a2edcd4dd9a97188bbb81856632bab5c2a8995edde96f1cc02223
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112468709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507d02e4180de236b10a91c68373d0cc6e694c2846cd995591b7b9fb14990a5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:55:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 03:55:11 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 03:55:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 03:55:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:55:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:55:12 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:57:38 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:57:41 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:57:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:57:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:57:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:57:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:57:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:57:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd94e8d5ab3de910e95edb78fdde0ea66df13e7ad9bf916690b28bafe248b6d`  
		Last Modified: Thu, 17 Oct 2024 03:58:58 GMT  
		Size: 85.0 MB (84976615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d9b29663f7a9f46b498ff8d0ec7cc98b7dbbc8fc084607283f531c314bd3ec`  
		Last Modified: Thu, 17 Oct 2024 03:58:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de3b12e1922df954d52eb1e54ca2ac9a195a03b65fc0169437b9deebc0ce263`  
		Last Modified: Thu, 17 Oct 2024 03:58:45 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5-alpine`

```console
$ docker pull varnish@sha256:d92362a83ce30bfd76c14777917466e76ce02e5ae154d08097435d28aed181be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.5-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:59c3a09fc5abfcf1e68bd38d438688b7d0c83569e0a65c816969f83c90c13273
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73215829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f0db10e5790bfe29bd8386463af42eb77b410cb236646e6cd7360a0a9cd1d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:46:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 02:46:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 02:46:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 02:46:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 02:46:48 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:48:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:48:01 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:48:01 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:48:01 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:48:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:48:01 GMT
USER varnish
# Sat, 07 Sep 2024 02:48:02 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:48:02 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d285cdda36ba02e39fb5db5899ec835cee363b7ad2b87db63f3466c8e3527e`  
		Last Modified: Sat, 07 Sep 2024 02:53:41 GMT  
		Size: 69.8 MB (69794098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c3d3db1cd5550aceec91aca8a9a5acc85970f5d33b92957a32cb32b8653f63`  
		Last Modified: Sat, 07 Sep 2024 02:53:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babcaa75a49952cbb065a2d7ac35803afdabcc27c20e4167bee80ebe34d7d2b4`  
		Last Modified: Sat, 07 Sep 2024 02:53:33 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7fa07b0786b863dc266f351943439c8aafe5c3f1b93a8ac717ba1b00c802e9c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57421050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e86e2caef22106bf8ecd12f84c635b831a9666146b0dd59490107dad72d475a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:53:17 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 06 Sep 2024 23:53:17 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 06 Sep 2024 23:53:18 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 06 Sep 2024 23:53:18 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 06 Sep 2024 23:53:18 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 06 Sep 2024 23:53:18 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 06 Sep 2024 23:53:18 GMT
ENV VARNISH_SIZE=100M
# Fri, 06 Sep 2024 23:54:36 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 06 Sep 2024 23:54:37 GMT
WORKDIR /etc/varnish
# Fri, 06 Sep 2024 23:54:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:54:38 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 06 Sep 2024 23:54:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 06 Sep 2024 23:54:38 GMT
USER varnish
# Fri, 06 Sep 2024 23:54:38 GMT
EXPOSE 80 8443
# Fri, 06 Sep 2024 23:54:38 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41154e939d991f21ae1b190b52d812049226a428aa6bed870d4e144e9496d9c7`  
		Last Modified: Sat, 07 Sep 2024 00:00:34 GMT  
		Size: 54.5 MB (54491364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6660d44e064182554dc06b729533de25fcc0f86a3b8274bc4f1f15100ea84`  
		Last Modified: Sat, 07 Sep 2024 00:00:28 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf5f2ac481a3f8c6a07650a539c5e858231e5eff291d331151f75229b0d6216`  
		Last Modified: Sat, 07 Sep 2024 00:00:28 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a6ea3915acfc6f2cff98f8e6397b051c2f1486e0b1abffc2a9b5f4b6fcf44726
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69922870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6fa80545d0146358c54e3b460875cbe64c34292c8ec0e2a5ee4d89825e37d8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:32:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 02:32:42 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 02:32:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 02:32:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 02:32:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 02:32:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 02:32:43 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:33:48 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:33:48 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:33:48 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:33:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:33:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:33:48 GMT
USER varnish
# Sat, 07 Sep 2024 02:33:49 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:33:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7c041f1a08d6904c5fc431550f1b46f386b1e8a0a15f60420d3f1c3f8e4956`  
		Last Modified: Sat, 07 Sep 2024 02:38:29 GMT  
		Size: 66.6 MB (66561743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13493d62ebb9230283c31f2c29616815b7261d8ea5ce1fef5cee06eca895d48a`  
		Last Modified: Sat, 07 Sep 2024 02:38:23 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b528f8eb0911d23806e92337fc161ee9f7ffd889a3fc47faac4df88c1ff84d`  
		Last Modified: Sat, 07 Sep 2024 02:38:23 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; 386

```console
$ docker pull varnish@sha256:055811aff351b9a4185b26939c7b779ba64ef187e21b5c1ab3ebfae72c5dd2b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75241120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b353d90e6191bdd87206bdce7c566b1a283c71ab91f523afb89549543eb7c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:57:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 01:57:46 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 01:57:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 01:57:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 01:57:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 01:57:47 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 01:59:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 01:59:50 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 01:59:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 01:59:51 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 01:59:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 01:59:51 GMT
USER varnish
# Sat, 07 Sep 2024 01:59:51 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 01:59:51 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60754c4db0c99b69e16cf7a780fe7598d9436a865cac09ee645434b131389f24`  
		Last Modified: Sat, 07 Sep 2024 02:06:53 GMT  
		Size: 72.0 MB (71985490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f0f44ea3af290ddd37e769969c21b165b3cefc3b2b6b6f2987ffe285c643c3`  
		Last Modified: Sat, 07 Sep 2024 02:06:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ecb4e83c13f39bf24e6f0249ae24efc4a9b03f78fb80807592920214edf0d3`  
		Last Modified: Sat, 07 Sep 2024 02:06:41 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:aa76e10acc20b1fb7084f61677fc684cfed97b7af8517311b64343a792ef2ce4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70745749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288e480738fe2b36328c2abf2943fa9a47d7ca87a45ccd079f4024dc985cad78`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:59:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 01:59:43 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 01:59:43 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 01:59:43 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 01:59:44 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 01:59:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 01:59:45 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 01:59:45 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 01:59:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 01:59:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 01:59:46 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:01:10 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:01:13 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:01:13 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:01:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:01:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:01:14 GMT
USER varnish
# Sat, 07 Sep 2024 02:01:15 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:01:15 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3498df33b2a1081026de1cfb84850fe2c222aab212e52e98eab4ff6476b50b3b`  
		Last Modified: Sat, 07 Sep 2024 02:06:57 GMT  
		Size: 67.4 MB (67379260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff4a12d0055dfaf864b93acd92e976c57dd6f419497e874f975fb708b18d9f2`  
		Last Modified: Sat, 07 Sep 2024 02:06:47 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a34c42ae7729aeb3a5fdb84562bf98b976005e144797c0774ee4dde3c9ba29`  
		Last Modified: Sat, 07 Sep 2024 02:06:47 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ebc3c7d1e6ec9e99118c774dbc40e74cbee9596bcd758b9ef0d883e5b8221676
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65126002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd6b7c87f2e0740249182cd21889878ccfc7e1ebcd9b00a210f3f696b98373a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:10:28 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 06 Sep 2024 23:10:29 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 06 Sep 2024 23:10:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 06 Sep 2024 23:10:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 06 Sep 2024 23:10:29 GMT
ENV VARNISH_SIZE=100M
# Fri, 06 Sep 2024 23:11:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 06 Sep 2024 23:11:51 GMT
WORKDIR /etc/varnish
# Fri, 06 Sep 2024 23:11:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:11:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 06 Sep 2024 23:11:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 06 Sep 2024 23:11:52 GMT
USER varnish
# Fri, 06 Sep 2024 23:11:52 GMT
EXPOSE 80 8443
# Fri, 06 Sep 2024 23:11:52 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118bc1dbba5c82d06fdfed695d8e80e8044a23b2970f2be0b57056e8cf88c48`  
		Last Modified: Fri, 06 Sep 2024 23:17:56 GMT  
		Size: 61.9 MB (61870619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d03fb424bdb1471e62681e8eceff4cd027a748ea17df08c21c4e3e4fb13763`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72312bc2baecd766ef19ab42b9999881f9ac906a0aa00b1897913ade4e9af474`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5.0`

```console
$ docker pull varnish@sha256:1630336e4aedf961c898ef01c13b99d3cda3b737660367410358559f24762bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.5.0` - linux; amd64

```console
$ docker pull varnish@sha256:4099ad9731a73b34541194e4490e3bc14e360e2522efb25ba30a2da6cc94894e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134865011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363cc58de3151a01aa94dccd83d502a2396e53450fd2a5f6b27f64b103dc843e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:50:44 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 04:50:44 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 04:50:44 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 04:50:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 04:50:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 04:50:45 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 04:53:18 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 04:53:19 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 04:53:19 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 04:53:19 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 04:53:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 04:53:20 GMT
USER varnish
# Thu, 17 Oct 2024 04:53:20 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 04:53:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ffbda90d6eab4093d088f5885aa38fd128bfe320d22f2951c372c2f67e3571`  
		Last Modified: Thu, 17 Oct 2024 04:56:09 GMT  
		Size: 105.7 MB (105736712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9623dcc07f3b385327c67ed943229adab5e9b2ea28f68163ac7f2cac1065f454`  
		Last Modified: Thu, 17 Oct 2024 04:55:55 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bb41e92330d176f97215235065761e1728e30826d39aea25b21bdc997430ec`  
		Last Modified: Thu, 17 Oct 2024 04:55:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:494279659aa62c069005aa8bd25cf183bb4968411c422ff1dce5d89ff6e16c24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105119244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6812a7a4bd88f6b261bfdd893abbaef8d92e956a62db3ba44798f5b3a855a79`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:17:22 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 06:17:22 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 06:17:22 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 06:17:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 06:17:23 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 06:19:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 06:19:51 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 06:19:52 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:19:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 06:19:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 06:19:52 GMT
USER varnish
# Thu, 17 Oct 2024 06:19:53 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 06:19:53 GMT
CMD []
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad3b48ea8d1b7cb39b019859fcab406e3584dd27e6f0fc8bb5af23a66fdf8f`  
		Last Modified: Thu, 17 Oct 2024 06:22:56 GMT  
		Size: 80.4 MB (80399037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d543d6d81d053da02cdcb5ed1a7e2b55e75313153335bb5afb96daa63468b3db`  
		Last Modified: Thu, 17 Oct 2024 06:22:43 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8879f1a68f9a03673fd50e901c151fe6ead69c10a3b236b1ec6474cd05922d63`  
		Last Modified: Thu, 17 Oct 2024 06:22:43 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ab6f5772f86a2a2b514c68488b1a7f7b795a4e044b7b620fd27a4684b5631ea3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129345086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6df37591b236482441fd618ef265ac12071d90d62cdb176e1e63d5600bf058b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 05:01:01 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 05:01:01 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 05:01:01 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 05:01:02 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 05:01:02 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 05:03:13 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 05:03:15 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 05:03:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:03:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 05:03:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 05:03:15 GMT
USER varnish
# Thu, 17 Oct 2024 05:03:15 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 05:03:15 GMT
CMD []
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85195e87a1f736d399209c1a2b91f39f4aea8b83515ab0e35a407306b0bd7c2`  
		Last Modified: Thu, 17 Oct 2024 05:05:47 GMT  
		Size: 100.2 MB (100186734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c532f6c8497e85f990231c0248e5ee7c66459f10f00ae97c90c8616bcf8b42c`  
		Last Modified: Thu, 17 Oct 2024 05:05:36 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac32a9ce62e5e32c859dab01b71bd3851d06d622c9618814eb6abeef214e22d5`  
		Last Modified: Thu, 17 Oct 2024 05:05:36 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; 386

```console
$ docker pull varnish@sha256:8cecc1c037409ff774426f9a7e9d2d439299259a999af6458e055e3ca73bd479
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132017498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a679115dba88f398f66a08162bedb11c07a58e7f0a513d5592d6f794a5b6363a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:26:33 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 06:26:33 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 06:26:33 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 06:26:33 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 06:26:33 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 06:26:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 06:26:34 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 06:26:34 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 06:26:34 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 06:26:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 06:26:34 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 06:29:53 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 06:29:55 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 06:29:55 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:29:55 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 06:29:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 06:29:55 GMT
USER varnish
# Thu, 17 Oct 2024 06:29:56 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 06:29:56 GMT
CMD []
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b23ee4714739cc950bca22358090e4514e9f6f2834e9ac3583d0098726c79d`  
		Last Modified: Thu, 17 Oct 2024 06:33:37 GMT  
		Size: 101.9 MB (101871221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e06a39a6add609cf4d500e5bcaa2456f14a4246d73561e5be47d64a6ce966e`  
		Last Modified: Thu, 17 Oct 2024 06:33:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b5182473e3894fd11b9a6659d4a725595373bd609f1dfbd986925beff61606`  
		Last Modified: Thu, 17 Oct 2024 06:33:17 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:9da2339b7c4f5fbc3df9e284868c821c81d77f309b54db2bbc764e534516ca4d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137797884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc79a1b5a152d76ce01bae93f78e6d7ae09ac0a63dbb45ac5ce6d4eb9c825a5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:25:01 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 03:25:02 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 03:25:03 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 03:25:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 03:25:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:25:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:25:03 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:28:37 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:28:40 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:28:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:28:41 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:28:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:28:41 GMT
USER varnish
# Thu, 17 Oct 2024 03:28:41 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:28:42 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991d76c211cf2a830615bad768d92d195caf1d6e2619b51c8eb761e653788f31`  
		Last Modified: Thu, 17 Oct 2024 03:29:58 GMT  
		Size: 104.7 MB (104673673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0aca5c509ba6f97231d47b9babaa090d823353b46b4a935003063b5ba0c3ea`  
		Last Modified: Thu, 17 Oct 2024 03:29:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9936b87d11cac7008368bb672920d65fc0b57fa32deee7ea18bc08d46e3ca0`  
		Last Modified: Thu, 17 Oct 2024 03:29:41 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; s390x

```console
$ docker pull varnish@sha256:3b34914b870a2edcd4dd9a97188bbb81856632bab5c2a8995edde96f1cc02223
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112468709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507d02e4180de236b10a91c68373d0cc6e694c2846cd995591b7b9fb14990a5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:55:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 03:55:11 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 03:55:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 03:55:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:55:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:55:12 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:57:38 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:57:41 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:57:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:57:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:57:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:57:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:57:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:57:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd94e8d5ab3de910e95edb78fdde0ea66df13e7ad9bf916690b28bafe248b6d`  
		Last Modified: Thu, 17 Oct 2024 03:58:58 GMT  
		Size: 85.0 MB (84976615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d9b29663f7a9f46b498ff8d0ec7cc98b7dbbc8fc084607283f531c314bd3ec`  
		Last Modified: Thu, 17 Oct 2024 03:58:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de3b12e1922df954d52eb1e54ca2ac9a195a03b65fc0169437b9deebc0ce263`  
		Last Modified: Thu, 17 Oct 2024 03:58:45 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5.0-alpine`

```console
$ docker pull varnish@sha256:d92362a83ce30bfd76c14777917466e76ce02e5ae154d08097435d28aed181be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.5.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:59c3a09fc5abfcf1e68bd38d438688b7d0c83569e0a65c816969f83c90c13273
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73215829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f0db10e5790bfe29bd8386463af42eb77b410cb236646e6cd7360a0a9cd1d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:46:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 02:46:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 02:46:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 02:46:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 02:46:48 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:48:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:48:01 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:48:01 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:48:01 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:48:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:48:01 GMT
USER varnish
# Sat, 07 Sep 2024 02:48:02 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:48:02 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d285cdda36ba02e39fb5db5899ec835cee363b7ad2b87db63f3466c8e3527e`  
		Last Modified: Sat, 07 Sep 2024 02:53:41 GMT  
		Size: 69.8 MB (69794098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c3d3db1cd5550aceec91aca8a9a5acc85970f5d33b92957a32cb32b8653f63`  
		Last Modified: Sat, 07 Sep 2024 02:53:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babcaa75a49952cbb065a2d7ac35803afdabcc27c20e4167bee80ebe34d7d2b4`  
		Last Modified: Sat, 07 Sep 2024 02:53:33 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7fa07b0786b863dc266f351943439c8aafe5c3f1b93a8ac717ba1b00c802e9c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57421050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e86e2caef22106bf8ecd12f84c635b831a9666146b0dd59490107dad72d475a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:53:17 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 06 Sep 2024 23:53:17 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 06 Sep 2024 23:53:18 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 06 Sep 2024 23:53:18 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 06 Sep 2024 23:53:18 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 06 Sep 2024 23:53:18 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 06 Sep 2024 23:53:18 GMT
ENV VARNISH_SIZE=100M
# Fri, 06 Sep 2024 23:54:36 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 06 Sep 2024 23:54:37 GMT
WORKDIR /etc/varnish
# Fri, 06 Sep 2024 23:54:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:54:38 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 06 Sep 2024 23:54:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 06 Sep 2024 23:54:38 GMT
USER varnish
# Fri, 06 Sep 2024 23:54:38 GMT
EXPOSE 80 8443
# Fri, 06 Sep 2024 23:54:38 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41154e939d991f21ae1b190b52d812049226a428aa6bed870d4e144e9496d9c7`  
		Last Modified: Sat, 07 Sep 2024 00:00:34 GMT  
		Size: 54.5 MB (54491364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6660d44e064182554dc06b729533de25fcc0f86a3b8274bc4f1f15100ea84`  
		Last Modified: Sat, 07 Sep 2024 00:00:28 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf5f2ac481a3f8c6a07650a539c5e858231e5eff291d331151f75229b0d6216`  
		Last Modified: Sat, 07 Sep 2024 00:00:28 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a6ea3915acfc6f2cff98f8e6397b051c2f1486e0b1abffc2a9b5f4b6fcf44726
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69922870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6fa80545d0146358c54e3b460875cbe64c34292c8ec0e2a5ee4d89825e37d8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:32:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 02:32:42 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 02:32:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 02:32:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 02:32:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 02:32:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 02:32:43 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:33:48 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:33:48 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:33:48 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:33:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:33:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:33:48 GMT
USER varnish
# Sat, 07 Sep 2024 02:33:49 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:33:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7c041f1a08d6904c5fc431550f1b46f386b1e8a0a15f60420d3f1c3f8e4956`  
		Last Modified: Sat, 07 Sep 2024 02:38:29 GMT  
		Size: 66.6 MB (66561743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13493d62ebb9230283c31f2c29616815b7261d8ea5ce1fef5cee06eca895d48a`  
		Last Modified: Sat, 07 Sep 2024 02:38:23 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b528f8eb0911d23806e92337fc161ee9f7ffd889a3fc47faac4df88c1ff84d`  
		Last Modified: Sat, 07 Sep 2024 02:38:23 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:055811aff351b9a4185b26939c7b779ba64ef187e21b5c1ab3ebfae72c5dd2b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75241120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b353d90e6191bdd87206bdce7c566b1a283c71ab91f523afb89549543eb7c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:57:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 01:57:46 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 01:57:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 01:57:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 01:57:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 01:57:47 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 01:59:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 01:59:50 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 01:59:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 01:59:51 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 01:59:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 01:59:51 GMT
USER varnish
# Sat, 07 Sep 2024 01:59:51 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 01:59:51 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60754c4db0c99b69e16cf7a780fe7598d9436a865cac09ee645434b131389f24`  
		Last Modified: Sat, 07 Sep 2024 02:06:53 GMT  
		Size: 72.0 MB (71985490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f0f44ea3af290ddd37e769969c21b165b3cefc3b2b6b6f2987ffe285c643c3`  
		Last Modified: Sat, 07 Sep 2024 02:06:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ecb4e83c13f39bf24e6f0249ae24efc4a9b03f78fb80807592920214edf0d3`  
		Last Modified: Sat, 07 Sep 2024 02:06:41 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:aa76e10acc20b1fb7084f61677fc684cfed97b7af8517311b64343a792ef2ce4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70745749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288e480738fe2b36328c2abf2943fa9a47d7ca87a45ccd079f4024dc985cad78`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:59:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 01:59:43 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 01:59:43 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 01:59:43 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 01:59:44 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 01:59:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 01:59:45 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 01:59:45 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 01:59:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 01:59:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 01:59:46 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:01:10 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:01:13 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:01:13 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:01:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:01:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:01:14 GMT
USER varnish
# Sat, 07 Sep 2024 02:01:15 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:01:15 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3498df33b2a1081026de1cfb84850fe2c222aab212e52e98eab4ff6476b50b3b`  
		Last Modified: Sat, 07 Sep 2024 02:06:57 GMT  
		Size: 67.4 MB (67379260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff4a12d0055dfaf864b93acd92e976c57dd6f419497e874f975fb708b18d9f2`  
		Last Modified: Sat, 07 Sep 2024 02:06:47 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a34c42ae7729aeb3a5fdb84562bf98b976005e144797c0774ee4dde3c9ba29`  
		Last Modified: Sat, 07 Sep 2024 02:06:47 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ebc3c7d1e6ec9e99118c774dbc40e74cbee9596bcd758b9ef0d883e5b8221676
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65126002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd6b7c87f2e0740249182cd21889878ccfc7e1ebcd9b00a210f3f696b98373a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:10:28 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 06 Sep 2024 23:10:29 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 06 Sep 2024 23:10:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 06 Sep 2024 23:10:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 06 Sep 2024 23:10:29 GMT
ENV VARNISH_SIZE=100M
# Fri, 06 Sep 2024 23:11:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 06 Sep 2024 23:11:51 GMT
WORKDIR /etc/varnish
# Fri, 06 Sep 2024 23:11:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:11:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 06 Sep 2024 23:11:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 06 Sep 2024 23:11:52 GMT
USER varnish
# Fri, 06 Sep 2024 23:11:52 GMT
EXPOSE 80 8443
# Fri, 06 Sep 2024 23:11:52 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118bc1dbba5c82d06fdfed695d8e80e8044a23b2970f2be0b57056e8cf88c48`  
		Last Modified: Fri, 06 Sep 2024 23:17:56 GMT  
		Size: 61.9 MB (61870619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d03fb424bdb1471e62681e8eceff4cd027a748ea17df08c21c4e3e4fb13763`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72312bc2baecd766ef19ab42b9999881f9ac906a0aa00b1897913ade4e9af474`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.6`

```console
$ docker pull varnish@sha256:aa7a267d1f81c5a25afe8f8bf9564afaf2283ed881875c522368d1c851ee5eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.6` - linux; amd64

```console
$ docker pull varnish@sha256:473a365a47b3924acfff098e50b11b5a7dddf85eb6410510d7603a79ae5b9819
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143571464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf901dfb1ff62a3354df282815f622b5f9d80f2d9cbf79d5f631e79880aa75b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:47:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:21:40 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:21:41 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:21:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:21:41 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:24:29 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:24:30 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:24:30 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:24:30 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:24:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:24:30 GMT
USER varnish
# Mon, 11 Nov 2024 19:24:30 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:24:30 GMT
CMD []
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b6c27a0e656bd6126f9e6864704320981ac160f96a8e7aa60d87d0c90d555`  
		Last Modified: Mon, 11 Nov 2024 19:28:40 GMT  
		Size: 114.4 MB (114443164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ef812aabddccb1e640bb3e0fd84f2131fdf18c8fd16e2c4fa001b90345913d`  
		Last Modified: Mon, 11 Nov 2024 19:28:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7c214d545fb51bddfc72672ec4b485c790f25944231f99ad88df647ea1633e`  
		Last Modified: Mon, 11 Nov 2024 19:28:25 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6` - linux; arm variant v7

```console
$ docker pull varnish@sha256:09fa967a3734e998bc40c821f2aaac9f662b19cc4d8128f4f7539a8f415e51bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111902796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c89d50e0512cf945fe5387283919dde94dc64e4e14506a2cc299b2947ff945c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:14:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:01:42 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:01:42 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:01:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:04:26 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:04:27 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:04:27 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:04:27 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:04:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:04:27 GMT
USER varnish
# Mon, 11 Nov 2024 19:04:27 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:04:28 GMT
CMD []
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45340662fa888cd2c956a219eee55d85c9884e74ed7c2c8b190c75c4c228fe93`  
		Last Modified: Mon, 11 Nov 2024 19:08:35 GMT  
		Size: 87.2 MB (87182589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2968e51bc5ec1ae7f50010dc5bb6bfa6571d6aef19c94f1f1e5e16c8632941`  
		Last Modified: Mon, 11 Nov 2024 19:08:22 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7aea8f0dc8796615b1fd29856d0553a50ebede0636ec71fba5514f6204aef21`  
		Last Modified: Mon, 11 Nov 2024 19:08:22 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f48619e02046c9af13f268a07bede3a7a78b680cb9c2112bcce994f3ab460b61
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129471374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2132f890084490ffc3b73e9c39b61060b16910b199c70ed53b181afb9e40db43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:58:36 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 04:58:36 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 04:58:37 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 04:58:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 04:58:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 04:58:37 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 04:58:37 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 05:00:52 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 05:00:53 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 05:00:54 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:00:54 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 05:00:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 05:00:54 GMT
USER varnish
# Thu, 17 Oct 2024 05:00:54 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 05:00:54 GMT
CMD []
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920f519bf05c04d947f910172f37dce9ca0bbf963f1627fa0433bcc0e4bf1506`  
		Last Modified: Thu, 17 Oct 2024 05:05:24 GMT  
		Size: 100.3 MB (100313021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a3f7e29289fec2dd6bf4fecf9367acb76ede80ed1cc8f300448dd91c0646a7`  
		Last Modified: Thu, 17 Oct 2024 05:05:13 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c1228ae30d329a4960da1af63d6e65f94295d2cf8e2c80f5957214bcd5f3f4`  
		Last Modified: Thu, 17 Oct 2024 05:05:13 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6` - linux; 386

```console
$ docker pull varnish@sha256:085f6d78fedf3d4656ea01f15687a83332d7fc4aaa9d80499d8a2553e59a4a1a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132117281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413a0a3cc64a13bf910924c242db8cec758743d582affb345a093f71475faf7b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:22:53 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 06:22:53 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 06:22:53 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 06:22:53 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 06:22:53 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 06:22:54 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 06:22:54 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 06:22:54 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 06:22:54 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 06:22:54 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 06:22:54 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 06:22:54 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 06:26:22 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 06:26:24 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 06:26:24 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:26:24 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 06:26:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 06:26:24 GMT
USER varnish
# Thu, 17 Oct 2024 06:26:24 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 06:26:24 GMT
CMD []
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c1974f89470975cedfe396e8b7531b9e7622560780bf5374bbef539f470e4b`  
		Last Modified: Thu, 17 Oct 2024 06:33:05 GMT  
		Size: 102.0 MB (101971003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437837e9ea2fa4bd8003ec0b24a7a4258714d01ecc009241dd79167b04d3acf3`  
		Last Modified: Thu, 17 Oct 2024 06:32:45 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cc9f9a19b333c1983c27fe7183d0d3d6499d005ab11eae2040034bd9a58610`  
		Last Modified: Thu, 17 Oct 2024 06:32:45 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6` - linux; ppc64le

```console
$ docker pull varnish@sha256:34ab4663d420d85b80bd205c1e48a318bc28d68be25c4d1c75202e7b9c49ea11
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147923000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbc72bc9a11e86e971b4b2fdaa161a6da96e170b9a4e18e9c05c639cf069eb1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:21:04 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:18:03 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:18:03 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:18:05 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:18:05 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:18:06 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:21:53 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:21:57 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:21:57 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:21:58 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:21:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:21:59 GMT
USER varnish
# Mon, 11 Nov 2024 19:21:59 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:21:59 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc660fddb560ae891f20fc8c92bc7fc6b2df2d316ae49eeabca76f342356985d`  
		Last Modified: Mon, 11 Nov 2024 19:27:38 GMT  
		Size: 114.8 MB (114798788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18cf87e0e197131e69ae697e540008a63b9fbfccaf3f3b08d75c444d232a6eb`  
		Last Modified: Mon, 11 Nov 2024 19:27:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcbdc78514c3748ff4fbb278dca8a900d7f3313053e6cf770a0b24826498af0`  
		Last Modified: Mon, 11 Nov 2024 19:27:19 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6` - linux; s390x

```console
$ docker pull varnish@sha256:a6ec5d891316fa5d9a7de24ce870da964ef4c2fa4ee44b395f7d67170fde681d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112580334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236aaceab22f4762ec0de9bbfcef5865a636024ce50e501f67041974f02a6dc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:52:07 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:52:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:52:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:54:39 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:54:42 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:54:42 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:54:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:54:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:54:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:54:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:54:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40600a7c357ca6c02d49abca4f445d2a67e0f817e8924a4bbc3dbc0ab1c07a8c`  
		Last Modified: Thu, 17 Oct 2024 03:58:35 GMT  
		Size: 85.1 MB (85088239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9308896b060d89adc522b31775c270cc70aed098d14753b9f0d1d1adf9b33b`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715abd33b2fc67e17eeb2b082afb3c4d1233b5432aac4c5f07735d030f32a7cc`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.6-alpine`

```console
$ docker pull varnish@sha256:8c75fc43cd73af27c0a0eae8836a8e89a6a6dfea3cb83569a573408a45f4f832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.6-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:f9a6ed1122a1272818ab4e56c5a81d9908b7ae5a7dc9c2df159a078d5195e7c6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75570805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ece2b8e0df29e6b825718cdb19ac0f897d6f8adc5a3c57905bb535daf6198f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:23:25 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:24:34 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:24:34 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:24:35 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:24:35 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:24:35 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:24:36 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:25:50 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:25:51 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:25:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:25:51 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:25:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:25:51 GMT
USER varnish
# Mon, 11 Nov 2024 19:25:51 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:25:52 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc27487cc250bc592fd70c8ac0a2278844de02e2bca5233887217853ac3561d`  
		Last Modified: Mon, 11 Nov 2024 19:29:01 GMT  
		Size: 72.1 MB (72149072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35948d6f1cc5ca4ab5bbee5f71dc552987d57a05fdccda3bb876e3ba249ec614`  
		Last Modified: Mon, 11 Nov 2024 19:28:52 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa217e907f0770ee2c4275dff2abd111342e46e4285ff7073da5b0a46a6f684b`  
		Last Modified: Mon, 11 Nov 2024 19:28:52 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:f111b003e4b88290cf74e60cf41a645d6831dbc65edf999a1a5bbfe8aac3478f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59334516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eef60ae264c3363c2700356ad1884fb9597ee1977dbc7b9e27ea7f59fd7fc81`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 22:00:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:04:36 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:04:36 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:06:01 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:06:02 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:06:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:06:02 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:06:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:06:02 GMT
USER varnish
# Mon, 11 Nov 2024 19:06:02 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:06:02 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac3ec7de75010c1a0c40ceef5f10d53d02ebf108b070595259b0535ce8ecd0a`  
		Last Modified: Mon, 11 Nov 2024 19:08:54 GMT  
		Size: 56.4 MB (56404825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe5e61d33a8b011b6c04e813585ce227edabf073beee9b1d12bcd9b7429cded`  
		Last Modified: Mon, 11 Nov 2024 19:08:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebeebcf04b930bc64fbcca40c39626e1ebc5a464323245fa4752b91acebf3c2`  
		Last Modified: Mon, 11 Nov 2024 19:08:47 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfe1aee4c184e7663ae040322c0c31b35cd0b8d728f3865de30a67122a3b6f0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70044444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21780c1110170fc966cb4748ff00e2f7a188c43db1b48811bfecc073ecb4c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:43:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:43:49 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:43:49 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:43:49 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:43:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:43:49 GMT
USER varnish
# Tue, 17 Sep 2024 21:43:49 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:43:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28ba5a4402255fdab74468444d26ba5a450bb3bf85308c8bfa037ff0d2e4481`  
		Last Modified: Tue, 17 Sep 2024 21:44:39 GMT  
		Size: 66.7 MB (66683314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c872d5a9b252a340d0656fdcf4b6e90d931d11f137f0b44b4444ff273873a2`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2c1c538a2d3a1c5c004361f6a4b125a2483e3a3dc1816c7ea8775f6c7c7f9`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6-alpine` - linux; 386

```console
$ docker pull varnish@sha256:3da50e3f81938d063b7849dd4d8f83dc09552bc13b68a0788b2bdaeb5e8966be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75354425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30579799344622ba130f6df5e174e986f75c31937b2056a74c7c6fb36422fccb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:44:36 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:44:37 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:44:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:44:37 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:44:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:44:37 GMT
USER varnish
# Tue, 17 Sep 2024 21:44:37 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:44:37 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cf3a67921019e12988f9ad85476068512edd6a81f7f1f8ff550e83621a3d5b`  
		Last Modified: Tue, 17 Sep 2024 21:45:52 GMT  
		Size: 72.1 MB (72098793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084453347407e41595c52dccc0c96066e579395b163b8855f44de0467535b488`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f056ae9a1c7699ea5fdc01d3dc561774699e1aa2129eb8e22bbd0390ccb475`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:da96bbb111d4301ba75841431f7625c4ed522962484bb173e79ffac68f85b861
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72947419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87adb260a8c333d5d831c17bafc9110886aeee1e61fdd0b145f1969168919a80`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:21:40 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:22:13 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:22:13 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:22:15 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:23:38 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:23:40 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:23:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:23:41 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:23:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:23:41 GMT
USER varnish
# Mon, 11 Nov 2024 19:23:42 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:23:42 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768b370a9245d801ab4973b219ec9c4855ea1f4320ac1872b444612038dd8add`  
		Last Modified: Mon, 11 Nov 2024 19:28:01 GMT  
		Size: 69.6 MB (69580930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1c2ee11b85b8737f3ca520a37b96fd08d1adf2cd7243ec08896624e216b893`  
		Last Modified: Mon, 11 Nov 2024 19:27:51 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a23933ee6f4218c9ea1c559a2ffb10ee4b6cf6fc0f733cedac0c7228eea7a3`  
		Last Modified: Mon, 11 Nov 2024 19:27:51 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:db93041e4e4775e3d4159fa1b5b7c65545a3c0dbdc12de978cded0fc36515740
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65242016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af743e848584bd94e6cf9c19729927521a094bfc5207e0be3a21a8aef0830a4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:46:31 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:46:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:46:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:47:54 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:47:56 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:47:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:47:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:47:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:47:57 GMT
USER varnish
# Tue, 17 Sep 2024 21:47:57 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:47:57 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6d1365d833d5e91a3423b89a361a19152c440c149cd7d12c26e57e64b3069`  
		Last Modified: Tue, 17 Sep 2024 21:49:17 GMT  
		Size: 62.0 MB (61986636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75daf6d5dfbb1c97cf59aa4a63c806056b36c721839e21899802891464a067a6`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85307912e9b6db6d28beb66a825b1bbaaafe821d0bc5b7156ff36f607b7b94c2`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.6.1`

```console
$ docker pull varnish@sha256:e1279b51631247d70ecc38fe4f3e820fe0c7e98080bf293d95b41885739d7f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `varnish:7.6.1` - linux; amd64

```console
$ docker pull varnish@sha256:473a365a47b3924acfff098e50b11b5a7dddf85eb6410510d7603a79ae5b9819
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143571464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf901dfb1ff62a3354df282815f622b5f9d80f2d9cbf79d5f631e79880aa75b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:47:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:21:40 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:21:41 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:21:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:21:41 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:24:29 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:24:30 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:24:30 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:24:30 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:24:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:24:30 GMT
USER varnish
# Mon, 11 Nov 2024 19:24:30 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:24:30 GMT
CMD []
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b6c27a0e656bd6126f9e6864704320981ac160f96a8e7aa60d87d0c90d555`  
		Last Modified: Mon, 11 Nov 2024 19:28:40 GMT  
		Size: 114.4 MB (114443164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ef812aabddccb1e640bb3e0fd84f2131fdf18c8fd16e2c4fa001b90345913d`  
		Last Modified: Mon, 11 Nov 2024 19:28:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7c214d545fb51bddfc72672ec4b485c790f25944231f99ad88df647ea1633e`  
		Last Modified: Mon, 11 Nov 2024 19:28:25 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.1` - linux; arm variant v7

```console
$ docker pull varnish@sha256:09fa967a3734e998bc40c821f2aaac9f662b19cc4d8128f4f7539a8f415e51bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111902796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c89d50e0512cf945fe5387283919dde94dc64e4e14506a2cc299b2947ff945c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:14:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:01:42 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:01:42 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:01:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:04:26 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:04:27 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:04:27 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:04:27 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:04:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:04:27 GMT
USER varnish
# Mon, 11 Nov 2024 19:04:27 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:04:28 GMT
CMD []
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45340662fa888cd2c956a219eee55d85c9884e74ed7c2c8b190c75c4c228fe93`  
		Last Modified: Mon, 11 Nov 2024 19:08:35 GMT  
		Size: 87.2 MB (87182589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2968e51bc5ec1ae7f50010dc5bb6bfa6571d6aef19c94f1f1e5e16c8632941`  
		Last Modified: Mon, 11 Nov 2024 19:08:22 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7aea8f0dc8796615b1fd29856d0553a50ebede0636ec71fba5514f6204aef21`  
		Last Modified: Mon, 11 Nov 2024 19:08:22 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.1` - linux; ppc64le

```console
$ docker pull varnish@sha256:34ab4663d420d85b80bd205c1e48a318bc28d68be25c4d1c75202e7b9c49ea11
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147923000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbc72bc9a11e86e971b4b2fdaa161a6da96e170b9a4e18e9c05c639cf069eb1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:21:04 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:18:03 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:18:03 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:18:05 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:18:05 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:18:06 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:21:53 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:21:57 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:21:57 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:21:58 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:21:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:21:59 GMT
USER varnish
# Mon, 11 Nov 2024 19:21:59 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:21:59 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc660fddb560ae891f20fc8c92bc7fc6b2df2d316ae49eeabca76f342356985d`  
		Last Modified: Mon, 11 Nov 2024 19:27:38 GMT  
		Size: 114.8 MB (114798788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18cf87e0e197131e69ae697e540008a63b9fbfccaf3f3b08d75c444d232a6eb`  
		Last Modified: Mon, 11 Nov 2024 19:27:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcbdc78514c3748ff4fbb278dca8a900d7f3313053e6cf770a0b24826498af0`  
		Last Modified: Mon, 11 Nov 2024 19:27:19 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.6.1-alpine`

```console
$ docker pull varnish@sha256:22412e3c4fdfe1f51520d955a9c896fbaed79a55ce3570259f7b2ce1d82562ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; ppc64le

### `varnish:7.6.1-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:f9a6ed1122a1272818ab4e56c5a81d9908b7ae5a7dc9c2df159a078d5195e7c6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75570805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ece2b8e0df29e6b825718cdb19ac0f897d6f8adc5a3c57905bb535daf6198f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:23:25 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:24:34 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:24:34 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:24:35 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:24:35 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:24:35 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:24:36 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:25:50 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:25:51 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:25:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:25:51 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:25:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:25:51 GMT
USER varnish
# Mon, 11 Nov 2024 19:25:51 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:25:52 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc27487cc250bc592fd70c8ac0a2278844de02e2bca5233887217853ac3561d`  
		Last Modified: Mon, 11 Nov 2024 19:29:01 GMT  
		Size: 72.1 MB (72149072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35948d6f1cc5ca4ab5bbee5f71dc552987d57a05fdccda3bb876e3ba249ec614`  
		Last Modified: Mon, 11 Nov 2024 19:28:52 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa217e907f0770ee2c4275dff2abd111342e46e4285ff7073da5b0a46a6f684b`  
		Last Modified: Mon, 11 Nov 2024 19:28:52 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.1-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:f111b003e4b88290cf74e60cf41a645d6831dbc65edf999a1a5bbfe8aac3478f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59334516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eef60ae264c3363c2700356ad1884fb9597ee1977dbc7b9e27ea7f59fd7fc81`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 22:00:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:04:36 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:04:36 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:06:01 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:06:02 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:06:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:06:02 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:06:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:06:02 GMT
USER varnish
# Mon, 11 Nov 2024 19:06:02 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:06:02 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac3ec7de75010c1a0c40ceef5f10d53d02ebf108b070595259b0535ce8ecd0a`  
		Last Modified: Mon, 11 Nov 2024 19:08:54 GMT  
		Size: 56.4 MB (56404825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe5e61d33a8b011b6c04e813585ce227edabf073beee9b1d12bcd9b7429cded`  
		Last Modified: Mon, 11 Nov 2024 19:08:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebeebcf04b930bc64fbcca40c39626e1ebc5a464323245fa4752b91acebf3c2`  
		Last Modified: Mon, 11 Nov 2024 19:08:47 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.1-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:da96bbb111d4301ba75841431f7625c4ed522962484bb173e79ffac68f85b861
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72947419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87adb260a8c333d5d831c17bafc9110886aeee1e61fdd0b145f1969168919a80`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:21:40 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:22:13 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:22:13 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:22:15 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:23:38 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:23:40 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:23:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:23:41 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:23:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:23:41 GMT
USER varnish
# Mon, 11 Nov 2024 19:23:42 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:23:42 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768b370a9245d801ab4973b219ec9c4855ea1f4320ac1872b444612038dd8add`  
		Last Modified: Mon, 11 Nov 2024 19:28:01 GMT  
		Size: 69.6 MB (69580930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1c2ee11b85b8737f3ca520a37b96fd08d1adf2cd7243ec08896624e216b893`  
		Last Modified: Mon, 11 Nov 2024 19:27:51 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a23933ee6f4218c9ea1c559a2ffb10ee4b6cf6fc0f733cedac0c7228eea7a3`  
		Last Modified: Mon, 11 Nov 2024 19:27:51 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:alpine`

```console
$ docker pull varnish@sha256:8c75fc43cd73af27c0a0eae8836a8e89a6a6dfea3cb83569a573408a45f4f832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:alpine` - linux; amd64

```console
$ docker pull varnish@sha256:f9a6ed1122a1272818ab4e56c5a81d9908b7ae5a7dc9c2df159a078d5195e7c6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75570805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ece2b8e0df29e6b825718cdb19ac0f897d6f8adc5a3c57905bb535daf6198f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:23:25 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:24:34 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:24:34 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:24:35 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:24:35 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:24:35 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:24:36 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:25:50 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:25:51 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:25:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:25:51 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:25:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:25:51 GMT
USER varnish
# Mon, 11 Nov 2024 19:25:51 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:25:52 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc27487cc250bc592fd70c8ac0a2278844de02e2bca5233887217853ac3561d`  
		Last Modified: Mon, 11 Nov 2024 19:29:01 GMT  
		Size: 72.1 MB (72149072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35948d6f1cc5ca4ab5bbee5f71dc552987d57a05fdccda3bb876e3ba249ec614`  
		Last Modified: Mon, 11 Nov 2024 19:28:52 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa217e907f0770ee2c4275dff2abd111342e46e4285ff7073da5b0a46a6f684b`  
		Last Modified: Mon, 11 Nov 2024 19:28:52 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:f111b003e4b88290cf74e60cf41a645d6831dbc65edf999a1a5bbfe8aac3478f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59334516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eef60ae264c3363c2700356ad1884fb9597ee1977dbc7b9e27ea7f59fd7fc81`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 22:00:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:04:36 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:04:36 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:06:01 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:06:02 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:06:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:06:02 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:06:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:06:02 GMT
USER varnish
# Mon, 11 Nov 2024 19:06:02 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:06:02 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac3ec7de75010c1a0c40ceef5f10d53d02ebf108b070595259b0535ce8ecd0a`  
		Last Modified: Mon, 11 Nov 2024 19:08:54 GMT  
		Size: 56.4 MB (56404825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe5e61d33a8b011b6c04e813585ce227edabf073beee9b1d12bcd9b7429cded`  
		Last Modified: Mon, 11 Nov 2024 19:08:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebeebcf04b930bc64fbcca40c39626e1ebc5a464323245fa4752b91acebf3c2`  
		Last Modified: Mon, 11 Nov 2024 19:08:47 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfe1aee4c184e7663ae040322c0c31b35cd0b8d728f3865de30a67122a3b6f0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70044444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21780c1110170fc966cb4748ff00e2f7a188c43db1b48811bfecc073ecb4c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:43:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:43:49 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:43:49 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:43:49 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:43:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:43:49 GMT
USER varnish
# Tue, 17 Sep 2024 21:43:49 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:43:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28ba5a4402255fdab74468444d26ba5a450bb3bf85308c8bfa037ff0d2e4481`  
		Last Modified: Tue, 17 Sep 2024 21:44:39 GMT  
		Size: 66.7 MB (66683314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c872d5a9b252a340d0656fdcf4b6e90d931d11f137f0b44b4444ff273873a2`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2c1c538a2d3a1c5c004361f6a4b125a2483e3a3dc1816c7ea8775f6c7c7f9`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:3da50e3f81938d063b7849dd4d8f83dc09552bc13b68a0788b2bdaeb5e8966be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75354425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30579799344622ba130f6df5e174e986f75c31937b2056a74c7c6fb36422fccb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:44:36 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:44:37 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:44:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:44:37 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:44:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:44:37 GMT
USER varnish
# Tue, 17 Sep 2024 21:44:37 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:44:37 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cf3a67921019e12988f9ad85476068512edd6a81f7f1f8ff550e83621a3d5b`  
		Last Modified: Tue, 17 Sep 2024 21:45:52 GMT  
		Size: 72.1 MB (72098793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084453347407e41595c52dccc0c96066e579395b163b8855f44de0467535b488`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f056ae9a1c7699ea5fdc01d3dc561774699e1aa2129eb8e22bbd0390ccb475`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:da96bbb111d4301ba75841431f7625c4ed522962484bb173e79ffac68f85b861
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72947419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87adb260a8c333d5d831c17bafc9110886aeee1e61fdd0b145f1969168919a80`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:21:40 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:22:13 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:22:13 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:22:15 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:23:38 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:23:40 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:23:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:23:41 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:23:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:23:41 GMT
USER varnish
# Mon, 11 Nov 2024 19:23:42 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:23:42 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768b370a9245d801ab4973b219ec9c4855ea1f4320ac1872b444612038dd8add`  
		Last Modified: Mon, 11 Nov 2024 19:28:01 GMT  
		Size: 69.6 MB (69580930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1c2ee11b85b8737f3ca520a37b96fd08d1adf2cd7243ec08896624e216b893`  
		Last Modified: Mon, 11 Nov 2024 19:27:51 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a23933ee6f4218c9ea1c559a2ffb10ee4b6cf6fc0f733cedac0c7228eea7a3`  
		Last Modified: Mon, 11 Nov 2024 19:27:51 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:db93041e4e4775e3d4159fa1b5b7c65545a3c0dbdc12de978cded0fc36515740
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65242016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af743e848584bd94e6cf9c19729927521a094bfc5207e0be3a21a8aef0830a4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:46:31 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:46:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:46:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:47:54 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:47:56 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:47:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:47:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:47:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:47:57 GMT
USER varnish
# Tue, 17 Sep 2024 21:47:57 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:47:57 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6d1365d833d5e91a3423b89a361a19152c440c149cd7d12c26e57e64b3069`  
		Last Modified: Tue, 17 Sep 2024 21:49:17 GMT  
		Size: 62.0 MB (61986636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75daf6d5dfbb1c97cf59aa4a63c806056b36c721839e21899802891464a067a6`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85307912e9b6db6d28beb66a825b1bbaaafe821d0bc5b7156ff36f607b7b94c2`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:aa7a267d1f81c5a25afe8f8bf9564afaf2283ed881875c522368d1c851ee5eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:473a365a47b3924acfff098e50b11b5a7dddf85eb6410510d7603a79ae5b9819
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143571464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf901dfb1ff62a3354df282815f622b5f9d80f2d9cbf79d5f631e79880aa75b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:47:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:21:40 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:21:41 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:21:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:21:41 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:24:29 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:24:30 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:24:30 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:24:30 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:24:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:24:30 GMT
USER varnish
# Mon, 11 Nov 2024 19:24:30 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:24:30 GMT
CMD []
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b6c27a0e656bd6126f9e6864704320981ac160f96a8e7aa60d87d0c90d555`  
		Last Modified: Mon, 11 Nov 2024 19:28:40 GMT  
		Size: 114.4 MB (114443164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ef812aabddccb1e640bb3e0fd84f2131fdf18c8fd16e2c4fa001b90345913d`  
		Last Modified: Mon, 11 Nov 2024 19:28:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7c214d545fb51bddfc72672ec4b485c790f25944231f99ad88df647ea1633e`  
		Last Modified: Mon, 11 Nov 2024 19:28:25 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:09fa967a3734e998bc40c821f2aaac9f662b19cc4d8128f4f7539a8f415e51bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111902796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c89d50e0512cf945fe5387283919dde94dc64e4e14506a2cc299b2947ff945c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:14:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:01:42 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:01:42 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:01:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:04:26 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:04:27 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:04:27 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:04:27 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:04:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:04:27 GMT
USER varnish
# Mon, 11 Nov 2024 19:04:27 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:04:28 GMT
CMD []
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45340662fa888cd2c956a219eee55d85c9884e74ed7c2c8b190c75c4c228fe93`  
		Last Modified: Mon, 11 Nov 2024 19:08:35 GMT  
		Size: 87.2 MB (87182589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2968e51bc5ec1ae7f50010dc5bb6bfa6571d6aef19c94f1f1e5e16c8632941`  
		Last Modified: Mon, 11 Nov 2024 19:08:22 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7aea8f0dc8796615b1fd29856d0553a50ebede0636ec71fba5514f6204aef21`  
		Last Modified: Mon, 11 Nov 2024 19:08:22 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f48619e02046c9af13f268a07bede3a7a78b680cb9c2112bcce994f3ab460b61
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129471374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2132f890084490ffc3b73e9c39b61060b16910b199c70ed53b181afb9e40db43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:58:36 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 04:58:36 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 04:58:37 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 04:58:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 04:58:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 04:58:37 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 04:58:37 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 05:00:52 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 05:00:53 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 05:00:54 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:00:54 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 05:00:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 05:00:54 GMT
USER varnish
# Thu, 17 Oct 2024 05:00:54 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 05:00:54 GMT
CMD []
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920f519bf05c04d947f910172f37dce9ca0bbf963f1627fa0433bcc0e4bf1506`  
		Last Modified: Thu, 17 Oct 2024 05:05:24 GMT  
		Size: 100.3 MB (100313021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a3f7e29289fec2dd6bf4fecf9367acb76ede80ed1cc8f300448dd91c0646a7`  
		Last Modified: Thu, 17 Oct 2024 05:05:13 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c1228ae30d329a4960da1af63d6e65f94295d2cf8e2c80f5957214bcd5f3f4`  
		Last Modified: Thu, 17 Oct 2024 05:05:13 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:085f6d78fedf3d4656ea01f15687a83332d7fc4aaa9d80499d8a2553e59a4a1a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132117281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413a0a3cc64a13bf910924c242db8cec758743d582affb345a093f71475faf7b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:22:53 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 06:22:53 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 06:22:53 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 06:22:53 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 06:22:53 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 06:22:54 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 06:22:54 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 06:22:54 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 06:22:54 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 06:22:54 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 06:22:54 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 06:22:54 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 06:26:22 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 06:26:24 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 06:26:24 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:26:24 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 06:26:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 06:26:24 GMT
USER varnish
# Thu, 17 Oct 2024 06:26:24 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 06:26:24 GMT
CMD []
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c1974f89470975cedfe396e8b7531b9e7622560780bf5374bbef539f470e4b`  
		Last Modified: Thu, 17 Oct 2024 06:33:05 GMT  
		Size: 102.0 MB (101971003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437837e9ea2fa4bd8003ec0b24a7a4258714d01ecc009241dd79167b04d3acf3`  
		Last Modified: Thu, 17 Oct 2024 06:32:45 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cc9f9a19b333c1983c27fe7183d0d3d6499d005ab11eae2040034bd9a58610`  
		Last Modified: Thu, 17 Oct 2024 06:32:45 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:34ab4663d420d85b80bd205c1e48a318bc28d68be25c4d1c75202e7b9c49ea11
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147923000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbc72bc9a11e86e971b4b2fdaa161a6da96e170b9a4e18e9c05c639cf069eb1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:21:04 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:18:03 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:18:03 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:18:05 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:18:05 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:18:06 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:21:53 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:21:57 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:21:57 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:21:58 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:21:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:21:59 GMT
USER varnish
# Mon, 11 Nov 2024 19:21:59 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:21:59 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc660fddb560ae891f20fc8c92bc7fc6b2df2d316ae49eeabca76f342356985d`  
		Last Modified: Mon, 11 Nov 2024 19:27:38 GMT  
		Size: 114.8 MB (114798788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18cf87e0e197131e69ae697e540008a63b9fbfccaf3f3b08d75c444d232a6eb`  
		Last Modified: Mon, 11 Nov 2024 19:27:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcbdc78514c3748ff4fbb278dca8a900d7f3313053e6cf770a0b24826498af0`  
		Last Modified: Mon, 11 Nov 2024 19:27:19 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:a6ec5d891316fa5d9a7de24ce870da964ef4c2fa4ee44b395f7d67170fde681d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112580334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236aaceab22f4762ec0de9bbfcef5865a636024ce50e501f67041974f02a6dc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:52:07 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:52:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:52:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:54:39 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:54:42 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:54:42 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:54:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:54:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:54:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:54:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:54:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40600a7c357ca6c02d49abca4f445d2a67e0f817e8924a4bbc3dbc0ab1c07a8c`  
		Last Modified: Thu, 17 Oct 2024 03:58:35 GMT  
		Size: 85.1 MB (85088239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9308896b060d89adc522b31775c270cc70aed098d14753b9f0d1d1adf9b33b`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715abd33b2fc67e17eeb2b082afb3c4d1233b5432aac4c5f07735d030f32a7cc`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:8c75fc43cd73af27c0a0eae8836a8e89a6a6dfea3cb83569a573408a45f4f832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:fresh-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:f9a6ed1122a1272818ab4e56c5a81d9908b7ae5a7dc9c2df159a078d5195e7c6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75570805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ece2b8e0df29e6b825718cdb19ac0f897d6f8adc5a3c57905bb535daf6198f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:23:25 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:24:34 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:24:34 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:24:35 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:24:35 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:24:35 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:24:35 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:24:36 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:25:50 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:25:51 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:25:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:25:51 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:25:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:25:51 GMT
USER varnish
# Mon, 11 Nov 2024 19:25:51 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:25:52 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc27487cc250bc592fd70c8ac0a2278844de02e2bca5233887217853ac3561d`  
		Last Modified: Mon, 11 Nov 2024 19:29:01 GMT  
		Size: 72.1 MB (72149072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35948d6f1cc5ca4ab5bbee5f71dc552987d57a05fdccda3bb876e3ba249ec614`  
		Last Modified: Mon, 11 Nov 2024 19:28:52 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa217e907f0770ee2c4275dff2abd111342e46e4285ff7073da5b0a46a6f684b`  
		Last Modified: Mon, 11 Nov 2024 19:28:52 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:f111b003e4b88290cf74e60cf41a645d6831dbc65edf999a1a5bbfe8aac3478f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59334516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eef60ae264c3363c2700356ad1884fb9597ee1977dbc7b9e27ea7f59fd7fc81`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 22:00:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:04:36 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:04:36 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:04:36 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:04:36 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:06:01 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:06:02 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:06:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:06:02 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:06:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:06:02 GMT
USER varnish
# Mon, 11 Nov 2024 19:06:02 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:06:02 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac3ec7de75010c1a0c40ceef5f10d53d02ebf108b070595259b0535ce8ecd0a`  
		Last Modified: Mon, 11 Nov 2024 19:08:54 GMT  
		Size: 56.4 MB (56404825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe5e61d33a8b011b6c04e813585ce227edabf073beee9b1d12bcd9b7429cded`  
		Last Modified: Mon, 11 Nov 2024 19:08:47 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebeebcf04b930bc64fbcca40c39626e1ebc5a464323245fa4752b91acebf3c2`  
		Last Modified: Mon, 11 Nov 2024 19:08:47 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfe1aee4c184e7663ae040322c0c31b35cd0b8d728f3865de30a67122a3b6f0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70044444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21780c1110170fc966cb4748ff00e2f7a188c43db1b48811bfecc073ecb4c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:43:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:43:49 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:43:49 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:43:49 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:43:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:43:49 GMT
USER varnish
# Tue, 17 Sep 2024 21:43:49 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:43:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28ba5a4402255fdab74468444d26ba5a450bb3bf85308c8bfa037ff0d2e4481`  
		Last Modified: Tue, 17 Sep 2024 21:44:39 GMT  
		Size: 66.7 MB (66683314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c872d5a9b252a340d0656fdcf4b6e90d931d11f137f0b44b4444ff273873a2`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2c1c538a2d3a1c5c004361f6a4b125a2483e3a3dc1816c7ea8775f6c7c7f9`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:3da50e3f81938d063b7849dd4d8f83dc09552bc13b68a0788b2bdaeb5e8966be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75354425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30579799344622ba130f6df5e174e986f75c31937b2056a74c7c6fb36422fccb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:44:36 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:44:37 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:44:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:44:37 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:44:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:44:37 GMT
USER varnish
# Tue, 17 Sep 2024 21:44:37 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:44:37 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cf3a67921019e12988f9ad85476068512edd6a81f7f1f8ff550e83621a3d5b`  
		Last Modified: Tue, 17 Sep 2024 21:45:52 GMT  
		Size: 72.1 MB (72098793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084453347407e41595c52dccc0c96066e579395b163b8855f44de0467535b488`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f056ae9a1c7699ea5fdc01d3dc561774699e1aa2129eb8e22bbd0390ccb475`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:da96bbb111d4301ba75841431f7625c4ed522962484bb173e79ffac68f85b861
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72947419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87adb260a8c333d5d831c17bafc9110886aeee1e61fdd0b145f1969168919a80`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:21:40 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:22:13 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:22:13 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:22:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:22:15 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:22:15 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:23:38 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:23:40 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:23:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:23:41 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:23:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:23:41 GMT
USER varnish
# Mon, 11 Nov 2024 19:23:42 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:23:42 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768b370a9245d801ab4973b219ec9c4855ea1f4320ac1872b444612038dd8add`  
		Last Modified: Mon, 11 Nov 2024 19:28:01 GMT  
		Size: 69.6 MB (69580930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1c2ee11b85b8737f3ca520a37b96fd08d1adf2cd7243ec08896624e216b893`  
		Last Modified: Mon, 11 Nov 2024 19:27:51 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a23933ee6f4218c9ea1c559a2ffb10ee4b6cf6fc0f733cedac0c7228eea7a3`  
		Last Modified: Mon, 11 Nov 2024 19:27:51 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:db93041e4e4775e3d4159fa1b5b7c65545a3c0dbdc12de978cded0fc36515740
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65242016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af743e848584bd94e6cf9c19729927521a094bfc5207e0be3a21a8aef0830a4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:46:31 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:46:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:46:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:47:54 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:47:56 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:47:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:47:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:47:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:47:57 GMT
USER varnish
# Tue, 17 Sep 2024 21:47:57 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:47:57 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6d1365d833d5e91a3423b89a361a19152c440c149cd7d12c26e57e64b3069`  
		Last Modified: Tue, 17 Sep 2024 21:49:17 GMT  
		Size: 62.0 MB (61986636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75daf6d5dfbb1c97cf59aa4a63c806056b36c721839e21899802891464a067a6`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85307912e9b6db6d28beb66a825b1bbaaafe821d0bc5b7156ff36f607b7b94c2`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:aa7a267d1f81c5a25afe8f8bf9564afaf2283ed881875c522368d1c851ee5eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:473a365a47b3924acfff098e50b11b5a7dddf85eb6410510d7603a79ae5b9819
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143571464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf901dfb1ff62a3354df282815f622b5f9d80f2d9cbf79d5f631e79880aa75b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:47:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:21:40 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:21:40 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:21:41 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:21:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:21:41 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:21:41 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:24:29 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:24:30 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:24:30 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:24:30 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:24:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:24:30 GMT
USER varnish
# Mon, 11 Nov 2024 19:24:30 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:24:30 GMT
CMD []
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b6c27a0e656bd6126f9e6864704320981ac160f96a8e7aa60d87d0c90d555`  
		Last Modified: Mon, 11 Nov 2024 19:28:40 GMT  
		Size: 114.4 MB (114443164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ef812aabddccb1e640bb3e0fd84f2131fdf18c8fd16e2c4fa001b90345913d`  
		Last Modified: Mon, 11 Nov 2024 19:28:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7c214d545fb51bddfc72672ec4b485c790f25944231f99ad88df647ea1633e`  
		Last Modified: Mon, 11 Nov 2024 19:28:25 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:09fa967a3734e998bc40c821f2aaac9f662b19cc4d8128f4f7539a8f415e51bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111902796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c89d50e0512cf945fe5387283919dde94dc64e4e14506a2cc299b2947ff945c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:14:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:01:42 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:01:42 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:01:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:01:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:01:43 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:04:26 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:04:27 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:04:27 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:04:27 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:04:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:04:27 GMT
USER varnish
# Mon, 11 Nov 2024 19:04:27 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:04:28 GMT
CMD []
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45340662fa888cd2c956a219eee55d85c9884e74ed7c2c8b190c75c4c228fe93`  
		Last Modified: Mon, 11 Nov 2024 19:08:35 GMT  
		Size: 87.2 MB (87182589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2968e51bc5ec1ae7f50010dc5bb6bfa6571d6aef19c94f1f1e5e16c8632941`  
		Last Modified: Mon, 11 Nov 2024 19:08:22 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7aea8f0dc8796615b1fd29856d0553a50ebede0636ec71fba5514f6204aef21`  
		Last Modified: Mon, 11 Nov 2024 19:08:22 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f48619e02046c9af13f268a07bede3a7a78b680cb9c2112bcce994f3ab460b61
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129471374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2132f890084490ffc3b73e9c39b61060b16910b199c70ed53b181afb9e40db43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:58:36 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 04:58:36 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 04:58:37 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 04:58:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 04:58:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 04:58:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 04:58:37 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 04:58:37 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 05:00:52 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 05:00:53 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 05:00:54 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:00:54 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 05:00:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 05:00:54 GMT
USER varnish
# Thu, 17 Oct 2024 05:00:54 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 05:00:54 GMT
CMD []
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920f519bf05c04d947f910172f37dce9ca0bbf963f1627fa0433bcc0e4bf1506`  
		Last Modified: Thu, 17 Oct 2024 05:05:24 GMT  
		Size: 100.3 MB (100313021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a3f7e29289fec2dd6bf4fecf9367acb76ede80ed1cc8f300448dd91c0646a7`  
		Last Modified: Thu, 17 Oct 2024 05:05:13 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c1228ae30d329a4960da1af63d6e65f94295d2cf8e2c80f5957214bcd5f3f4`  
		Last Modified: Thu, 17 Oct 2024 05:05:13 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:085f6d78fedf3d4656ea01f15687a83332d7fc4aaa9d80499d8a2553e59a4a1a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132117281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413a0a3cc64a13bf910924c242db8cec758743d582affb345a093f71475faf7b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:22:53 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 06:22:53 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 06:22:53 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 06:22:53 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 06:22:53 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 06:22:54 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 06:22:54 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 06:22:54 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 06:22:54 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 06:22:54 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 06:22:54 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 06:22:54 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 06:26:22 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 06:26:24 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 06:26:24 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:26:24 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 06:26:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 06:26:24 GMT
USER varnish
# Thu, 17 Oct 2024 06:26:24 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 06:26:24 GMT
CMD []
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c1974f89470975cedfe396e8b7531b9e7622560780bf5374bbef539f470e4b`  
		Last Modified: Thu, 17 Oct 2024 06:33:05 GMT  
		Size: 102.0 MB (101971003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437837e9ea2fa4bd8003ec0b24a7a4258714d01ecc009241dd79167b04d3acf3`  
		Last Modified: Thu, 17 Oct 2024 06:32:45 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cc9f9a19b333c1983c27fe7183d0d3d6499d005ab11eae2040034bd9a58610`  
		Last Modified: Thu, 17 Oct 2024 06:32:45 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:34ab4663d420d85b80bd205c1e48a318bc28d68be25c4d1c75202e7b9c49ea11
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147923000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbc72bc9a11e86e971b4b2fdaa161a6da96e170b9a4e18e9c05c639cf069eb1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:21:04 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 11 Nov 2024 19:18:03 GMT
ARG VARNISH_VERSION=7.6.1
# Mon, 11 Nov 2024 19:18:03 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Mon, 11 Nov 2024 19:18:04 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Mon, 11 Nov 2024 19:18:05 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Mon, 11 Nov 2024 19:18:05 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Mon, 11 Nov 2024 19:18:06 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:18:06 GMT
ENV VSM_NOPID=1
# Mon, 11 Nov 2024 19:21:53 GMT
# ARGS: DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.1 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Mon, 11 Nov 2024 19:21:57 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:21:57 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:21:58 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Mon, 11 Nov 2024 19:21:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:21:59 GMT
USER varnish
# Mon, 11 Nov 2024 19:21:59 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:21:59 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc660fddb560ae891f20fc8c92bc7fc6b2df2d316ae49eeabca76f342356985d`  
		Last Modified: Mon, 11 Nov 2024 19:27:38 GMT  
		Size: 114.8 MB (114798788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18cf87e0e197131e69ae697e540008a63b9fbfccaf3f3b08d75c444d232a6eb`  
		Last Modified: Mon, 11 Nov 2024 19:27:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcbdc78514c3748ff4fbb278dca8a900d7f3313053e6cf770a0b24826498af0`  
		Last Modified: Mon, 11 Nov 2024 19:27:19 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:a6ec5d891316fa5d9a7de24ce870da964ef4c2fa4ee44b395f7d67170fde681d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112580334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236aaceab22f4762ec0de9bbfcef5865a636024ce50e501f67041974f02a6dc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:52:07 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:52:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:52:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:54:39 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:54:42 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:54:42 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:54:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:54:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:54:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:54:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:54:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40600a7c357ca6c02d49abca4f445d2a67e0f817e8924a4bbc3dbc0ab1c07a8c`  
		Last Modified: Thu, 17 Oct 2024 03:58:35 GMT  
		Size: 85.1 MB (85088239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9308896b060d89adc522b31775c270cc70aed098d14753b9f0d1d1adf9b33b`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715abd33b2fc67e17eeb2b082afb3c4d1233b5432aac4c5f07735d030f32a7cc`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old`

```console
$ docker pull varnish@sha256:1630336e4aedf961c898ef01c13b99d3cda3b737660367410358559f24762bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:4099ad9731a73b34541194e4490e3bc14e360e2522efb25ba30a2da6cc94894e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134865011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363cc58de3151a01aa94dccd83d502a2396e53450fd2a5f6b27f64b103dc843e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:50:44 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 04:50:44 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 04:50:44 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 04:50:45 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 04:50:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 04:50:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 04:50:45 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 04:53:18 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 04:53:19 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 04:53:19 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 04:53:19 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 04:53:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 04:53:20 GMT
USER varnish
# Thu, 17 Oct 2024 04:53:20 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 04:53:20 GMT
CMD []
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ffbda90d6eab4093d088f5885aa38fd128bfe320d22f2951c372c2f67e3571`  
		Last Modified: Thu, 17 Oct 2024 04:56:09 GMT  
		Size: 105.7 MB (105736712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9623dcc07f3b385327c67ed943229adab5e9b2ea28f68163ac7f2cac1065f454`  
		Last Modified: Thu, 17 Oct 2024 04:55:55 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bb41e92330d176f97215235065761e1728e30826d39aea25b21bdc997430ec`  
		Last Modified: Thu, 17 Oct 2024 04:55:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:494279659aa62c069005aa8bd25cf183bb4968411c422ff1dce5d89ff6e16c24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105119244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6812a7a4bd88f6b261bfdd893abbaef8d92e956a62db3ba44798f5b3a855a79`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:17:22 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 06:17:22 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 06:17:22 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 06:17:22 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 06:17:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 06:17:23 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 06:19:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 06:19:51 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 06:19:52 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:19:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 06:19:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 06:19:52 GMT
USER varnish
# Thu, 17 Oct 2024 06:19:53 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 06:19:53 GMT
CMD []
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ad3b48ea8d1b7cb39b019859fcab406e3584dd27e6f0fc8bb5af23a66fdf8f`  
		Last Modified: Thu, 17 Oct 2024 06:22:56 GMT  
		Size: 80.4 MB (80399037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d543d6d81d053da02cdcb5ed1a7e2b55e75313153335bb5afb96daa63468b3db`  
		Last Modified: Thu, 17 Oct 2024 06:22:43 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8879f1a68f9a03673fd50e901c151fe6ead69c10a3b236b1ec6474cd05922d63`  
		Last Modified: Thu, 17 Oct 2024 06:22:43 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ab6f5772f86a2a2b514c68488b1a7f7b795a4e044b7b620fd27a4684b5631ea3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129345086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6df37591b236482441fd618ef265ac12071d90d62cdb176e1e63d5600bf058b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 05:01:01 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 05:01:01 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 05:01:01 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 05:01:01 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 05:01:02 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 05:01:02 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 05:03:13 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 05:03:15 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 05:03:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:03:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 05:03:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 05:03:15 GMT
USER varnish
# Thu, 17 Oct 2024 05:03:15 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 05:03:15 GMT
CMD []
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85195e87a1f736d399209c1a2b91f39f4aea8b83515ab0e35a407306b0bd7c2`  
		Last Modified: Thu, 17 Oct 2024 05:05:47 GMT  
		Size: 100.2 MB (100186734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c532f6c8497e85f990231c0248e5ee7c66459f10f00ae97c90c8616bcf8b42c`  
		Last Modified: Thu, 17 Oct 2024 05:05:36 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac32a9ce62e5e32c859dab01b71bd3851d06d622c9618814eb6abeef214e22d5`  
		Last Modified: Thu, 17 Oct 2024 05:05:36 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:8cecc1c037409ff774426f9a7e9d2d439299259a999af6458e055e3ca73bd479
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132017498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a679115dba88f398f66a08162bedb11c07a58e7f0a513d5592d6f794a5b6363a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:26:33 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 06:26:33 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 06:26:33 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 06:26:33 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 06:26:33 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 06:26:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 06:26:34 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 06:26:34 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 06:26:34 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 06:26:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 06:26:34 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 06:29:53 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 06:29:55 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 06:29:55 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:29:55 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 06:29:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 06:29:55 GMT
USER varnish
# Thu, 17 Oct 2024 06:29:56 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 06:29:56 GMT
CMD []
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b23ee4714739cc950bca22358090e4514e9f6f2834e9ac3583d0098726c79d`  
		Last Modified: Thu, 17 Oct 2024 06:33:37 GMT  
		Size: 101.9 MB (101871221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e06a39a6add609cf4d500e5bcaa2456f14a4246d73561e5be47d64a6ce966e`  
		Last Modified: Thu, 17 Oct 2024 06:33:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b5182473e3894fd11b9a6659d4a725595373bd609f1dfbd986925beff61606`  
		Last Modified: Thu, 17 Oct 2024 06:33:17 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:9da2339b7c4f5fbc3df9e284868c821c81d77f309b54db2bbc764e534516ca4d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137797884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc79a1b5a152d76ce01bae93f78e6d7ae09ac0a63dbb45ac5ce6d4eb9c825a5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:25:01 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 03:25:02 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 03:25:03 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 03:25:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 03:25:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:25:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:25:03 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:28:37 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:28:40 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:28:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:28:41 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:28:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:28:41 GMT
USER varnish
# Thu, 17 Oct 2024 03:28:41 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:28:42 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991d76c211cf2a830615bad768d92d195caf1d6e2619b51c8eb761e653788f31`  
		Last Modified: Thu, 17 Oct 2024 03:29:58 GMT  
		Size: 104.7 MB (104673673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0aca5c509ba6f97231d47b9babaa090d823353b46b4a935003063b5ba0c3ea`  
		Last Modified: Thu, 17 Oct 2024 03:29:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9936b87d11cac7008368bb672920d65fc0b57fa32deee7ea18bc08d46e3ca0`  
		Last Modified: Thu, 17 Oct 2024 03:29:41 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:3b34914b870a2edcd4dd9a97188bbb81856632bab5c2a8995edde96f1cc02223
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112468709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507d02e4180de236b10a91c68373d0cc6e694c2846cd995591b7b9fb14990a5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:55:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 03:55:11 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 03:55:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 03:55:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:55:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:55:12 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:57:38 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:57:41 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:57:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:57:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:57:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:57:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:57:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:57:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd94e8d5ab3de910e95edb78fdde0ea66df13e7ad9bf916690b28bafe248b6d`  
		Last Modified: Thu, 17 Oct 2024 03:58:58 GMT  
		Size: 85.0 MB (84976615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d9b29663f7a9f46b498ff8d0ec7cc98b7dbbc8fc084607283f531c314bd3ec`  
		Last Modified: Thu, 17 Oct 2024 03:58:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de3b12e1922df954d52eb1e54ca2ac9a195a03b65fc0169437b9deebc0ce263`  
		Last Modified: Thu, 17 Oct 2024 03:58:45 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:d92362a83ce30bfd76c14777917466e76ce02e5ae154d08097435d28aed181be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:59c3a09fc5abfcf1e68bd38d438688b7d0c83569e0a65c816969f83c90c13273
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73215829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f0db10e5790bfe29bd8386463af42eb77b410cb236646e6cd7360a0a9cd1d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:46:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 02:46:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 02:46:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 02:46:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 02:46:48 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:48:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:48:01 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:48:01 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:48:01 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:48:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:48:01 GMT
USER varnish
# Sat, 07 Sep 2024 02:48:02 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:48:02 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d285cdda36ba02e39fb5db5899ec835cee363b7ad2b87db63f3466c8e3527e`  
		Last Modified: Sat, 07 Sep 2024 02:53:41 GMT  
		Size: 69.8 MB (69794098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c3d3db1cd5550aceec91aca8a9a5acc85970f5d33b92957a32cb32b8653f63`  
		Last Modified: Sat, 07 Sep 2024 02:53:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babcaa75a49952cbb065a2d7ac35803afdabcc27c20e4167bee80ebe34d7d2b4`  
		Last Modified: Sat, 07 Sep 2024 02:53:33 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7fa07b0786b863dc266f351943439c8aafe5c3f1b93a8ac717ba1b00c802e9c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57421050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e86e2caef22106bf8ecd12f84c635b831a9666146b0dd59490107dad72d475a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:53:17 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 06 Sep 2024 23:53:17 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 06 Sep 2024 23:53:18 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 06 Sep 2024 23:53:18 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 06 Sep 2024 23:53:18 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 06 Sep 2024 23:53:18 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 06 Sep 2024 23:53:18 GMT
ENV VARNISH_SIZE=100M
# Fri, 06 Sep 2024 23:54:36 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 06 Sep 2024 23:54:37 GMT
WORKDIR /etc/varnish
# Fri, 06 Sep 2024 23:54:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:54:38 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 06 Sep 2024 23:54:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 06 Sep 2024 23:54:38 GMT
USER varnish
# Fri, 06 Sep 2024 23:54:38 GMT
EXPOSE 80 8443
# Fri, 06 Sep 2024 23:54:38 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41154e939d991f21ae1b190b52d812049226a428aa6bed870d4e144e9496d9c7`  
		Last Modified: Sat, 07 Sep 2024 00:00:34 GMT  
		Size: 54.5 MB (54491364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6660d44e064182554dc06b729533de25fcc0f86a3b8274bc4f1f15100ea84`  
		Last Modified: Sat, 07 Sep 2024 00:00:28 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf5f2ac481a3f8c6a07650a539c5e858231e5eff291d331151f75229b0d6216`  
		Last Modified: Sat, 07 Sep 2024 00:00:28 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a6ea3915acfc6f2cff98f8e6397b051c2f1486e0b1abffc2a9b5f4b6fcf44726
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69922870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6fa80545d0146358c54e3b460875cbe64c34292c8ec0e2a5ee4d89825e37d8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:32:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 02:32:42 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 02:32:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 02:32:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 02:32:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 02:32:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 02:32:43 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:33:48 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:33:48 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:33:48 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:33:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:33:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:33:48 GMT
USER varnish
# Sat, 07 Sep 2024 02:33:49 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:33:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7c041f1a08d6904c5fc431550f1b46f386b1e8a0a15f60420d3f1c3f8e4956`  
		Last Modified: Sat, 07 Sep 2024 02:38:29 GMT  
		Size: 66.6 MB (66561743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13493d62ebb9230283c31f2c29616815b7261d8ea5ce1fef5cee06eca895d48a`  
		Last Modified: Sat, 07 Sep 2024 02:38:23 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b528f8eb0911d23806e92337fc161ee9f7ffd889a3fc47faac4df88c1ff84d`  
		Last Modified: Sat, 07 Sep 2024 02:38:23 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:055811aff351b9a4185b26939c7b779ba64ef187e21b5c1ab3ebfae72c5dd2b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75241120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b353d90e6191bdd87206bdce7c566b1a283c71ab91f523afb89549543eb7c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:57:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 01:57:46 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 01:57:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 01:57:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 01:57:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 01:57:47 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 01:59:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 01:59:50 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 01:59:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 01:59:51 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 01:59:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 01:59:51 GMT
USER varnish
# Sat, 07 Sep 2024 01:59:51 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 01:59:51 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60754c4db0c99b69e16cf7a780fe7598d9436a865cac09ee645434b131389f24`  
		Last Modified: Sat, 07 Sep 2024 02:06:53 GMT  
		Size: 72.0 MB (71985490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f0f44ea3af290ddd37e769969c21b165b3cefc3b2b6b6f2987ffe285c643c3`  
		Last Modified: Sat, 07 Sep 2024 02:06:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ecb4e83c13f39bf24e6f0249ae24efc4a9b03f78fb80807592920214edf0d3`  
		Last Modified: Sat, 07 Sep 2024 02:06:41 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:aa76e10acc20b1fb7084f61677fc684cfed97b7af8517311b64343a792ef2ce4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70745749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288e480738fe2b36328c2abf2943fa9a47d7ca87a45ccd079f4024dc985cad78`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:59:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 01:59:43 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 01:59:43 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 01:59:43 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 01:59:44 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 01:59:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 01:59:45 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 01:59:45 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 01:59:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 01:59:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 01:59:46 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:01:10 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:01:13 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:01:13 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:01:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:01:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:01:14 GMT
USER varnish
# Sat, 07 Sep 2024 02:01:15 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:01:15 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3498df33b2a1081026de1cfb84850fe2c222aab212e52e98eab4ff6476b50b3b`  
		Last Modified: Sat, 07 Sep 2024 02:06:57 GMT  
		Size: 67.4 MB (67379260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff4a12d0055dfaf864b93acd92e976c57dd6f419497e874f975fb708b18d9f2`  
		Last Modified: Sat, 07 Sep 2024 02:06:47 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a34c42ae7729aeb3a5fdb84562bf98b976005e144797c0774ee4dde3c9ba29`  
		Last Modified: Sat, 07 Sep 2024 02:06:47 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ebc3c7d1e6ec9e99118c774dbc40e74cbee9596bcd758b9ef0d883e5b8221676
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65126002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd6b7c87f2e0740249182cd21889878ccfc7e1ebcd9b00a210f3f696b98373a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:10:28 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 06 Sep 2024 23:10:29 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 06 Sep 2024 23:10:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 06 Sep 2024 23:10:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 06 Sep 2024 23:10:29 GMT
ENV VARNISH_SIZE=100M
# Fri, 06 Sep 2024 23:11:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 06 Sep 2024 23:11:51 GMT
WORKDIR /etc/varnish
# Fri, 06 Sep 2024 23:11:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:11:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 06 Sep 2024 23:11:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 06 Sep 2024 23:11:52 GMT
USER varnish
# Fri, 06 Sep 2024 23:11:52 GMT
EXPOSE 80 8443
# Fri, 06 Sep 2024 23:11:52 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118bc1dbba5c82d06fdfed695d8e80e8044a23b2970f2be0b57056e8cf88c48`  
		Last Modified: Fri, 06 Sep 2024 23:17:56 GMT  
		Size: 61.9 MB (61870619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d03fb424bdb1471e62681e8eceff4cd027a748ea17df08c21c4e3e4fb13763`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72312bc2baecd766ef19ab42b9999881f9ac906a0aa00b1897913ade4e9af474`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:7a9d331853d515b045394b58509a39a3a9f739b88b42dfcd4082afd01c842d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:fda835e89501b3bfcdf7d465340c8b204ca9776ab551e811470e7312b2e99557
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137061519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60db612975912a663a1afc429ed8408e13ceffd856b92f86a133a0c24874b885`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 19:26:03 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 11 Nov 2024 19:26:04 GMT
ARG VARNISH_VERSION=6.0.13
# Mon, 11 Nov 2024 19:26:04 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Mon, 11 Nov 2024 19:26:04 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:27:56 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 11 Nov 2024 19:27:57 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:27:57 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:27:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:27:57 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:27:57 GMT
CMD []
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05966a0c665906794ab09e261101843fb5c1946a37a8c9f94db87bf549d07cf2`  
		Last Modified: Mon, 11 Nov 2024 19:29:30 GMT  
		Size: 107.9 MB (107934514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d590f21368f44a2a0ebd18308949d102dbf743e768c96f3400819bd6684c5da`  
		Last Modified: Mon, 11 Nov 2024 19:29:15 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d7abf2045f401927745a85aaa8a94e711e6885d638e084c8e478570db113a5e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105572118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c035b821cc4a214def698275b58aa9b2581c5ab2146ebb88848edd384d87d162`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 19:06:17 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 11 Nov 2024 19:06:17 GMT
ARG VARNISH_VERSION=6.0.13
# Mon, 11 Nov 2024 19:06:17 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Mon, 11 Nov 2024 19:06:17 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:08:06 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 11 Nov 2024 19:08:08 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:08:08 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:08:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:08:08 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:08:08 GMT
CMD []
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99b753c14f33f1802a71bfa07320696185ee0f185274e88a4b71caf01b5094d`  
		Last Modified: Mon, 11 Nov 2024 19:09:19 GMT  
		Size: 80.9 MB (80853201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c20ff8699d72c6c6aebbfcf4010484d1465c6bad8ffd6f2db47eca38558d769`  
		Last Modified: Mon, 11 Nov 2024 19:09:07 GMT  
		Size: 720.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:6f1af1221e7ee8a04b3fb0e3991ffe092f96a596d3290e2b4865d429438af794
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89962518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2457629dfbc9692b85ed2c1e01b356229137c975953652f73605e95c6379373f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 05:03:26 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Thu, 17 Oct 2024 05:03:26 GMT
ARG VARNISH_VERSION=6.0.13
# Thu, 17 Oct 2024 05:03:26 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Thu, 17 Oct 2024 05:03:26 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 05:04:54 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 17 Oct 2024 05:04:54 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 05:04:54 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:04:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 05:04:54 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 05:04:54 GMT
CMD []
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ffa19fe0da90c936e292635fee1beda4f024fd427bea366b745c939d0372c0`  
		Last Modified: Thu, 17 Oct 2024 05:06:02 GMT  
		Size: 59.9 MB (59886046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b614fa5710849988446d38aa6d216330b1fe9c0e81c4f0de9da7d8437ce5d1bf`  
		Last Modified: Thu, 17 Oct 2024 05:05:56 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:2e7f7fbcb5e9f5828cc258fafdd263a7a03036101c463771858a2c401dec0d1c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97133295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e95963497935e8a245ce7ef275e65611eefa1822de42ef90a163c2ed9501596`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 00:39:19 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Thu, 17 Oct 2024 00:39:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 06:30:12 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Thu, 17 Oct 2024 06:30:13 GMT
ARG VARNISH_VERSION=6.0.13
# Thu, 17 Oct 2024 06:30:13 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Thu, 17 Oct 2024 06:30:13 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 06:32:20 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 17 Oct 2024 06:32:20 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 06:32:20 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Thu, 17 Oct 2024 06:32:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 06:32:21 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 06:32:21 GMT
CMD []
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1692d1a37679dcc33d7c210823d4a8285f5a731f674b2d905c226bbfd229f9b2`  
		Last Modified: Thu, 17 Oct 2024 06:33:58 GMT  
		Size: 64.7 MB (64718749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8326c5577321e2d7c296f00eb279fc6ec2262d56a0174bac8cf7937dd396ea1b`  
		Last Modified: Thu, 17 Oct 2024 06:33:46 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:2c8f1d0368a69bc5c2ee47b9d94f0bdcf9d118fbbde53f423561900c4dc3858b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141302279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5736a990cf4e26bd0a1bc3fe3ec7b0802ec358817f77ec0c2e156ead2389fc76`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 19:23:58 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 11 Nov 2024 19:23:58 GMT
ARG VARNISH_VERSION=6.0.13
# Mon, 11 Nov 2024 19:23:58 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Mon, 11 Nov 2024 19:23:58 GMT
ENV VARNISH_SIZE=100M
# Mon, 11 Nov 2024 19:26:46 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Mon, 11 Nov 2024 19:26:50 GMT
WORKDIR /etc/varnish
# Mon, 11 Nov 2024 19:26:50 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Mon, 11 Nov 2024 19:26:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 11 Nov 2024 19:26:51 GMT
EXPOSE 80 8443
# Mon, 11 Nov 2024 19:26:51 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024faa4175d8beb860272554bc0e100344a0c97b054fc77c1c40a922d76c59`  
		Last Modified: Mon, 11 Nov 2024 19:28:34 GMT  
		Size: 108.2 MB (108179358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10630b3b7197b4a3a286d5733c694832216644d75fa86c19b976da37325476ce`  
		Last Modified: Mon, 11 Nov 2024 19:28:17 GMT  
		Size: 720.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:32841bc0f7503dfd6c456ad94c8f78007b3100045965cadbe18f456099ac8abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76258728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded5fdd03ff15a069138878b85906a9196b3fc3ba8c26fafc22d244e44a35304`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 04 Sep 2024 21:43:26 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Wed, 04 Sep 2024 21:43:27 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:09:00 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Thu, 05 Sep 2024 00:09:00 GMT
ARG VARNISH_VERSION=6.0.13
# Thu, 05 Sep 2024 00:09:01 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Thu, 05 Sep 2024 00:09:01 GMT
ENV VARNISH_SIZE=100M
# Thu, 05 Sep 2024 00:10:22 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 05 Sep 2024 00:10:23 GMT
WORKDIR /etc/varnish
# Thu, 05 Sep 2024 00:10:23 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Thu, 05 Sep 2024 00:10:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 05 Sep 2024 00:10:23 GMT
EXPOSE 80 8443
# Thu, 05 Sep 2024 00:10:23 GMT
CMD []
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea184e408ee8a3bda0cdce477eb9806a10f7582bd36e0d18c1a36e645d4a8524`  
		Last Modified: Thu, 05 Sep 2024 00:17:59 GMT  
		Size: 46.6 MB (46594565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce81c8f7a8af9c632886d9382a8489c48b529c3a16f50cd485b6cd0cc3a2a19`  
		Last Modified: Thu, 05 Sep 2024 00:17:53 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
