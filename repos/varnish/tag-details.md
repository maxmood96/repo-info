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
$ docker pull varnish@sha256:5316358e37d6483a9d871567fe040188e8b7fc5e428b5a05bafa3cea45d519ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:64aeae75a5e09d94db2c76895f130f5c052c39e0eb9c63b483021a69d4c28de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128656670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b94fc1fd2fe475b5f9ad3911e1be01e58c8931190ffadca398cd68343a0fb3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c487894b11ae490ed2019b5325b3f15ce8264a7f2668193a8376330c5aac73e`  
		Last Modified: Tue, 12 Nov 2024 02:13:08 GMT  
		Size: 99.5 MB (99527937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae224e44658b5574e45a2688885f4a0c9eeb5384c107f662c0e0eebd3f28ae8`  
		Last Modified: Tue, 12 Nov 2024 02:13:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:b333b90d72fbe742b7de9f179a1a76808d1693126090444ea2ff54af9c57a255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0548c5fa56eea15d4006a254f506faf603b0af9f9221e78ea7fa24a34b6fcdeb`

```dockerfile
```

-	Layers:
	-	`sha256:0a0e4192aa712731cafe7b8c5f79740ea638b2d38ccf116057d547098cb2a88d`  
		Last Modified: Tue, 12 Nov 2024 02:13:06 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:64869f8649218936d22fbc4ddac170fa656110142449f0c2a1fb5f5267fb824a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99067059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8faed3629ad3e6492ad5706a215925c220a6e34862d0f3cda68d4b0ae6889198`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8456a9b5aa6395e5bd4e0d827bd0199786266efef009523afdebcecd9951a00f`  
		Last Modified: Tue, 12 Nov 2024 15:58:13 GMT  
		Size: 74.3 MB (74347410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3502743e7a4885b252192550073c40c3d05ceb83c44064ac6796510cfb6b9a5`  
		Last Modified: Tue, 12 Nov 2024 15:58:11 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:5f0d72757437b64ee1a3c80df979868e544eb384f4fb590e5db0ae967ceaabff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e599a23ce279cbd2c4813430f6977c69171fa8037fa7b65e0c3c107e3162b3`

```dockerfile
```

-	Layers:
	-	`sha256:5160c1321f23efb99a42de03d1215594467e7b280037b0a7ed07b5fde3b8e9f8`  
		Last Modified: Tue, 12 Nov 2024 15:58:11 GMT  
		Size: 12.7 KB (12733 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:13060403b287be57e729c8c7a32d91064d053531f048ace88bc0cb55214a1fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123444270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e51986dfd32b22e41cb76677e09b2adac44994cca787825e68575a582fe2b19`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d483cab88ce3581e81c671bdbedee568fe2d602a18330b40776c6167df407bb0`  
		Last Modified: Tue, 12 Nov 2024 10:56:57 GMT  
		Size: 94.3 MB (94286175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ebc8794c007f9d635580a20ae6573877e00b8f3a8041a1bb7462e3c42788b8`  
		Last Modified: Tue, 12 Nov 2024 10:56:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:764356b1568f4e67f4b1251ba1968e3042d8233bc750731cafd8463f64016628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d102cb1d9e10a14e729f90fc3bc826702e0487a92406dc4904e7fa079fb17f`

```dockerfile
```

-	Layers:
	-	`sha256:3c08a032f3396b103a97c5bab64e3d19c0ea4417054d633e1edefdd41d0c0247`  
		Last Modified: Tue, 12 Nov 2024 10:56:54 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:9e44f5f6611a706a296ac8eb79a8f3fc24bf660535a26737537d7df64dcf9183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125834427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d0f68a59169a073f7e9a13262a13ef9ab278c9f26f16eaa20989eb450cae32`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867085a972406fae8a8329d78c27fbd0627185530d7c34e8deb90d3aa745189b`  
		Last Modified: Tue, 12 Nov 2024 02:13:27 GMT  
		Size: 95.7 MB (95688237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c02d919c6bdcfa5b509588ac1fab36fbb3ca112216438ac05264938564b6da`  
		Last Modified: Tue, 12 Nov 2024 02:13:24 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:a6e4f7796d9edac4849d087dc2392fd40f320f86dfd6102192ea3e485d452703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca167cb9e7d623d92ae1f70c9360a12e7679a5ece1c28737a0feef42e21193c`

```dockerfile
```

-	Layers:
	-	`sha256:89316ce791ee480dba1b5bb1c8dee974597a82174b9dbf9eb9f716c6336634d8`  
		Last Modified: Tue, 12 Nov 2024 02:13:24 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:806ba0a60018422bfc0e7988cd5f543f50d3353b9cea8de6f2969f11c7fcd557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131456053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d8a38a5ab3ace0c6670d059ac25eadc79275ae555453176228c48d4c66aa88`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25bdec4f657e8fbba9815ff7113c29239ffaaf6708efa25f009e634c61d5949`  
		Last Modified: Tue, 12 Nov 2024 08:27:51 GMT  
		Size: 98.3 MB (98329960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0570a365404c3c134a2b3020ca2943c01ed8874c91ada4690fbb3301384f9c`  
		Last Modified: Tue, 12 Nov 2024 08:27:48 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:1690f179714f2a0f0085d36d5e429db7fa6c3b75732111cc2c88e179b337f452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45fda85373e547abcc335bcdf3a2ced67ee04184050ff096b491e89bf22e716`

```dockerfile
```

-	Layers:
	-	`sha256:c7e87262c0785f1a05e3940da2daf1c465a40e3b9b24de0301103f72ca5b5bab`  
		Last Modified: Tue, 12 Nov 2024 08:27:47 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:2a93f5f6c28e0e74b83a73237b530b9193f6ceb87ea78150ad032487fd80a0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106222947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e841bbcea8c324181247a6a52921d2a07b561859c0c84a3bbbe52256235ef5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427dcfa76abd1ed38c5a3a565bb1ba3fb0611ea06d61285aa2446b4ed5b7459`  
		Last Modified: Tue, 12 Nov 2024 09:00:00 GMT  
		Size: 78.7 MB (78730579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658c572f815bfab73a7ea7d0472638b0693a9889faa06c37927945fedce377d`  
		Last Modified: Tue, 12 Nov 2024 08:59:58 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:1381f215e33733e48b21f30b27edb085109c545a9a1a56909aad61d1891d2f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43375fa1bfd0730d623bb813021c83cc0b9aad4e335a7e9e5dbfcbd4f38f3e1`

```dockerfile
```

-	Layers:
	-	`sha256:a479eed989d6c882bfd7350767c63deca6eb6d124471ffd16b837c0b037ecb75`  
		Last Modified: Tue, 12 Nov 2024 08:59:58 GMT  
		Size: 12.7 KB (12664 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.13`

```console
$ docker pull varnish@sha256:5316358e37d6483a9d871567fe040188e8b7fc5e428b5a05bafa3cea45d519ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:6.0.13` - linux; amd64

```console
$ docker pull varnish@sha256:64aeae75a5e09d94db2c76895f130f5c052c39e0eb9c63b483021a69d4c28de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128656670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b94fc1fd2fe475b5f9ad3911e1be01e58c8931190ffadca398cd68343a0fb3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c487894b11ae490ed2019b5325b3f15ce8264a7f2668193a8376330c5aac73e`  
		Last Modified: Tue, 12 Nov 2024 02:13:08 GMT  
		Size: 99.5 MB (99527937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae224e44658b5574e45a2688885f4a0c9eeb5384c107f662c0e0eebd3f28ae8`  
		Last Modified: Tue, 12 Nov 2024 02:13:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:b333b90d72fbe742b7de9f179a1a76808d1693126090444ea2ff54af9c57a255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0548c5fa56eea15d4006a254f506faf603b0af9f9221e78ea7fa24a34b6fcdeb`

```dockerfile
```

-	Layers:
	-	`sha256:0a0e4192aa712731cafe7b8c5f79740ea638b2d38ccf116057d547098cb2a88d`  
		Last Modified: Tue, 12 Nov 2024 02:13:06 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; arm variant v7

```console
$ docker pull varnish@sha256:64869f8649218936d22fbc4ddac170fa656110142449f0c2a1fb5f5267fb824a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99067059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8faed3629ad3e6492ad5706a215925c220a6e34862d0f3cda68d4b0ae6889198`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8456a9b5aa6395e5bd4e0d827bd0199786266efef009523afdebcecd9951a00f`  
		Last Modified: Tue, 12 Nov 2024 15:58:13 GMT  
		Size: 74.3 MB (74347410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3502743e7a4885b252192550073c40c3d05ceb83c44064ac6796510cfb6b9a5`  
		Last Modified: Tue, 12 Nov 2024 15:58:11 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:5f0d72757437b64ee1a3c80df979868e544eb384f4fb590e5db0ae967ceaabff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e599a23ce279cbd2c4813430f6977c69171fa8037fa7b65e0c3c107e3162b3`

```dockerfile
```

-	Layers:
	-	`sha256:5160c1321f23efb99a42de03d1215594467e7b280037b0a7ed07b5fde3b8e9f8`  
		Last Modified: Tue, 12 Nov 2024 15:58:11 GMT  
		Size: 12.7 KB (12733 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:13060403b287be57e729c8c7a32d91064d053531f048ace88bc0cb55214a1fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123444270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e51986dfd32b22e41cb76677e09b2adac44994cca787825e68575a582fe2b19`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d483cab88ce3581e81c671bdbedee568fe2d602a18330b40776c6167df407bb0`  
		Last Modified: Tue, 12 Nov 2024 10:56:57 GMT  
		Size: 94.3 MB (94286175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ebc8794c007f9d635580a20ae6573877e00b8f3a8041a1bb7462e3c42788b8`  
		Last Modified: Tue, 12 Nov 2024 10:56:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:764356b1568f4e67f4b1251ba1968e3042d8233bc750731cafd8463f64016628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d102cb1d9e10a14e729f90fc3bc826702e0487a92406dc4904e7fa079fb17f`

```dockerfile
```

-	Layers:
	-	`sha256:3c08a032f3396b103a97c5bab64e3d19c0ea4417054d633e1edefdd41d0c0247`  
		Last Modified: Tue, 12 Nov 2024 10:56:54 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; 386

```console
$ docker pull varnish@sha256:9e44f5f6611a706a296ac8eb79a8f3fc24bf660535a26737537d7df64dcf9183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125834427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d0f68a59169a073f7e9a13262a13ef9ab278c9f26f16eaa20989eb450cae32`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867085a972406fae8a8329d78c27fbd0627185530d7c34e8deb90d3aa745189b`  
		Last Modified: Tue, 12 Nov 2024 02:13:27 GMT  
		Size: 95.7 MB (95688237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c02d919c6bdcfa5b509588ac1fab36fbb3ca112216438ac05264938564b6da`  
		Last Modified: Tue, 12 Nov 2024 02:13:24 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:a6e4f7796d9edac4849d087dc2392fd40f320f86dfd6102192ea3e485d452703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca167cb9e7d623d92ae1f70c9360a12e7679a5ece1c28737a0feef42e21193c`

```dockerfile
```

-	Layers:
	-	`sha256:89316ce791ee480dba1b5bb1c8dee974597a82174b9dbf9eb9f716c6336634d8`  
		Last Modified: Tue, 12 Nov 2024 02:13:24 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; ppc64le

```console
$ docker pull varnish@sha256:806ba0a60018422bfc0e7988cd5f543f50d3353b9cea8de6f2969f11c7fcd557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131456053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d8a38a5ab3ace0c6670d059ac25eadc79275ae555453176228c48d4c66aa88`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25bdec4f657e8fbba9815ff7113c29239ffaaf6708efa25f009e634c61d5949`  
		Last Modified: Tue, 12 Nov 2024 08:27:51 GMT  
		Size: 98.3 MB (98329960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0570a365404c3c134a2b3020ca2943c01ed8874c91ada4690fbb3301384f9c`  
		Last Modified: Tue, 12 Nov 2024 08:27:48 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:1690f179714f2a0f0085d36d5e429db7fa6c3b75732111cc2c88e179b337f452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45fda85373e547abcc335bcdf3a2ced67ee04184050ff096b491e89bf22e716`

```dockerfile
```

-	Layers:
	-	`sha256:c7e87262c0785f1a05e3940da2daf1c465a40e3b9b24de0301103f72ca5b5bab`  
		Last Modified: Tue, 12 Nov 2024 08:27:47 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; s390x

```console
$ docker pull varnish@sha256:2a93f5f6c28e0e74b83a73237b530b9193f6ceb87ea78150ad032487fd80a0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106222947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e841bbcea8c324181247a6a52921d2a07b561859c0c84a3bbbe52256235ef5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427dcfa76abd1ed38c5a3a565bb1ba3fb0611ea06d61285aa2446b4ed5b7459`  
		Last Modified: Tue, 12 Nov 2024 09:00:00 GMT  
		Size: 78.7 MB (78730579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658c572f815bfab73a7ea7d0472638b0693a9889faa06c37927945fedce377d`  
		Last Modified: Tue, 12 Nov 2024 08:59:58 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:1381f215e33733e48b21f30b27edb085109c545a9a1a56909aad61d1891d2f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43375fa1bfd0730d623bb813021c83cc0b9aad4e335a7e9e5dbfcbd4f38f3e1`

```dockerfile
```

-	Layers:
	-	`sha256:a479eed989d6c882bfd7350767c63deca6eb6d124471ffd16b837c0b037ecb75`  
		Last Modified: Tue, 12 Nov 2024 08:59:58 GMT  
		Size: 12.7 KB (12664 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7`

```console
$ docker pull varnish@sha256:a14caeb57b4a1bda2acf8f9a0bfc558fb79419442a7038912f4a3992a86e7dc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:7` - linux; amd64

```console
$ docker pull varnish@sha256:f1887f671936054ffce40ee4f1ac606ccfe72ecbf54a6df79dc67e79a354f083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135144957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64030ab17f3104027d4aa981b245b5f353a3ef1a583bc622c8692aaf1bd3e5c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfd8cf94806044561883a9b5e76fea7ce7f77eff1edabe59cf2b4c4be452e12`  
		Last Modified: Tue, 12 Nov 2024 02:39:42 GMT  
		Size: 106.0 MB (106014934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ad340d8a4ae656651b563ccfa5217f12af81402ffc836c45aa31b5c65fde80`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddf610da1690ccf8889523e73d47d0e9d513e38cab68ba61160a2ac0a0f9c9e`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:1e89d4fa68525c8529220acffdf647ea246726bd6ab37aa35e9221e2cdcaa839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d3220eb09a3ea207fb331d02b0a146de411da4d4d4a2ee2e994ffccba95ca2`

```dockerfile
```

-	Layers:
	-	`sha256:c56a34258477eb10afb018c472f107873dd63f5ac6404a6eceb28339f491002f`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:86839bcd6e0cb7c700da3519e17ffa2de352aba06bb5c800cc923956ae2155fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105377035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a5ae730f63fecba7088a0a43a511aacc9d2b481976f45d08cb4274b73f37da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193b251ba0c785db1ddd647e543f7c3014c8a390a2c0a0002206a09d3e39db63`  
		Last Modified: Tue, 12 Nov 2024 15:43:35 GMT  
		Size: 80.7 MB (80656091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f9fd31cb20911ab9074104705f66cae11f91abc0ba6e6003e66ebeef3121e`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621b5dd00fdfdf04c730b796619283911b601d05f42dda275cb82c533dbee4ea`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:25134a573879bc47cf07d340ee755a9380912635d223f1f96cf3946bc998aa51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34405eb30257c2b0c3d220cf008a1a0a41bd82c775a45fee629140dfbffed7fe`

```dockerfile
```

-	Layers:
	-	`sha256:27292e6fd0b558edfdc2d5d8bfead9952722be4febd38d8e07a418b13092fcde`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:697f309f869dcac35ca2c1a8f8a5a0ac652952f4d5a8a1978767bb93617e8fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129638012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ed58a228f0ecd362459fe6be914ab772698b564728270e7363b04da0fe7599`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63d53be09f2e6b77c6452a52054f0b72a7331c67a1142f5f8fe9283991c05c6`  
		Last Modified: Tue, 12 Nov 2024 10:48:44 GMT  
		Size: 100.5 MB (100478623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa1a8b658b784f659f7efda570d5ffcae601bba8a690796a4ae81f5c5277550`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b6ef671bd477fe8f63b7abc44109c2636f8224108541581fdd551fb054ec93`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:1180878f25f57d8761c3fc436a7e25bb7e07343653858b63050fa88952385c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74eafa66c1381bdd46acba9d12438322a74d4e4e5f238f55dedbbda860873f61`

```dockerfile
```

-	Layers:
	-	`sha256:4d08c542d5b23e3e68d57899cb694f5cd7d7454acad345198fc173638a179a78`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; 386

```console
$ docker pull varnish@sha256:f6570237cf1c53b7fc9798f7d7d180fd85a810ec7508ddf678be907805478477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132279504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76828b8ec4ffe1c00bbb572cc26baf17fbba83775e2e3d304b682a579746b6b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c93e3e24b17f6f4677565573caa7c1fcb50037a15b0c78f697c14fec1bfe7f8`  
		Last Modified: Tue, 12 Nov 2024 03:08:20 GMT  
		Size: 102.1 MB (102132018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc93bf5d627266a3e6baee1921524e02dc602ba00b654a6b1c4acec1bfcbeae`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba71f3fb3528c4a90663ba66aa7ce5407d2acd9714e370fd3fbcd9eb7cf5526`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:24b3be81ddf3e057596748db5e20253c7f6c6d297be3700ed517574ee8b3ef10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec81166fd8290376a1f9ed06ddfd54d839dfff16886844dc3053955bb53631f9`

```dockerfile
```

-	Layers:
	-	`sha256:422ba87ca39da1f044b674ae8bc931cc96ba1729b26fee285d45c5071094d056`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; ppc64le

```console
$ docker pull varnish@sha256:23fa67728036d3fa71b0e8d14ecbcc0790ff417cdea386bc0f1f59ea08c54fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138071252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dc50f91816e6b79c2e34d97563e7192ae06ab99f6449de29c2a103f692fbdb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b40b8ec21666519f6048e9809c98d76cdb14cdd1f714124c728cdcde74b201`  
		Last Modified: Tue, 12 Nov 2024 08:16:03 GMT  
		Size: 104.9 MB (104943862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db6d1a8e68ac2829ce68950198a4a5d6bd31792b8f74a392f2a9ca2d0aed14`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb4cbd2942a8262cd4df9b8ff386bbea378dc638bc71d5add84a5825e1375aa`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:71547c8f59c36f7246f88890ac942f133fa911de88c5991e17bcbaf74c65f447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c1f525f9a4ffae1ed0e97818cd93877bad42950f6f42ec26828e94c4a3de20`

```dockerfile
```

-	Layers:
	-	`sha256:0788868b60f7f88bca46fb03d6186b3e94938faefe4fa9d7aa928e4d6c14e177`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; s390x

```console
$ docker pull varnish@sha256:01db2624b5765bf290eed9a2e85931a64f88b7036e7d5c0ae1794097e04cf6e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112730439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36f7f17ec67918459d161c53fcb045125407b045e4df3b449f5903053bde8f2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73895e6530429bd612b9331487ed4811ebd13bf2ac83e86bbb9420ea2779b2bc`  
		Last Modified: Tue, 12 Nov 2024 08:50:39 GMT  
		Size: 85.2 MB (85236779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8731a2370a6a81543907fc7a5ca55c7f89742f1f15ab0d4a6a79017a7c0fc7ab`  
		Last Modified: Tue, 12 Nov 2024 08:50:36 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a191d99ce02a230e9d85421b014d896f26f71503736d3696b654198161bc76`  
		Last Modified: Tue, 12 Nov 2024 08:50:37 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:673ebf6cf0d2a68417555ac882a255175d54bd39747b74c26845c61bd24b04e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe4d455733fd153e0ae17465ac077e05d2343f6531863707618d5063d219ee1`

```dockerfile
```

-	Layers:
	-	`sha256:cf0b77ed9acc0c7df48fbe09538ae5cd332afd2c72a896e0e64419dc124c6553`  
		Last Modified: Tue, 12 Nov 2024 08:50:36 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7-alpine`

```console
$ docker pull varnish@sha256:71e03ca9c56aa1c1bf8312c11de8ff96c71e0ba8151da2bb311d513a287851bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:7-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:734526105e8a73deb29880a30a8ea3ca5a3f6551a2414fb7582126729db82fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75571429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99261e656ffaef89212c06879d8ffd0a2e0a77d3ee3bb46db6ccdb837960f998`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd18d066a2534bb937baae7f43312291bbdebd9e011aa1ca8442a80cb92179`  
		Last Modified: Tue, 12 Nov 2024 02:12:46 GMT  
		Size: 72.1 MB (72149654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b86ea8455fa80ea9c4e840d50734b01b252918032889c7042ff356ac7434a4`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a657ebdd24aea07615cdedf01b64f6e9c56acd221fa99b40c2e04d31eef981c`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:09c5155bd3580c828b54df0e97c73b53d8fdee486fcdf381f0c3c7ab27a4cb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f4de71a1473c6399fc2712271473cd4ccc34f960af41104794679eee8039f`

```dockerfile
```

-	Layers:
	-	`sha256:bac5652b26b6dd3c851c3458214dc4900d0788677478ec151df55d1f34804847`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:136fc141010dc51574484fcbba9ba988f57ea942ac08e0b9423a53e0b2f48a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59334501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b477aac65d60d05a3fcfa069d583ebd04517928f689c8caaa6bf1390f527ea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4146cd2e9bfe30e036ca44a694b114955cfa0d81d82b09f55f4becff13b1ced`  
		Last Modified: Tue, 12 Nov 2024 15:46:43 GMT  
		Size: 56.4 MB (56404722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a695ae119c7fb8c829151e7070c08b103efb05d8e758e7ae88d85fcaeff28c9`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c2e597896bc956b9429c75733917197a7dc70c9b343cad765cdaa7d722eead`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3b12a943b27aff108b8b9aad7e5bb0a5e8e8f27ccb049880a9dc4efb826dd009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b5d647207732a2c16e9e4af34889f07142c3e63378fd5ff475fb2ee90f44cf`

```dockerfile
```

-	Layers:
	-	`sha256:62d334d70e119e6128bc8006bede7b71dcc6a6b8dee06e4ad4ba3f50c496e5d0`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8e0eb93f8254b9caba56523d3363579157f0c8d3ec0a532ef9bf0f6a5ecd5b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72167567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0180a70e03f8f4aa857407e74647e7b95891b4bf4718d3bd13c2739408e48b0f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6b16e5a695b41f99394c63ac1f5280714ebe2fc04c8ab237f0ce944ae25a7b`  
		Last Modified: Tue, 12 Nov 2024 10:50:26 GMT  
		Size: 68.8 MB (68806274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b67a81cdfc65d279272138408dc2d97d0e7e6f9a1703d87ed74465afe07984`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1856d82587e0084100ea903b22480aa95ceb784f24211cc088ad962b7df4e2`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ec593337520ff6285c6c7180e68369420252fd2a5d05d5019442e73bb9f913f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877d07d40294570104e1270b4d4d0f57160d5fd68bf2269a9dda10a73649a3f9`

```dockerfile
```

-	Layers:
	-	`sha256:5af3068eead5af5d8df11ff144a90cde56f3f8235175008ef6c6f025286b84de`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 19.5 KB (19535 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:2834fecda283594871274453290a2c32995405ffbd1cb36b0142dabd64c6aa41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77417612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ff26998f99ce36d7afba43984d1003013021469c34ca26074ea64f985e9b7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ecda4138670a3b812fc81a695fd9039c19b32ab99a3c37222f85b52edc70cb`  
		Last Modified: Tue, 12 Nov 2024 02:13:26 GMT  
		Size: 74.2 MB (74161899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b61ae47424cf9a4da181cec57432c8137ad9fc8abf98d41f809c818e68239c`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1117a17cfb8711601fc64652c8b28f375a3b0783f8cc3ed5a3d355dfc0ee46`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:69f6b1b7913a210b0e541e8bdd0262c619344601b938790e1cbf26ff3fb1cac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b41efdd0d57fb68398c5f7195f729ae351814c67f8a01f40a5f674b8701411`

```dockerfile
```

-	Layers:
	-	`sha256:aa644e18ac20df61b6830d7099aed73d20ddb776d4b1d730e8ab400b3e552afd`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:0cde0eefb059807950a94c89ba0a7317c379a106e0dd07f546c0b7d4b78c448c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72948010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cfaae595c7ec6a3695a9940c2cdfc5de397cc38a6c72e7425365ecc93aeab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ab68b2bfe89abc0133fdb51841b7558cd3586ee23c9b8955f3fa741cfa125`  
		Last Modified: Tue, 12 Nov 2024 08:18:05 GMT  
		Size: 69.6 MB (69581462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeac10562fa7c4a4cc127cdcd8b92b84cf4fe902259905e7f3b3c55619a14f6e`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f4d34a34ad043b6a110f1011b375de170526bb7041207eabe17f0fd587320f`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7ae561aa579e96a66d289967eff239cbfea935754d133129d116533f06246590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe17a004126d973197c0a63377b9daa600da2288a0005a3b8ef9df3a284169b`

```dockerfile
```

-	Layers:
	-	`sha256:74500f417505f2e44d78f9745c3f1b52078f1b5c18ba08622179bd242d83e55f`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:54286872273d28adde7fbdf72b5da06b19e8eacaa8980a0e1b6d719a48feb047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67226471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7576f7982594069fcacce46036976ebd45e0904de4ab77ec25782c98b61d5dcc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a0d631961a00f4bd5b680f2a859bc945e97a1f070cf7983e6afab3074c3bfe`  
		Last Modified: Tue, 12 Nov 2024 08:52:38 GMT  
		Size: 64.0 MB (63971024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4295a934b4400d12d8b9a5d67da1f597255b186adf7fc450f7bd5a2219fadae`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb2d2197875fd4fe8653ace14c11f094ffddfcefb5050905a4ff4b479760a9`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7ca01929086339d2a32f9a35f37fa1e13cd46b0888aaf17861704c93fd883c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c6930c96e9c224ba90924e21554d5c392ac55e9e4dd1126debbf8c30d6dcbb`

```dockerfile
```

-	Layers:
	-	`sha256:242e0ff3285bb7cf08ea74daf6e7f22b247a2d5f070962ca2388c042539258ac`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.5`

```console
$ docker pull varnish@sha256:b618e376341ca332583e924eff5f184098ff96600bfb46473ed184f8f2a61cdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:7.5` - linux; amd64

```console
$ docker pull varnish@sha256:94a0b719b3e2640ded1e17857eb2f17dd52f981f9f438b072e739932b5f3d910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134853200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bee4e830916f6bf61c542a6ca360e4e739860721e8fe4dc0ae3f59d744ce059`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488cc84bf670e30574b1befbf0cd6925eb970dc7edb66339d5cd3b1bb30e4191`  
		Last Modified: Tue, 12 Nov 2024 02:14:01 GMT  
		Size: 105.7 MB (105723175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90d869b88149c7e067a143b4ba1e6c7fd811b4de90818e14cbe2b4c98f08b0`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f43dddd82b1799b259a52d84c8f97886ac435347592ea3d16620fc053e5ba2f`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5` - unknown; unknown

```console
$ docker pull varnish@sha256:2c212cc3ee562ed0bc28a0fd59af348f37ceb4bcc9d597f6cecc236f926abaa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3ecccd4f353937ea748cb36599c9262502f8672808315c03cb94b5e51f2c12`

```dockerfile
```

-	Layers:
	-	`sha256:693b458079835e525c2325e20fa5a2f63e1fad9ef98cac1da5bb0d217f5f84b1`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull varnish@sha256:313a647516a8b72bfab18b3d90290d52ddb51fae4f7011d88f6f61d525ff90d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129354645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2283dd3e564e52b6a551dcc405668a0de000267f5b05b64bc994addea1db1670`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485c9bf90a9b47fc9e115175e1438347317130056edda023687e2b8d1964e297`  
		Last Modified: Tue, 12 Nov 2024 10:53:15 GMT  
		Size: 100.2 MB (100195258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc95d7d18e652867e79c05434cec6f760630bc2e49896fd7dc49fb554e94ed9b`  
		Last Modified: Tue, 12 Nov 2024 10:53:11 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5923fb57e575a592fabbcec9b22a65e1d89d705b55cc286efe87b51d774041`  
		Last Modified: Tue, 12 Nov 2024 10:53:11 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5` - unknown; unknown

```console
$ docker pull varnish@sha256:bacc180149f2fa20e1b9a5c1c59ea3c163d571fbe3ea7a5e05126449d18946ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d7564445cba3ec00c65d853472ed00f181fd1fb723b4811bd561b8f15db5d3`

```dockerfile
```

-	Layers:
	-	`sha256:52679d071576580797ce9d04ef9250cf0cb9d5cf7c6949945788560c45839d52`  
		Last Modified: Tue, 12 Nov 2024 10:53:11 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5` - linux; 386

```console
$ docker pull varnish@sha256:305c470aa3ded14f764b1f41124b7671c2a6b6da6212e89691e475162e8014df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132015848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9e56880094fdd51985109b9cd6c3ca4c284b00969afc88c4ee475b9782b8ca`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd48256999b923e6a5a6939529b9e97e128448e2dc38e5a98226f9c2483b75e7`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 101.9 MB (101868368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178779e0dd46b7438ebf7a2a171ac4a6135b19b9314e50165261851c781b86e6`  
		Last Modified: Tue, 12 Nov 2024 02:14:00 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58aa1c556f9dbfcead83df9fc499ea78d38c9f4274c6506634659101326a3f4`  
		Last Modified: Tue, 12 Nov 2024 02:14:00 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5` - unknown; unknown

```console
$ docker pull varnish@sha256:5a00c08c0e1059006be591813c815e366c428d89439dee428a0074898963ba22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03398597f16554f1cbb20fd418f774939e22db27ebdb04a27d06a0da7686fc5`

```dockerfile
```

-	Layers:
	-	`sha256:7d42e31fc94550053d0e1d64ae23d11da1fbc085f594d5aaae87d550fdabcd40`  
		Last Modified: Tue, 12 Nov 2024 02:14:00 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5` - linux; ppc64le

```console
$ docker pull varnish@sha256:9c5f38d08cf8ac979b28e55d30ba193bef196ae74854cee656900e23092ad734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137788869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed05ddb045976c21f3f59d42db251caec405e05430317746cc5f7ab035461d8c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b21e9096689a76a0e0cb9bf72040ecc6624d1be69a2e1f21a723b52aafb3c`  
		Last Modified: Tue, 12 Nov 2024 08:22:19 GMT  
		Size: 104.7 MB (104661479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4794496f5b55b28c84ebc111fa82dd0b6040610392d9d8a226e714ebc204b503`  
		Last Modified: Tue, 12 Nov 2024 08:22:13 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6698a62de09bc055930556e9fe57e1e2ea0c75f24acf1f6d23d0a931d624feec`  
		Last Modified: Tue, 12 Nov 2024 08:22:13 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5` - unknown; unknown

```console
$ docker pull varnish@sha256:882d801335d297cc2fd2e4ab00849288f38d77e10dfcf86bac6b68227d74ec58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c975b09bc154554c02eb9a2caf76ce99f37751cc7f363a71d364118967352e`

```dockerfile
```

-	Layers:
	-	`sha256:4ec8b5f662b837363dc4c989f263629678518e880b93b31b44247116a72be65e`  
		Last Modified: Tue, 12 Nov 2024 08:22:13 GMT  
		Size: 18.8 KB (18842 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5` - linux; s390x

```console
$ docker pull varnish@sha256:96948e4610b7964e6db67d68abff531467e77c7260448407cb130ba0580691f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112446573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b59f5979e8749072f59210d597a4eaaa302260573c664f2133bcf3ddb4943a7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64e58c8b20bf75539cf7f1f804b16e5553bb1c7bdf0b7b89b4ae337fa8e81b2`  
		Last Modified: Tue, 12 Nov 2024 08:55:42 GMT  
		Size: 85.0 MB (84952911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92103b008c483694642898d758639f8d7c3484eaa82959196c0f41769a3f939d`  
		Last Modified: Tue, 12 Nov 2024 08:55:41 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3ba0561e0f89a79cb397c6c11d6bf6b7d38bcb8ddbda0a8b922b45eb0c6db9`  
		Last Modified: Tue, 12 Nov 2024 08:55:41 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5` - unknown; unknown

```console
$ docker pull varnish@sha256:a2421848df597788940a00db58ec724a441bb8f655476fcd2fed5782c9d3e08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592e17482e7b45896b113979ae7a19c16397c4189c963dd152f8104a69efbf6d`

```dockerfile
```

-	Layers:
	-	`sha256:d3e19ea591bf8e2bee1dd63307d753e1a376b06dc60326880e6833a9ef5772e7`  
		Last Modified: Tue, 12 Nov 2024 08:55:41 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.5-alpine`

```console
$ docker pull varnish@sha256:bdb2d25c2abc7a40dab307580ec6b224bc583159d5e1c958e6490d645e6b5889
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:7.5-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:b88e87349ef0526e4c3c9ca342419cad272ae9d859e191dbc6b905f75d8f584b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75295019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b575452f4dbc566faa94f864acfbdb179386c138abe40cc9915e09ecff1571`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372b7c820710eb59ac6294c8d1bf020b6054fff084972627d39ea76fc7cc730a`  
		Last Modified: Tue, 12 Nov 2024 02:13:00 GMT  
		Size: 71.9 MB (71873252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f479569ba4eee3fba63e1c3f816b50bdcf4f066744c4bd0097f88f53af4839f`  
		Last Modified: Tue, 12 Nov 2024 02:12:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf86448644c977c6a76b0ce5d7e4af967be1b6f53d2232f3c6c9be422e44865e`  
		Last Modified: Tue, 12 Nov 2024 02:12:59 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:94c867e59bc863b7f4fe4ff0b6fbfd7f57f18f0dc0e76b1b75cba108e6e77bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cf59ab507654bbc1044a931afb77617ce5c4b390f3584352628aa914c73b65`

```dockerfile
```

-	Layers:
	-	`sha256:cde3780c4fc1a186faded0b7a02c286b675dbc292b491df0987c0beaf043856f`  
		Last Modified: Tue, 12 Nov 2024 02:12:59 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:253674c883bcfcb4a1f31b239f2c24e7a04db73e6ed93cc65b51e0e26ebecf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59056711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2506cc77824d3689ac65e41e67258e793a249356d53b88cd01aa72a862ac6a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bd5cb802d85c2e91c74445d25463939b0907216488f4851e74e1c702dd991c`  
		Last Modified: Tue, 12 Nov 2024 15:54:26 GMT  
		Size: 56.1 MB (56126931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc1f70712333298b8460020efce137c9f3b37524c3d35457bfd4fbc274271ee`  
		Last Modified: Tue, 12 Nov 2024 15:54:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a637ef13df496373fe769d481b8fcdd358d0a2e8ed259a99a4da9b1a2cc3924a`  
		Last Modified: Tue, 12 Nov 2024 15:54:27 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:828f64dde270181077e8075a682091daf054af6d99b5d8abb0f534ab786b8401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee28dbe0715d58aba783abbbaa9241295728ee4481c563be8b363b906d6955a1`

```dockerfile
```

-	Layers:
	-	`sha256:927ee010c38ad7110b9c618472cbeb1ad23ca2d5510355b0fa703fb599b507ba`  
		Last Modified: Tue, 12 Nov 2024 15:54:24 GMT  
		Size: 18.8 KB (18830 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5b124902dd89c2420a1f911a752f430bf19313e3e18b815792c9758e39c26dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71884849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f379f32b28042de5e48af9c14a5a06d9ce38ed3af4b23f94d8f937d2d3bd101`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eeda6add61cff16b44d1a88d6ed0c519389906f9aa494add7a583a0a6dfbbd`  
		Last Modified: Tue, 12 Nov 2024 10:54:53 GMT  
		Size: 68.5 MB (68523556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dda850377a6ad5f54f6035bac4db6f6bd8457d78e8a65a0af2185cd2181c24`  
		Last Modified: Tue, 12 Nov 2024 10:54:51 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd69887e6e4a1fb9b8e4d849cfbf3f5ca49775c6ee373d04d42434dcc3f898c0`  
		Last Modified: Tue, 12 Nov 2024 10:54:51 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:987df32dfad2fbf229c6e462eca7c3b87207ea40f6ac4613d82471057ea69410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6146b5011321b518fe02b97459fd0768023d3bea266e5bdfd7a3a30c1ee6e6`

```dockerfile
```

-	Layers:
	-	`sha256:d3e0430312d540571589e2c3394223aca871baa1d24f9bdebc3ef643308cceb7`  
		Last Modified: Tue, 12 Nov 2024 10:54:51 GMT  
		Size: 18.9 KB (18855 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5-alpine` - linux; 386

```console
$ docker pull varnish@sha256:74b46799a1437550ecef5b61ac7e66d95ad6d44ba748ae38e5e6d09d21e5ea66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77144543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fa6b8af0ddb441fd25f4feb96591eca4237743aa6e2fc85f583bbc7d0ca724`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707f4676f8155f7af3467c0ac98ee79aa94abe48a3b20ee8c46a3e336b2f7dc`  
		Last Modified: Tue, 12 Nov 2024 02:13:11 GMT  
		Size: 73.9 MB (73888830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c01057ef20a199981392af38cb8ee25e15a9771d7e894f32e37d96856307e8`  
		Last Modified: Tue, 12 Nov 2024 02:13:09 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefde6ea9150f15fb457283144cb065f9c8e206794272d30d384716e897f5fdb`  
		Last Modified: Tue, 12 Nov 2024 02:13:09 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7b046a42b16fce1c6d97d986c9dc237689af1e23622eabfaf3ce45adee7a8636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c364eb2440d15f91c64952e3c8d3ae4e91345d8395081575484fc04066d9fb6`

```dockerfile
```

-	Layers:
	-	`sha256:0f7d8e747f6a04af94ffac3d2651bb786d0d5bc9601daa00cf3eedfbb2b73b89`  
		Last Modified: Tue, 12 Nov 2024 02:13:09 GMT  
		Size: 18.7 KB (18736 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:203426874009453571dbb4535c51e3660ca6c859fbc3322ff583f182a1d503ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72670810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdb5a0b7df6474ab21cc21174102ba749618a7934fd570a897a7d2928a30bf5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315d3daa8ba656231edb65340bf5373311e6520a6a4a77a7ddc98874600de571`  
		Last Modified: Tue, 12 Nov 2024 08:24:18 GMT  
		Size: 69.3 MB (69304263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b6a331cdc0580cd1d9b409a087fb509dd222f62e74498a640741da87752ce1`  
		Last Modified: Tue, 12 Nov 2024 08:24:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4129387d9100b5a099dd0e287fa8e518cea2fd43d789ebd3592ccfe8fd760d8e`  
		Last Modified: Tue, 12 Nov 2024 08:24:15 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6e0fc6f1ead4f281d104c2c6538fa43e0b68090c75ea989df8e94fd823ce9c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4516fb439c1e017c3367b1e817e3bac65c4adb1c0fb759dc647266a5439b5a`

```dockerfile
```

-	Layers:
	-	`sha256:0353503967374c9544a14d9477dd93cca528fc16bc6133418ce8b7d1d281337a`  
		Last Modified: Tue, 12 Nov 2024 08:24:14 GMT  
		Size: 18.8 KB (18800 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:280431fdc972bb57d70db6aba3fd865af9eeb3b2b539f279dd52ec5d5f22d65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66945128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191829c29028766d13169c317eb8dfdd60607e5c2c9a7b4378fe840ec2a796ee`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227ed073ea3a72fe745d5cf9086d188c5621272441c473087c9551d8fe016845`  
		Last Modified: Tue, 12 Nov 2024 08:57:47 GMT  
		Size: 63.7 MB (63689686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786c47033a0cdf1d9694e8f155195d486564713bbcc8c0afa25f10e8cc9cf5a4`  
		Last Modified: Tue, 12 Nov 2024 08:57:46 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdad625a2298295c47b0afe38537b97adfab617b746533d7813203e73ba2e6`  
		Last Modified: Tue, 12 Nov 2024 08:57:47 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1af76c98938d555bf70b17f809fc384184efd5dcb553252fa561c11cfeda0d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b774ff1a12a4ed11c894c7d291af79edf0f336d527b0b9123697b6488ef056`

```dockerfile
```

-	Layers:
	-	`sha256:2a25a9381e53150af50066c9cc8bcc9b8b94ba544f58e1ace2fc4908e90e929b`  
		Last Modified: Tue, 12 Nov 2024 08:57:46 GMT  
		Size: 18.8 KB (18763 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.5.0`

```console
$ docker pull varnish@sha256:b618e376341ca332583e924eff5f184098ff96600bfb46473ed184f8f2a61cdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:7.5.0` - linux; amd64

```console
$ docker pull varnish@sha256:94a0b719b3e2640ded1e17857eb2f17dd52f981f9f438b072e739932b5f3d910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134853200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bee4e830916f6bf61c542a6ca360e4e739860721e8fe4dc0ae3f59d744ce059`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488cc84bf670e30574b1befbf0cd6925eb970dc7edb66339d5cd3b1bb30e4191`  
		Last Modified: Tue, 12 Nov 2024 02:14:01 GMT  
		Size: 105.7 MB (105723175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90d869b88149c7e067a143b4ba1e6c7fd811b4de90818e14cbe2b4c98f08b0`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f43dddd82b1799b259a52d84c8f97886ac435347592ea3d16620fc053e5ba2f`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0` - unknown; unknown

```console
$ docker pull varnish@sha256:2c212cc3ee562ed0bc28a0fd59af348f37ceb4bcc9d597f6cecc236f926abaa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3ecccd4f353937ea748cb36599c9262502f8672808315c03cb94b5e51f2c12`

```dockerfile
```

-	Layers:
	-	`sha256:693b458079835e525c2325e20fa5a2f63e1fad9ef98cac1da5bb0d217f5f84b1`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull varnish@sha256:313a647516a8b72bfab18b3d90290d52ddb51fae4f7011d88f6f61d525ff90d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129354645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2283dd3e564e52b6a551dcc405668a0de000267f5b05b64bc994addea1db1670`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485c9bf90a9b47fc9e115175e1438347317130056edda023687e2b8d1964e297`  
		Last Modified: Tue, 12 Nov 2024 10:53:15 GMT  
		Size: 100.2 MB (100195258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc95d7d18e652867e79c05434cec6f760630bc2e49896fd7dc49fb554e94ed9b`  
		Last Modified: Tue, 12 Nov 2024 10:53:11 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5923fb57e575a592fabbcec9b22a65e1d89d705b55cc286efe87b51d774041`  
		Last Modified: Tue, 12 Nov 2024 10:53:11 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0` - unknown; unknown

```console
$ docker pull varnish@sha256:bacc180149f2fa20e1b9a5c1c59ea3c163d571fbe3ea7a5e05126449d18946ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d7564445cba3ec00c65d853472ed00f181fd1fb723b4811bd561b8f15db5d3`

```dockerfile
```

-	Layers:
	-	`sha256:52679d071576580797ce9d04ef9250cf0cb9d5cf7c6949945788560c45839d52`  
		Last Modified: Tue, 12 Nov 2024 10:53:11 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0` - linux; 386

```console
$ docker pull varnish@sha256:305c470aa3ded14f764b1f41124b7671c2a6b6da6212e89691e475162e8014df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132015848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9e56880094fdd51985109b9cd6c3ca4c284b00969afc88c4ee475b9782b8ca`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd48256999b923e6a5a6939529b9e97e128448e2dc38e5a98226f9c2483b75e7`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 101.9 MB (101868368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178779e0dd46b7438ebf7a2a171ac4a6135b19b9314e50165261851c781b86e6`  
		Last Modified: Tue, 12 Nov 2024 02:14:00 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58aa1c556f9dbfcead83df9fc499ea78d38c9f4274c6506634659101326a3f4`  
		Last Modified: Tue, 12 Nov 2024 02:14:00 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0` - unknown; unknown

```console
$ docker pull varnish@sha256:5a00c08c0e1059006be591813c815e366c428d89439dee428a0074898963ba22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03398597f16554f1cbb20fd418f774939e22db27ebdb04a27d06a0da7686fc5`

```dockerfile
```

-	Layers:
	-	`sha256:7d42e31fc94550053d0e1d64ae23d11da1fbc085f594d5aaae87d550fdabcd40`  
		Last Modified: Tue, 12 Nov 2024 02:14:00 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:9c5f38d08cf8ac979b28e55d30ba193bef196ae74854cee656900e23092ad734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137788869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed05ddb045976c21f3f59d42db251caec405e05430317746cc5f7ab035461d8c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b21e9096689a76a0e0cb9bf72040ecc6624d1be69a2e1f21a723b52aafb3c`  
		Last Modified: Tue, 12 Nov 2024 08:22:19 GMT  
		Size: 104.7 MB (104661479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4794496f5b55b28c84ebc111fa82dd0b6040610392d9d8a226e714ebc204b503`  
		Last Modified: Tue, 12 Nov 2024 08:22:13 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6698a62de09bc055930556e9fe57e1e2ea0c75f24acf1f6d23d0a931d624feec`  
		Last Modified: Tue, 12 Nov 2024 08:22:13 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0` - unknown; unknown

```console
$ docker pull varnish@sha256:882d801335d297cc2fd2e4ab00849288f38d77e10dfcf86bac6b68227d74ec58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c975b09bc154554c02eb9a2caf76ce99f37751cc7f363a71d364118967352e`

```dockerfile
```

-	Layers:
	-	`sha256:4ec8b5f662b837363dc4c989f263629678518e880b93b31b44247116a72be65e`  
		Last Modified: Tue, 12 Nov 2024 08:22:13 GMT  
		Size: 18.8 KB (18842 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0` - linux; s390x

```console
$ docker pull varnish@sha256:96948e4610b7964e6db67d68abff531467e77c7260448407cb130ba0580691f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112446573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b59f5979e8749072f59210d597a4eaaa302260573c664f2133bcf3ddb4943a7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64e58c8b20bf75539cf7f1f804b16e5553bb1c7bdf0b7b89b4ae337fa8e81b2`  
		Last Modified: Tue, 12 Nov 2024 08:55:42 GMT  
		Size: 85.0 MB (84952911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92103b008c483694642898d758639f8d7c3484eaa82959196c0f41769a3f939d`  
		Last Modified: Tue, 12 Nov 2024 08:55:41 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3ba0561e0f89a79cb397c6c11d6bf6b7d38bcb8ddbda0a8b922b45eb0c6db9`  
		Last Modified: Tue, 12 Nov 2024 08:55:41 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0` - unknown; unknown

```console
$ docker pull varnish@sha256:a2421848df597788940a00db58ec724a441bb8f655476fcd2fed5782c9d3e08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592e17482e7b45896b113979ae7a19c16397c4189c963dd152f8104a69efbf6d`

```dockerfile
```

-	Layers:
	-	`sha256:d3e19ea591bf8e2bee1dd63307d753e1a376b06dc60326880e6833a9ef5772e7`  
		Last Modified: Tue, 12 Nov 2024 08:55:41 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.5.0-alpine`

```console
$ docker pull varnish@sha256:bdb2d25c2abc7a40dab307580ec6b224bc583159d5e1c958e6490d645e6b5889
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:7.5.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:b88e87349ef0526e4c3c9ca342419cad272ae9d859e191dbc6b905f75d8f584b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75295019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b575452f4dbc566faa94f864acfbdb179386c138abe40cc9915e09ecff1571`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372b7c820710eb59ac6294c8d1bf020b6054fff084972627d39ea76fc7cc730a`  
		Last Modified: Tue, 12 Nov 2024 02:13:00 GMT  
		Size: 71.9 MB (71873252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f479569ba4eee3fba63e1c3f816b50bdcf4f066744c4bd0097f88f53af4839f`  
		Last Modified: Tue, 12 Nov 2024 02:12:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf86448644c977c6a76b0ce5d7e4af967be1b6f53d2232f3c6c9be422e44865e`  
		Last Modified: Tue, 12 Nov 2024 02:12:59 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:94c867e59bc863b7f4fe4ff0b6fbfd7f57f18f0dc0e76b1b75cba108e6e77bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cf59ab507654bbc1044a931afb77617ce5c4b390f3584352628aa914c73b65`

```dockerfile
```

-	Layers:
	-	`sha256:cde3780c4fc1a186faded0b7a02c286b675dbc292b491df0987c0beaf043856f`  
		Last Modified: Tue, 12 Nov 2024 02:12:59 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:253674c883bcfcb4a1f31b239f2c24e7a04db73e6ed93cc65b51e0e26ebecf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59056711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2506cc77824d3689ac65e41e67258e793a249356d53b88cd01aa72a862ac6a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bd5cb802d85c2e91c74445d25463939b0907216488f4851e74e1c702dd991c`  
		Last Modified: Tue, 12 Nov 2024 15:54:26 GMT  
		Size: 56.1 MB (56126931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc1f70712333298b8460020efce137c9f3b37524c3d35457bfd4fbc274271ee`  
		Last Modified: Tue, 12 Nov 2024 15:54:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a637ef13df496373fe769d481b8fcdd358d0a2e8ed259a99a4da9b1a2cc3924a`  
		Last Modified: Tue, 12 Nov 2024 15:54:27 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:828f64dde270181077e8075a682091daf054af6d99b5d8abb0f534ab786b8401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee28dbe0715d58aba783abbbaa9241295728ee4481c563be8b363b906d6955a1`

```dockerfile
```

-	Layers:
	-	`sha256:927ee010c38ad7110b9c618472cbeb1ad23ca2d5510355b0fa703fb599b507ba`  
		Last Modified: Tue, 12 Nov 2024 15:54:24 GMT  
		Size: 18.8 KB (18830 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5b124902dd89c2420a1f911a752f430bf19313e3e18b815792c9758e39c26dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71884849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f379f32b28042de5e48af9c14a5a06d9ce38ed3af4b23f94d8f937d2d3bd101`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eeda6add61cff16b44d1a88d6ed0c519389906f9aa494add7a583a0a6dfbbd`  
		Last Modified: Tue, 12 Nov 2024 10:54:53 GMT  
		Size: 68.5 MB (68523556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dda850377a6ad5f54f6035bac4db6f6bd8457d78e8a65a0af2185cd2181c24`  
		Last Modified: Tue, 12 Nov 2024 10:54:51 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd69887e6e4a1fb9b8e4d849cfbf3f5ca49775c6ee373d04d42434dcc3f898c0`  
		Last Modified: Tue, 12 Nov 2024 10:54:51 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:987df32dfad2fbf229c6e462eca7c3b87207ea40f6ac4613d82471057ea69410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6146b5011321b518fe02b97459fd0768023d3bea266e5bdfd7a3a30c1ee6e6`

```dockerfile
```

-	Layers:
	-	`sha256:d3e0430312d540571589e2c3394223aca871baa1d24f9bdebc3ef643308cceb7`  
		Last Modified: Tue, 12 Nov 2024 10:54:51 GMT  
		Size: 18.9 KB (18855 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:74b46799a1437550ecef5b61ac7e66d95ad6d44ba748ae38e5e6d09d21e5ea66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77144543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fa6b8af0ddb441fd25f4feb96591eca4237743aa6e2fc85f583bbc7d0ca724`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707f4676f8155f7af3467c0ac98ee79aa94abe48a3b20ee8c46a3e336b2f7dc`  
		Last Modified: Tue, 12 Nov 2024 02:13:11 GMT  
		Size: 73.9 MB (73888830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c01057ef20a199981392af38cb8ee25e15a9771d7e894f32e37d96856307e8`  
		Last Modified: Tue, 12 Nov 2024 02:13:09 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefde6ea9150f15fb457283144cb065f9c8e206794272d30d384716e897f5fdb`  
		Last Modified: Tue, 12 Nov 2024 02:13:09 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7b046a42b16fce1c6d97d986c9dc237689af1e23622eabfaf3ce45adee7a8636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c364eb2440d15f91c64952e3c8d3ae4e91345d8395081575484fc04066d9fb6`

```dockerfile
```

-	Layers:
	-	`sha256:0f7d8e747f6a04af94ffac3d2651bb786d0d5bc9601daa00cf3eedfbb2b73b89`  
		Last Modified: Tue, 12 Nov 2024 02:13:09 GMT  
		Size: 18.7 KB (18736 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:203426874009453571dbb4535c51e3660ca6c859fbc3322ff583f182a1d503ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72670810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdb5a0b7df6474ab21cc21174102ba749618a7934fd570a897a7d2928a30bf5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315d3daa8ba656231edb65340bf5373311e6520a6a4a77a7ddc98874600de571`  
		Last Modified: Tue, 12 Nov 2024 08:24:18 GMT  
		Size: 69.3 MB (69304263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b6a331cdc0580cd1d9b409a087fb509dd222f62e74498a640741da87752ce1`  
		Last Modified: Tue, 12 Nov 2024 08:24:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4129387d9100b5a099dd0e287fa8e518cea2fd43d789ebd3592ccfe8fd760d8e`  
		Last Modified: Tue, 12 Nov 2024 08:24:15 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6e0fc6f1ead4f281d104c2c6538fa43e0b68090c75ea989df8e94fd823ce9c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4516fb439c1e017c3367b1e817e3bac65c4adb1c0fb759dc647266a5439b5a`

```dockerfile
```

-	Layers:
	-	`sha256:0353503967374c9544a14d9477dd93cca528fc16bc6133418ce8b7d1d281337a`  
		Last Modified: Tue, 12 Nov 2024 08:24:14 GMT  
		Size: 18.8 KB (18800 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:280431fdc972bb57d70db6aba3fd865af9eeb3b2b539f279dd52ec5d5f22d65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66945128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191829c29028766d13169c317eb8dfdd60607e5c2c9a7b4378fe840ec2a796ee`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227ed073ea3a72fe745d5cf9086d188c5621272441c473087c9551d8fe016845`  
		Last Modified: Tue, 12 Nov 2024 08:57:47 GMT  
		Size: 63.7 MB (63689686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786c47033a0cdf1d9694e8f155195d486564713bbcc8c0afa25f10e8cc9cf5a4`  
		Last Modified: Tue, 12 Nov 2024 08:57:46 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdad625a2298295c47b0afe38537b97adfab617b746533d7813203e73ba2e6`  
		Last Modified: Tue, 12 Nov 2024 08:57:47 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1af76c98938d555bf70b17f809fc384184efd5dcb553252fa561c11cfeda0d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b774ff1a12a4ed11c894c7d291af79edf0f336d527b0b9123697b6488ef056`

```dockerfile
```

-	Layers:
	-	`sha256:2a25a9381e53150af50066c9cc8bcc9b8b94ba544f58e1ace2fc4908e90e929b`  
		Last Modified: Tue, 12 Nov 2024 08:57:46 GMT  
		Size: 18.8 KB (18763 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6`

```console
$ docker pull varnish@sha256:a14caeb57b4a1bda2acf8f9a0bfc558fb79419442a7038912f4a3992a86e7dc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:7.6` - linux; amd64

```console
$ docker pull varnish@sha256:f1887f671936054ffce40ee4f1ac606ccfe72ecbf54a6df79dc67e79a354f083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135144957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64030ab17f3104027d4aa981b245b5f353a3ef1a583bc622c8692aaf1bd3e5c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfd8cf94806044561883a9b5e76fea7ce7f77eff1edabe59cf2b4c4be452e12`  
		Last Modified: Tue, 12 Nov 2024 02:39:42 GMT  
		Size: 106.0 MB (106014934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ad340d8a4ae656651b563ccfa5217f12af81402ffc836c45aa31b5c65fde80`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddf610da1690ccf8889523e73d47d0e9d513e38cab68ba61160a2ac0a0f9c9e`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:1e89d4fa68525c8529220acffdf647ea246726bd6ab37aa35e9221e2cdcaa839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d3220eb09a3ea207fb331d02b0a146de411da4d4d4a2ee2e994ffccba95ca2`

```dockerfile
```

-	Layers:
	-	`sha256:c56a34258477eb10afb018c472f107873dd63f5ac6404a6eceb28339f491002f`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm variant v7

```console
$ docker pull varnish@sha256:86839bcd6e0cb7c700da3519e17ffa2de352aba06bb5c800cc923956ae2155fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105377035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a5ae730f63fecba7088a0a43a511aacc9d2b481976f45d08cb4274b73f37da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193b251ba0c785db1ddd647e543f7c3014c8a390a2c0a0002206a09d3e39db63`  
		Last Modified: Tue, 12 Nov 2024 15:43:35 GMT  
		Size: 80.7 MB (80656091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f9fd31cb20911ab9074104705f66cae11f91abc0ba6e6003e66ebeef3121e`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621b5dd00fdfdf04c730b796619283911b601d05f42dda275cb82c533dbee4ea`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:25134a573879bc47cf07d340ee755a9380912635d223f1f96cf3946bc998aa51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34405eb30257c2b0c3d220cf008a1a0a41bd82c775a45fee629140dfbffed7fe`

```dockerfile
```

-	Layers:
	-	`sha256:27292e6fd0b558edfdc2d5d8bfead9952722be4febd38d8e07a418b13092fcde`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:697f309f869dcac35ca2c1a8f8a5a0ac652952f4d5a8a1978767bb93617e8fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129638012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ed58a228f0ecd362459fe6be914ab772698b564728270e7363b04da0fe7599`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63d53be09f2e6b77c6452a52054f0b72a7331c67a1142f5f8fe9283991c05c6`  
		Last Modified: Tue, 12 Nov 2024 10:48:44 GMT  
		Size: 100.5 MB (100478623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa1a8b658b784f659f7efda570d5ffcae601bba8a690796a4ae81f5c5277550`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b6ef671bd477fe8f63b7abc44109c2636f8224108541581fdd551fb054ec93`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:1180878f25f57d8761c3fc436a7e25bb7e07343653858b63050fa88952385c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74eafa66c1381bdd46acba9d12438322a74d4e4e5f238f55dedbbda860873f61`

```dockerfile
```

-	Layers:
	-	`sha256:4d08c542d5b23e3e68d57899cb694f5cd7d7454acad345198fc173638a179a78`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; 386

```console
$ docker pull varnish@sha256:f6570237cf1c53b7fc9798f7d7d180fd85a810ec7508ddf678be907805478477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132279504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76828b8ec4ffe1c00bbb572cc26baf17fbba83775e2e3d304b682a579746b6b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c93e3e24b17f6f4677565573caa7c1fcb50037a15b0c78f697c14fec1bfe7f8`  
		Last Modified: Tue, 12 Nov 2024 03:08:20 GMT  
		Size: 102.1 MB (102132018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc93bf5d627266a3e6baee1921524e02dc602ba00b654a6b1c4acec1bfcbeae`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba71f3fb3528c4a90663ba66aa7ce5407d2acd9714e370fd3fbcd9eb7cf5526`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:24b3be81ddf3e057596748db5e20253c7f6c6d297be3700ed517574ee8b3ef10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec81166fd8290376a1f9ed06ddfd54d839dfff16886844dc3053955bb53631f9`

```dockerfile
```

-	Layers:
	-	`sha256:422ba87ca39da1f044b674ae8bc931cc96ba1729b26fee285d45c5071094d056`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; ppc64le

```console
$ docker pull varnish@sha256:23fa67728036d3fa71b0e8d14ecbcc0790ff417cdea386bc0f1f59ea08c54fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138071252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dc50f91816e6b79c2e34d97563e7192ae06ab99f6449de29c2a103f692fbdb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b40b8ec21666519f6048e9809c98d76cdb14cdd1f714124c728cdcde74b201`  
		Last Modified: Tue, 12 Nov 2024 08:16:03 GMT  
		Size: 104.9 MB (104943862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db6d1a8e68ac2829ce68950198a4a5d6bd31792b8f74a392f2a9ca2d0aed14`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb4cbd2942a8262cd4df9b8ff386bbea378dc638bc71d5add84a5825e1375aa`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:71547c8f59c36f7246f88890ac942f133fa911de88c5991e17bcbaf74c65f447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c1f525f9a4ffae1ed0e97818cd93877bad42950f6f42ec26828e94c4a3de20`

```dockerfile
```

-	Layers:
	-	`sha256:0788868b60f7f88bca46fb03d6186b3e94938faefe4fa9d7aa928e4d6c14e177`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; s390x

```console
$ docker pull varnish@sha256:01db2624b5765bf290eed9a2e85931a64f88b7036e7d5c0ae1794097e04cf6e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112730439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36f7f17ec67918459d161c53fcb045125407b045e4df3b449f5903053bde8f2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73895e6530429bd612b9331487ed4811ebd13bf2ac83e86bbb9420ea2779b2bc`  
		Last Modified: Tue, 12 Nov 2024 08:50:39 GMT  
		Size: 85.2 MB (85236779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8731a2370a6a81543907fc7a5ca55c7f89742f1f15ab0d4a6a79017a7c0fc7ab`  
		Last Modified: Tue, 12 Nov 2024 08:50:36 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a191d99ce02a230e9d85421b014d896f26f71503736d3696b654198161bc76`  
		Last Modified: Tue, 12 Nov 2024 08:50:37 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:673ebf6cf0d2a68417555ac882a255175d54bd39747b74c26845c61bd24b04e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe4d455733fd153e0ae17465ac077e05d2343f6531863707618d5063d219ee1`

```dockerfile
```

-	Layers:
	-	`sha256:cf0b77ed9acc0c7df48fbe09538ae5cd332afd2c72a896e0e64419dc124c6553`  
		Last Modified: Tue, 12 Nov 2024 08:50:36 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6-alpine`

```console
$ docker pull varnish@sha256:71e03ca9c56aa1c1bf8312c11de8ff96c71e0ba8151da2bb311d513a287851bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:7.6-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:734526105e8a73deb29880a30a8ea3ca5a3f6551a2414fb7582126729db82fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75571429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99261e656ffaef89212c06879d8ffd0a2e0a77d3ee3bb46db6ccdb837960f998`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd18d066a2534bb937baae7f43312291bbdebd9e011aa1ca8442a80cb92179`  
		Last Modified: Tue, 12 Nov 2024 02:12:46 GMT  
		Size: 72.1 MB (72149654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b86ea8455fa80ea9c4e840d50734b01b252918032889c7042ff356ac7434a4`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a657ebdd24aea07615cdedf01b64f6e9c56acd221fa99b40c2e04d31eef981c`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:09c5155bd3580c828b54df0e97c73b53d8fdee486fcdf381f0c3c7ab27a4cb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f4de71a1473c6399fc2712271473cd4ccc34f960af41104794679eee8039f`

```dockerfile
```

-	Layers:
	-	`sha256:bac5652b26b6dd3c851c3458214dc4900d0788677478ec151df55d1f34804847`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:136fc141010dc51574484fcbba9ba988f57ea942ac08e0b9423a53e0b2f48a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59334501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b477aac65d60d05a3fcfa069d583ebd04517928f689c8caaa6bf1390f527ea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4146cd2e9bfe30e036ca44a694b114955cfa0d81d82b09f55f4becff13b1ced`  
		Last Modified: Tue, 12 Nov 2024 15:46:43 GMT  
		Size: 56.4 MB (56404722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a695ae119c7fb8c829151e7070c08b103efb05d8e758e7ae88d85fcaeff28c9`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c2e597896bc956b9429c75733917197a7dc70c9b343cad765cdaa7d722eead`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3b12a943b27aff108b8b9aad7e5bb0a5e8e8f27ccb049880a9dc4efb826dd009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b5d647207732a2c16e9e4af34889f07142c3e63378fd5ff475fb2ee90f44cf`

```dockerfile
```

-	Layers:
	-	`sha256:62d334d70e119e6128bc8006bede7b71dcc6a6b8dee06e4ad4ba3f50c496e5d0`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8e0eb93f8254b9caba56523d3363579157f0c8d3ec0a532ef9bf0f6a5ecd5b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72167567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0180a70e03f8f4aa857407e74647e7b95891b4bf4718d3bd13c2739408e48b0f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6b16e5a695b41f99394c63ac1f5280714ebe2fc04c8ab237f0ce944ae25a7b`  
		Last Modified: Tue, 12 Nov 2024 10:50:26 GMT  
		Size: 68.8 MB (68806274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b67a81cdfc65d279272138408dc2d97d0e7e6f9a1703d87ed74465afe07984`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1856d82587e0084100ea903b22480aa95ceb784f24211cc088ad962b7df4e2`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ec593337520ff6285c6c7180e68369420252fd2a5d05d5019442e73bb9f913f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877d07d40294570104e1270b4d4d0f57160d5fd68bf2269a9dda10a73649a3f9`

```dockerfile
```

-	Layers:
	-	`sha256:5af3068eead5af5d8df11ff144a90cde56f3f8235175008ef6c6f025286b84de`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 19.5 KB (19535 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; 386

```console
$ docker pull varnish@sha256:2834fecda283594871274453290a2c32995405ffbd1cb36b0142dabd64c6aa41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77417612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ff26998f99ce36d7afba43984d1003013021469c34ca26074ea64f985e9b7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ecda4138670a3b812fc81a695fd9039c19b32ab99a3c37222f85b52edc70cb`  
		Last Modified: Tue, 12 Nov 2024 02:13:26 GMT  
		Size: 74.2 MB (74161899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b61ae47424cf9a4da181cec57432c8137ad9fc8abf98d41f809c818e68239c`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1117a17cfb8711601fc64652c8b28f375a3b0783f8cc3ed5a3d355dfc0ee46`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:69f6b1b7913a210b0e541e8bdd0262c619344601b938790e1cbf26ff3fb1cac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b41efdd0d57fb68398c5f7195f729ae351814c67f8a01f40a5f674b8701411`

```dockerfile
```

-	Layers:
	-	`sha256:aa644e18ac20df61b6830d7099aed73d20ddb776d4b1d730e8ab400b3e552afd`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:0cde0eefb059807950a94c89ba0a7317c379a106e0dd07f546c0b7d4b78c448c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72948010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cfaae595c7ec6a3695a9940c2cdfc5de397cc38a6c72e7425365ecc93aeab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ab68b2bfe89abc0133fdb51841b7558cd3586ee23c9b8955f3fa741cfa125`  
		Last Modified: Tue, 12 Nov 2024 08:18:05 GMT  
		Size: 69.6 MB (69581462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeac10562fa7c4a4cc127cdcd8b92b84cf4fe902259905e7f3b3c55619a14f6e`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f4d34a34ad043b6a110f1011b375de170526bb7041207eabe17f0fd587320f`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7ae561aa579e96a66d289967eff239cbfea935754d133129d116533f06246590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe17a004126d973197c0a63377b9daa600da2288a0005a3b8ef9df3a284169b`

```dockerfile
```

-	Layers:
	-	`sha256:74500f417505f2e44d78f9745c3f1b52078f1b5c18ba08622179bd242d83e55f`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:54286872273d28adde7fbdf72b5da06b19e8eacaa8980a0e1b6d719a48feb047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67226471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7576f7982594069fcacce46036976ebd45e0904de4ab77ec25782c98b61d5dcc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a0d631961a00f4bd5b680f2a859bc945e97a1f070cf7983e6afab3074c3bfe`  
		Last Modified: Tue, 12 Nov 2024 08:52:38 GMT  
		Size: 64.0 MB (63971024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4295a934b4400d12d8b9a5d67da1f597255b186adf7fc450f7bd5a2219fadae`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb2d2197875fd4fe8653ace14c11f094ffddfcefb5050905a4ff4b479760a9`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7ca01929086339d2a32f9a35f37fa1e13cd46b0888aaf17861704c93fd883c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c6930c96e9c224ba90924e21554d5c392ac55e9e4dd1126debbf8c30d6dcbb`

```dockerfile
```

-	Layers:
	-	`sha256:242e0ff3285bb7cf08ea74daf6e7f22b247a2d5f070962ca2388c042539258ac`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.1`

```console
$ docker pull varnish@sha256:a14caeb57b4a1bda2acf8f9a0bfc558fb79419442a7038912f4a3992a86e7dc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:7.6.1` - linux; amd64

```console
$ docker pull varnish@sha256:f1887f671936054ffce40ee4f1ac606ccfe72ecbf54a6df79dc67e79a354f083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135144957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64030ab17f3104027d4aa981b245b5f353a3ef1a583bc622c8692aaf1bd3e5c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfd8cf94806044561883a9b5e76fea7ce7f77eff1edabe59cf2b4c4be452e12`  
		Last Modified: Tue, 12 Nov 2024 02:39:42 GMT  
		Size: 106.0 MB (106014934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ad340d8a4ae656651b563ccfa5217f12af81402ffc836c45aa31b5c65fde80`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddf610da1690ccf8889523e73d47d0e9d513e38cab68ba61160a2ac0a0f9c9e`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:1e89d4fa68525c8529220acffdf647ea246726bd6ab37aa35e9221e2cdcaa839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d3220eb09a3ea207fb331d02b0a146de411da4d4d4a2ee2e994ffccba95ca2`

```dockerfile
```

-	Layers:
	-	`sha256:c56a34258477eb10afb018c472f107873dd63f5ac6404a6eceb28339f491002f`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; arm variant v7

```console
$ docker pull varnish@sha256:86839bcd6e0cb7c700da3519e17ffa2de352aba06bb5c800cc923956ae2155fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105377035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a5ae730f63fecba7088a0a43a511aacc9d2b481976f45d08cb4274b73f37da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193b251ba0c785db1ddd647e543f7c3014c8a390a2c0a0002206a09d3e39db63`  
		Last Modified: Tue, 12 Nov 2024 15:43:35 GMT  
		Size: 80.7 MB (80656091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f9fd31cb20911ab9074104705f66cae11f91abc0ba6e6003e66ebeef3121e`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621b5dd00fdfdf04c730b796619283911b601d05f42dda275cb82c533dbee4ea`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:25134a573879bc47cf07d340ee755a9380912635d223f1f96cf3946bc998aa51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34405eb30257c2b0c3d220cf008a1a0a41bd82c775a45fee629140dfbffed7fe`

```dockerfile
```

-	Layers:
	-	`sha256:27292e6fd0b558edfdc2d5d8bfead9952722be4febd38d8e07a418b13092fcde`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:697f309f869dcac35ca2c1a8f8a5a0ac652952f4d5a8a1978767bb93617e8fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129638012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ed58a228f0ecd362459fe6be914ab772698b564728270e7363b04da0fe7599`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63d53be09f2e6b77c6452a52054f0b72a7331c67a1142f5f8fe9283991c05c6`  
		Last Modified: Tue, 12 Nov 2024 10:48:44 GMT  
		Size: 100.5 MB (100478623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa1a8b658b784f659f7efda570d5ffcae601bba8a690796a4ae81f5c5277550`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b6ef671bd477fe8f63b7abc44109c2636f8224108541581fdd551fb054ec93`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:1180878f25f57d8761c3fc436a7e25bb7e07343653858b63050fa88952385c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74eafa66c1381bdd46acba9d12438322a74d4e4e5f238f55dedbbda860873f61`

```dockerfile
```

-	Layers:
	-	`sha256:4d08c542d5b23e3e68d57899cb694f5cd7d7454acad345198fc173638a179a78`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; 386

```console
$ docker pull varnish@sha256:f6570237cf1c53b7fc9798f7d7d180fd85a810ec7508ddf678be907805478477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132279504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76828b8ec4ffe1c00bbb572cc26baf17fbba83775e2e3d304b682a579746b6b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c93e3e24b17f6f4677565573caa7c1fcb50037a15b0c78f697c14fec1bfe7f8`  
		Last Modified: Tue, 12 Nov 2024 03:08:20 GMT  
		Size: 102.1 MB (102132018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc93bf5d627266a3e6baee1921524e02dc602ba00b654a6b1c4acec1bfcbeae`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba71f3fb3528c4a90663ba66aa7ce5407d2acd9714e370fd3fbcd9eb7cf5526`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:24b3be81ddf3e057596748db5e20253c7f6c6d297be3700ed517574ee8b3ef10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec81166fd8290376a1f9ed06ddfd54d839dfff16886844dc3053955bb53631f9`

```dockerfile
```

-	Layers:
	-	`sha256:422ba87ca39da1f044b674ae8bc931cc96ba1729b26fee285d45c5071094d056`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; ppc64le

```console
$ docker pull varnish@sha256:23fa67728036d3fa71b0e8d14ecbcc0790ff417cdea386bc0f1f59ea08c54fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138071252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dc50f91816e6b79c2e34d97563e7192ae06ab99f6449de29c2a103f692fbdb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b40b8ec21666519f6048e9809c98d76cdb14cdd1f714124c728cdcde74b201`  
		Last Modified: Tue, 12 Nov 2024 08:16:03 GMT  
		Size: 104.9 MB (104943862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db6d1a8e68ac2829ce68950198a4a5d6bd31792b8f74a392f2a9ca2d0aed14`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb4cbd2942a8262cd4df9b8ff386bbea378dc638bc71d5add84a5825e1375aa`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:71547c8f59c36f7246f88890ac942f133fa911de88c5991e17bcbaf74c65f447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c1f525f9a4ffae1ed0e97818cd93877bad42950f6f42ec26828e94c4a3de20`

```dockerfile
```

-	Layers:
	-	`sha256:0788868b60f7f88bca46fb03d6186b3e94938faefe4fa9d7aa928e4d6c14e177`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; s390x

```console
$ docker pull varnish@sha256:01db2624b5765bf290eed9a2e85931a64f88b7036e7d5c0ae1794097e04cf6e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112730439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36f7f17ec67918459d161c53fcb045125407b045e4df3b449f5903053bde8f2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73895e6530429bd612b9331487ed4811ebd13bf2ac83e86bbb9420ea2779b2bc`  
		Last Modified: Tue, 12 Nov 2024 08:50:39 GMT  
		Size: 85.2 MB (85236779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8731a2370a6a81543907fc7a5ca55c7f89742f1f15ab0d4a6a79017a7c0fc7ab`  
		Last Modified: Tue, 12 Nov 2024 08:50:36 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a191d99ce02a230e9d85421b014d896f26f71503736d3696b654198161bc76`  
		Last Modified: Tue, 12 Nov 2024 08:50:37 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:673ebf6cf0d2a68417555ac882a255175d54bd39747b74c26845c61bd24b04e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe4d455733fd153e0ae17465ac077e05d2343f6531863707618d5063d219ee1`

```dockerfile
```

-	Layers:
	-	`sha256:cf0b77ed9acc0c7df48fbe09538ae5cd332afd2c72a896e0e64419dc124c6553`  
		Last Modified: Tue, 12 Nov 2024 08:50:36 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.1-alpine`

```console
$ docker pull varnish@sha256:71e03ca9c56aa1c1bf8312c11de8ff96c71e0ba8151da2bb311d513a287851bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:7.6.1-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:734526105e8a73deb29880a30a8ea3ca5a3f6551a2414fb7582126729db82fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75571429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99261e656ffaef89212c06879d8ffd0a2e0a77d3ee3bb46db6ccdb837960f998`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd18d066a2534bb937baae7f43312291bbdebd9e011aa1ca8442a80cb92179`  
		Last Modified: Tue, 12 Nov 2024 02:12:46 GMT  
		Size: 72.1 MB (72149654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b86ea8455fa80ea9c4e840d50734b01b252918032889c7042ff356ac7434a4`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a657ebdd24aea07615cdedf01b64f6e9c56acd221fa99b40c2e04d31eef981c`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:09c5155bd3580c828b54df0e97c73b53d8fdee486fcdf381f0c3c7ab27a4cb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f4de71a1473c6399fc2712271473cd4ccc34f960af41104794679eee8039f`

```dockerfile
```

-	Layers:
	-	`sha256:bac5652b26b6dd3c851c3458214dc4900d0788677478ec151df55d1f34804847`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:136fc141010dc51574484fcbba9ba988f57ea942ac08e0b9423a53e0b2f48a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59334501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b477aac65d60d05a3fcfa069d583ebd04517928f689c8caaa6bf1390f527ea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4146cd2e9bfe30e036ca44a694b114955cfa0d81d82b09f55f4becff13b1ced`  
		Last Modified: Tue, 12 Nov 2024 15:46:43 GMT  
		Size: 56.4 MB (56404722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a695ae119c7fb8c829151e7070c08b103efb05d8e758e7ae88d85fcaeff28c9`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c2e597896bc956b9429c75733917197a7dc70c9b343cad765cdaa7d722eead`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3b12a943b27aff108b8b9aad7e5bb0a5e8e8f27ccb049880a9dc4efb826dd009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b5d647207732a2c16e9e4af34889f07142c3e63378fd5ff475fb2ee90f44cf`

```dockerfile
```

-	Layers:
	-	`sha256:62d334d70e119e6128bc8006bede7b71dcc6a6b8dee06e4ad4ba3f50c496e5d0`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8e0eb93f8254b9caba56523d3363579157f0c8d3ec0a532ef9bf0f6a5ecd5b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72167567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0180a70e03f8f4aa857407e74647e7b95891b4bf4718d3bd13c2739408e48b0f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6b16e5a695b41f99394c63ac1f5280714ebe2fc04c8ab237f0ce944ae25a7b`  
		Last Modified: Tue, 12 Nov 2024 10:50:26 GMT  
		Size: 68.8 MB (68806274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b67a81cdfc65d279272138408dc2d97d0e7e6f9a1703d87ed74465afe07984`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1856d82587e0084100ea903b22480aa95ceb784f24211cc088ad962b7df4e2`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ec593337520ff6285c6c7180e68369420252fd2a5d05d5019442e73bb9f913f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877d07d40294570104e1270b4d4d0f57160d5fd68bf2269a9dda10a73649a3f9`

```dockerfile
```

-	Layers:
	-	`sha256:5af3068eead5af5d8df11ff144a90cde56f3f8235175008ef6c6f025286b84de`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 19.5 KB (19535 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; 386

```console
$ docker pull varnish@sha256:2834fecda283594871274453290a2c32995405ffbd1cb36b0142dabd64c6aa41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77417612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ff26998f99ce36d7afba43984d1003013021469c34ca26074ea64f985e9b7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ecda4138670a3b812fc81a695fd9039c19b32ab99a3c37222f85b52edc70cb`  
		Last Modified: Tue, 12 Nov 2024 02:13:26 GMT  
		Size: 74.2 MB (74161899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b61ae47424cf9a4da181cec57432c8137ad9fc8abf98d41f809c818e68239c`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1117a17cfb8711601fc64652c8b28f375a3b0783f8cc3ed5a3d355dfc0ee46`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:69f6b1b7913a210b0e541e8bdd0262c619344601b938790e1cbf26ff3fb1cac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b41efdd0d57fb68398c5f7195f729ae351814c67f8a01f40a5f674b8701411`

```dockerfile
```

-	Layers:
	-	`sha256:aa644e18ac20df61b6830d7099aed73d20ddb776d4b1d730e8ab400b3e552afd`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:0cde0eefb059807950a94c89ba0a7317c379a106e0dd07f546c0b7d4b78c448c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72948010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cfaae595c7ec6a3695a9940c2cdfc5de397cc38a6c72e7425365ecc93aeab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ab68b2bfe89abc0133fdb51841b7558cd3586ee23c9b8955f3fa741cfa125`  
		Last Modified: Tue, 12 Nov 2024 08:18:05 GMT  
		Size: 69.6 MB (69581462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeac10562fa7c4a4cc127cdcd8b92b84cf4fe902259905e7f3b3c55619a14f6e`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f4d34a34ad043b6a110f1011b375de170526bb7041207eabe17f0fd587320f`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7ae561aa579e96a66d289967eff239cbfea935754d133129d116533f06246590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe17a004126d973197c0a63377b9daa600da2288a0005a3b8ef9df3a284169b`

```dockerfile
```

-	Layers:
	-	`sha256:74500f417505f2e44d78f9745c3f1b52078f1b5c18ba08622179bd242d83e55f`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:54286872273d28adde7fbdf72b5da06b19e8eacaa8980a0e1b6d719a48feb047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67226471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7576f7982594069fcacce46036976ebd45e0904de4ab77ec25782c98b61d5dcc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a0d631961a00f4bd5b680f2a859bc945e97a1f070cf7983e6afab3074c3bfe`  
		Last Modified: Tue, 12 Nov 2024 08:52:38 GMT  
		Size: 64.0 MB (63971024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4295a934b4400d12d8b9a5d67da1f597255b186adf7fc450f7bd5a2219fadae`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb2d2197875fd4fe8653ace14c11f094ffddfcefb5050905a4ff4b479760a9`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7ca01929086339d2a32f9a35f37fa1e13cd46b0888aaf17861704c93fd883c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c6930c96e9c224ba90924e21554d5c392ac55e9e4dd1126debbf8c30d6dcbb`

```dockerfile
```

-	Layers:
	-	`sha256:242e0ff3285bb7cf08ea74daf6e7f22b247a2d5f070962ca2388c042539258ac`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:alpine`

```console
$ docker pull varnish@sha256:71e03ca9c56aa1c1bf8312c11de8ff96c71e0ba8151da2bb311d513a287851bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:alpine` - linux; amd64

```console
$ docker pull varnish@sha256:734526105e8a73deb29880a30a8ea3ca5a3f6551a2414fb7582126729db82fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75571429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99261e656ffaef89212c06879d8ffd0a2e0a77d3ee3bb46db6ccdb837960f998`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd18d066a2534bb937baae7f43312291bbdebd9e011aa1ca8442a80cb92179`  
		Last Modified: Tue, 12 Nov 2024 02:12:46 GMT  
		Size: 72.1 MB (72149654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b86ea8455fa80ea9c4e840d50734b01b252918032889c7042ff356ac7434a4`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a657ebdd24aea07615cdedf01b64f6e9c56acd221fa99b40c2e04d31eef981c`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:09c5155bd3580c828b54df0e97c73b53d8fdee486fcdf381f0c3c7ab27a4cb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f4de71a1473c6399fc2712271473cd4ccc34f960af41104794679eee8039f`

```dockerfile
```

-	Layers:
	-	`sha256:bac5652b26b6dd3c851c3458214dc4900d0788677478ec151df55d1f34804847`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:136fc141010dc51574484fcbba9ba988f57ea942ac08e0b9423a53e0b2f48a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59334501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b477aac65d60d05a3fcfa069d583ebd04517928f689c8caaa6bf1390f527ea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4146cd2e9bfe30e036ca44a694b114955cfa0d81d82b09f55f4becff13b1ced`  
		Last Modified: Tue, 12 Nov 2024 15:46:43 GMT  
		Size: 56.4 MB (56404722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a695ae119c7fb8c829151e7070c08b103efb05d8e758e7ae88d85fcaeff28c9`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c2e597896bc956b9429c75733917197a7dc70c9b343cad765cdaa7d722eead`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3b12a943b27aff108b8b9aad7e5bb0a5e8e8f27ccb049880a9dc4efb826dd009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b5d647207732a2c16e9e4af34889f07142c3e63378fd5ff475fb2ee90f44cf`

```dockerfile
```

-	Layers:
	-	`sha256:62d334d70e119e6128bc8006bede7b71dcc6a6b8dee06e4ad4ba3f50c496e5d0`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8e0eb93f8254b9caba56523d3363579157f0c8d3ec0a532ef9bf0f6a5ecd5b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72167567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0180a70e03f8f4aa857407e74647e7b95891b4bf4718d3bd13c2739408e48b0f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6b16e5a695b41f99394c63ac1f5280714ebe2fc04c8ab237f0ce944ae25a7b`  
		Last Modified: Tue, 12 Nov 2024 10:50:26 GMT  
		Size: 68.8 MB (68806274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b67a81cdfc65d279272138408dc2d97d0e7e6f9a1703d87ed74465afe07984`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1856d82587e0084100ea903b22480aa95ceb784f24211cc088ad962b7df4e2`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ec593337520ff6285c6c7180e68369420252fd2a5d05d5019442e73bb9f913f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877d07d40294570104e1270b4d4d0f57160d5fd68bf2269a9dda10a73649a3f9`

```dockerfile
```

-	Layers:
	-	`sha256:5af3068eead5af5d8df11ff144a90cde56f3f8235175008ef6c6f025286b84de`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 19.5 KB (19535 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:2834fecda283594871274453290a2c32995405ffbd1cb36b0142dabd64c6aa41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77417612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ff26998f99ce36d7afba43984d1003013021469c34ca26074ea64f985e9b7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ecda4138670a3b812fc81a695fd9039c19b32ab99a3c37222f85b52edc70cb`  
		Last Modified: Tue, 12 Nov 2024 02:13:26 GMT  
		Size: 74.2 MB (74161899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b61ae47424cf9a4da181cec57432c8137ad9fc8abf98d41f809c818e68239c`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1117a17cfb8711601fc64652c8b28f375a3b0783f8cc3ed5a3d355dfc0ee46`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:69f6b1b7913a210b0e541e8bdd0262c619344601b938790e1cbf26ff3fb1cac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b41efdd0d57fb68398c5f7195f729ae351814c67f8a01f40a5f674b8701411`

```dockerfile
```

-	Layers:
	-	`sha256:aa644e18ac20df61b6830d7099aed73d20ddb776d4b1d730e8ab400b3e552afd`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:0cde0eefb059807950a94c89ba0a7317c379a106e0dd07f546c0b7d4b78c448c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72948010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cfaae595c7ec6a3695a9940c2cdfc5de397cc38a6c72e7425365ecc93aeab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ab68b2bfe89abc0133fdb51841b7558cd3586ee23c9b8955f3fa741cfa125`  
		Last Modified: Tue, 12 Nov 2024 08:18:05 GMT  
		Size: 69.6 MB (69581462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeac10562fa7c4a4cc127cdcd8b92b84cf4fe902259905e7f3b3c55619a14f6e`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f4d34a34ad043b6a110f1011b375de170526bb7041207eabe17f0fd587320f`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7ae561aa579e96a66d289967eff239cbfea935754d133129d116533f06246590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe17a004126d973197c0a63377b9daa600da2288a0005a3b8ef9df3a284169b`

```dockerfile
```

-	Layers:
	-	`sha256:74500f417505f2e44d78f9745c3f1b52078f1b5c18ba08622179bd242d83e55f`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:54286872273d28adde7fbdf72b5da06b19e8eacaa8980a0e1b6d719a48feb047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67226471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7576f7982594069fcacce46036976ebd45e0904de4ab77ec25782c98b61d5dcc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a0d631961a00f4bd5b680f2a859bc945e97a1f070cf7983e6afab3074c3bfe`  
		Last Modified: Tue, 12 Nov 2024 08:52:38 GMT  
		Size: 64.0 MB (63971024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4295a934b4400d12d8b9a5d67da1f597255b186adf7fc450f7bd5a2219fadae`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb2d2197875fd4fe8653ace14c11f094ffddfcefb5050905a4ff4b479760a9`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7ca01929086339d2a32f9a35f37fa1e13cd46b0888aaf17861704c93fd883c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c6930c96e9c224ba90924e21554d5c392ac55e9e4dd1126debbf8c30d6dcbb`

```dockerfile
```

-	Layers:
	-	`sha256:242e0ff3285bb7cf08ea74daf6e7f22b247a2d5f070962ca2388c042539258ac`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:a14caeb57b4a1bda2acf8f9a0bfc558fb79419442a7038912f4a3992a86e7dc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:f1887f671936054ffce40ee4f1ac606ccfe72ecbf54a6df79dc67e79a354f083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135144957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64030ab17f3104027d4aa981b245b5f353a3ef1a583bc622c8692aaf1bd3e5c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfd8cf94806044561883a9b5e76fea7ce7f77eff1edabe59cf2b4c4be452e12`  
		Last Modified: Tue, 12 Nov 2024 02:39:42 GMT  
		Size: 106.0 MB (106014934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ad340d8a4ae656651b563ccfa5217f12af81402ffc836c45aa31b5c65fde80`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddf610da1690ccf8889523e73d47d0e9d513e38cab68ba61160a2ac0a0f9c9e`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:1e89d4fa68525c8529220acffdf647ea246726bd6ab37aa35e9221e2cdcaa839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d3220eb09a3ea207fb331d02b0a146de411da4d4d4a2ee2e994ffccba95ca2`

```dockerfile
```

-	Layers:
	-	`sha256:c56a34258477eb10afb018c472f107873dd63f5ac6404a6eceb28339f491002f`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:86839bcd6e0cb7c700da3519e17ffa2de352aba06bb5c800cc923956ae2155fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105377035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a5ae730f63fecba7088a0a43a511aacc9d2b481976f45d08cb4274b73f37da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193b251ba0c785db1ddd647e543f7c3014c8a390a2c0a0002206a09d3e39db63`  
		Last Modified: Tue, 12 Nov 2024 15:43:35 GMT  
		Size: 80.7 MB (80656091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f9fd31cb20911ab9074104705f66cae11f91abc0ba6e6003e66ebeef3121e`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621b5dd00fdfdf04c730b796619283911b601d05f42dda275cb82c533dbee4ea`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:25134a573879bc47cf07d340ee755a9380912635d223f1f96cf3946bc998aa51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34405eb30257c2b0c3d220cf008a1a0a41bd82c775a45fee629140dfbffed7fe`

```dockerfile
```

-	Layers:
	-	`sha256:27292e6fd0b558edfdc2d5d8bfead9952722be4febd38d8e07a418b13092fcde`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:697f309f869dcac35ca2c1a8f8a5a0ac652952f4d5a8a1978767bb93617e8fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129638012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ed58a228f0ecd362459fe6be914ab772698b564728270e7363b04da0fe7599`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63d53be09f2e6b77c6452a52054f0b72a7331c67a1142f5f8fe9283991c05c6`  
		Last Modified: Tue, 12 Nov 2024 10:48:44 GMT  
		Size: 100.5 MB (100478623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa1a8b658b784f659f7efda570d5ffcae601bba8a690796a4ae81f5c5277550`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b6ef671bd477fe8f63b7abc44109c2636f8224108541581fdd551fb054ec93`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:1180878f25f57d8761c3fc436a7e25bb7e07343653858b63050fa88952385c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74eafa66c1381bdd46acba9d12438322a74d4e4e5f238f55dedbbda860873f61`

```dockerfile
```

-	Layers:
	-	`sha256:4d08c542d5b23e3e68d57899cb694f5cd7d7454acad345198fc173638a179a78`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:f6570237cf1c53b7fc9798f7d7d180fd85a810ec7508ddf678be907805478477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132279504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76828b8ec4ffe1c00bbb572cc26baf17fbba83775e2e3d304b682a579746b6b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c93e3e24b17f6f4677565573caa7c1fcb50037a15b0c78f697c14fec1bfe7f8`  
		Last Modified: Tue, 12 Nov 2024 03:08:20 GMT  
		Size: 102.1 MB (102132018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc93bf5d627266a3e6baee1921524e02dc602ba00b654a6b1c4acec1bfcbeae`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba71f3fb3528c4a90663ba66aa7ce5407d2acd9714e370fd3fbcd9eb7cf5526`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:24b3be81ddf3e057596748db5e20253c7f6c6d297be3700ed517574ee8b3ef10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec81166fd8290376a1f9ed06ddfd54d839dfff16886844dc3053955bb53631f9`

```dockerfile
```

-	Layers:
	-	`sha256:422ba87ca39da1f044b674ae8bc931cc96ba1729b26fee285d45c5071094d056`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:23fa67728036d3fa71b0e8d14ecbcc0790ff417cdea386bc0f1f59ea08c54fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138071252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dc50f91816e6b79c2e34d97563e7192ae06ab99f6449de29c2a103f692fbdb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b40b8ec21666519f6048e9809c98d76cdb14cdd1f714124c728cdcde74b201`  
		Last Modified: Tue, 12 Nov 2024 08:16:03 GMT  
		Size: 104.9 MB (104943862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db6d1a8e68ac2829ce68950198a4a5d6bd31792b8f74a392f2a9ca2d0aed14`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb4cbd2942a8262cd4df9b8ff386bbea378dc638bc71d5add84a5825e1375aa`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:71547c8f59c36f7246f88890ac942f133fa911de88c5991e17bcbaf74c65f447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c1f525f9a4ffae1ed0e97818cd93877bad42950f6f42ec26828e94c4a3de20`

```dockerfile
```

-	Layers:
	-	`sha256:0788868b60f7f88bca46fb03d6186b3e94938faefe4fa9d7aa928e4d6c14e177`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:01db2624b5765bf290eed9a2e85931a64f88b7036e7d5c0ae1794097e04cf6e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112730439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36f7f17ec67918459d161c53fcb045125407b045e4df3b449f5903053bde8f2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73895e6530429bd612b9331487ed4811ebd13bf2ac83e86bbb9420ea2779b2bc`  
		Last Modified: Tue, 12 Nov 2024 08:50:39 GMT  
		Size: 85.2 MB (85236779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8731a2370a6a81543907fc7a5ca55c7f89742f1f15ab0d4a6a79017a7c0fc7ab`  
		Last Modified: Tue, 12 Nov 2024 08:50:36 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a191d99ce02a230e9d85421b014d896f26f71503736d3696b654198161bc76`  
		Last Modified: Tue, 12 Nov 2024 08:50:37 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:673ebf6cf0d2a68417555ac882a255175d54bd39747b74c26845c61bd24b04e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe4d455733fd153e0ae17465ac077e05d2343f6531863707618d5063d219ee1`

```dockerfile
```

-	Layers:
	-	`sha256:cf0b77ed9acc0c7df48fbe09538ae5cd332afd2c72a896e0e64419dc124c6553`  
		Last Modified: Tue, 12 Nov 2024 08:50:36 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:71e03ca9c56aa1c1bf8312c11de8ff96c71e0ba8151da2bb311d513a287851bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:fresh-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:734526105e8a73deb29880a30a8ea3ca5a3f6551a2414fb7582126729db82fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75571429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99261e656ffaef89212c06879d8ffd0a2e0a77d3ee3bb46db6ccdb837960f998`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd18d066a2534bb937baae7f43312291bbdebd9e011aa1ca8442a80cb92179`  
		Last Modified: Tue, 12 Nov 2024 02:12:46 GMT  
		Size: 72.1 MB (72149654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b86ea8455fa80ea9c4e840d50734b01b252918032889c7042ff356ac7434a4`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a657ebdd24aea07615cdedf01b64f6e9c56acd221fa99b40c2e04d31eef981c`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:09c5155bd3580c828b54df0e97c73b53d8fdee486fcdf381f0c3c7ab27a4cb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f4de71a1473c6399fc2712271473cd4ccc34f960af41104794679eee8039f`

```dockerfile
```

-	Layers:
	-	`sha256:bac5652b26b6dd3c851c3458214dc4900d0788677478ec151df55d1f34804847`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:136fc141010dc51574484fcbba9ba988f57ea942ac08e0b9423a53e0b2f48a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59334501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b477aac65d60d05a3fcfa069d583ebd04517928f689c8caaa6bf1390f527ea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4146cd2e9bfe30e036ca44a694b114955cfa0d81d82b09f55f4becff13b1ced`  
		Last Modified: Tue, 12 Nov 2024 15:46:43 GMT  
		Size: 56.4 MB (56404722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a695ae119c7fb8c829151e7070c08b103efb05d8e758e7ae88d85fcaeff28c9`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c2e597896bc956b9429c75733917197a7dc70c9b343cad765cdaa7d722eead`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3b12a943b27aff108b8b9aad7e5bb0a5e8e8f27ccb049880a9dc4efb826dd009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b5d647207732a2c16e9e4af34889f07142c3e63378fd5ff475fb2ee90f44cf`

```dockerfile
```

-	Layers:
	-	`sha256:62d334d70e119e6128bc8006bede7b71dcc6a6b8dee06e4ad4ba3f50c496e5d0`  
		Last Modified: Tue, 12 Nov 2024 15:46:41 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8e0eb93f8254b9caba56523d3363579157f0c8d3ec0a532ef9bf0f6a5ecd5b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72167567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0180a70e03f8f4aa857407e74647e7b95891b4bf4718d3bd13c2739408e48b0f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6b16e5a695b41f99394c63ac1f5280714ebe2fc04c8ab237f0ce944ae25a7b`  
		Last Modified: Tue, 12 Nov 2024 10:50:26 GMT  
		Size: 68.8 MB (68806274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b67a81cdfc65d279272138408dc2d97d0e7e6f9a1703d87ed74465afe07984`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1856d82587e0084100ea903b22480aa95ceb784f24211cc088ad962b7df4e2`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ec593337520ff6285c6c7180e68369420252fd2a5d05d5019442e73bb9f913f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877d07d40294570104e1270b4d4d0f57160d5fd68bf2269a9dda10a73649a3f9`

```dockerfile
```

-	Layers:
	-	`sha256:5af3068eead5af5d8df11ff144a90cde56f3f8235175008ef6c6f025286b84de`  
		Last Modified: Tue, 12 Nov 2024 10:50:24 GMT  
		Size: 19.5 KB (19535 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:2834fecda283594871274453290a2c32995405ffbd1cb36b0142dabd64c6aa41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77417612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ff26998f99ce36d7afba43984d1003013021469c34ca26074ea64f985e9b7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ecda4138670a3b812fc81a695fd9039c19b32ab99a3c37222f85b52edc70cb`  
		Last Modified: Tue, 12 Nov 2024 02:13:26 GMT  
		Size: 74.2 MB (74161899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b61ae47424cf9a4da181cec57432c8137ad9fc8abf98d41f809c818e68239c`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1117a17cfb8711601fc64652c8b28f375a3b0783f8cc3ed5a3d355dfc0ee46`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:69f6b1b7913a210b0e541e8bdd0262c619344601b938790e1cbf26ff3fb1cac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b41efdd0d57fb68398c5f7195f729ae351814c67f8a01f40a5f674b8701411`

```dockerfile
```

-	Layers:
	-	`sha256:aa644e18ac20df61b6830d7099aed73d20ddb776d4b1d730e8ab400b3e552afd`  
		Last Modified: Tue, 12 Nov 2024 02:13:23 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:0cde0eefb059807950a94c89ba0a7317c379a106e0dd07f546c0b7d4b78c448c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72948010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cfaae595c7ec6a3695a9940c2cdfc5de397cc38a6c72e7425365ecc93aeab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ab68b2bfe89abc0133fdb51841b7558cd3586ee23c9b8955f3fa741cfa125`  
		Last Modified: Tue, 12 Nov 2024 08:18:05 GMT  
		Size: 69.6 MB (69581462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeac10562fa7c4a4cc127cdcd8b92b84cf4fe902259905e7f3b3c55619a14f6e`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f4d34a34ad043b6a110f1011b375de170526bb7041207eabe17f0fd587320f`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7ae561aa579e96a66d289967eff239cbfea935754d133129d116533f06246590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe17a004126d973197c0a63377b9daa600da2288a0005a3b8ef9df3a284169b`

```dockerfile
```

-	Layers:
	-	`sha256:74500f417505f2e44d78f9745c3f1b52078f1b5c18ba08622179bd242d83e55f`  
		Last Modified: Tue, 12 Nov 2024 08:18:02 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:54286872273d28adde7fbdf72b5da06b19e8eacaa8980a0e1b6d719a48feb047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67226471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7576f7982594069fcacce46036976ebd45e0904de4ab77ec25782c98b61d5dcc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a0d631961a00f4bd5b680f2a859bc945e97a1f070cf7983e6afab3074c3bfe`  
		Last Modified: Tue, 12 Nov 2024 08:52:38 GMT  
		Size: 64.0 MB (63971024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4295a934b4400d12d8b9a5d67da1f597255b186adf7fc450f7bd5a2219fadae`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb2d2197875fd4fe8653ace14c11f094ffddfcefb5050905a4ff4b479760a9`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7ca01929086339d2a32f9a35f37fa1e13cd46b0888aaf17861704c93fd883c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c6930c96e9c224ba90924e21554d5c392ac55e9e4dd1126debbf8c30d6dcbb`

```dockerfile
```

-	Layers:
	-	`sha256:242e0ff3285bb7cf08ea74daf6e7f22b247a2d5f070962ca2388c042539258ac`  
		Last Modified: Tue, 12 Nov 2024 08:52:37 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:a14caeb57b4a1bda2acf8f9a0bfc558fb79419442a7038912f4a3992a86e7dc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:f1887f671936054ffce40ee4f1ac606ccfe72ecbf54a6df79dc67e79a354f083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135144957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64030ab17f3104027d4aa981b245b5f353a3ef1a583bc622c8692aaf1bd3e5c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfd8cf94806044561883a9b5e76fea7ce7f77eff1edabe59cf2b4c4be452e12`  
		Last Modified: Tue, 12 Nov 2024 02:39:42 GMT  
		Size: 106.0 MB (106014934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ad340d8a4ae656651b563ccfa5217f12af81402ffc836c45aa31b5c65fde80`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddf610da1690ccf8889523e73d47d0e9d513e38cab68ba61160a2ac0a0f9c9e`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:1e89d4fa68525c8529220acffdf647ea246726bd6ab37aa35e9221e2cdcaa839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d3220eb09a3ea207fb331d02b0a146de411da4d4d4a2ee2e994ffccba95ca2`

```dockerfile
```

-	Layers:
	-	`sha256:c56a34258477eb10afb018c472f107873dd63f5ac6404a6eceb28339f491002f`  
		Last Modified: Tue, 12 Nov 2024 02:39:40 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:86839bcd6e0cb7c700da3519e17ffa2de352aba06bb5c800cc923956ae2155fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105377035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a5ae730f63fecba7088a0a43a511aacc9d2b481976f45d08cb4274b73f37da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193b251ba0c785db1ddd647e543f7c3014c8a390a2c0a0002206a09d3e39db63`  
		Last Modified: Tue, 12 Nov 2024 15:43:35 GMT  
		Size: 80.7 MB (80656091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f9fd31cb20911ab9074104705f66cae11f91abc0ba6e6003e66ebeef3121e`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621b5dd00fdfdf04c730b796619283911b601d05f42dda275cb82c533dbee4ea`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:25134a573879bc47cf07d340ee755a9380912635d223f1f96cf3946bc998aa51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34405eb30257c2b0c3d220cf008a1a0a41bd82c775a45fee629140dfbffed7fe`

```dockerfile
```

-	Layers:
	-	`sha256:27292e6fd0b558edfdc2d5d8bfead9952722be4febd38d8e07a418b13092fcde`  
		Last Modified: Tue, 12 Nov 2024 15:43:32 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:697f309f869dcac35ca2c1a8f8a5a0ac652952f4d5a8a1978767bb93617e8fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129638012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ed58a228f0ecd362459fe6be914ab772698b564728270e7363b04da0fe7599`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63d53be09f2e6b77c6452a52054f0b72a7331c67a1142f5f8fe9283991c05c6`  
		Last Modified: Tue, 12 Nov 2024 10:48:44 GMT  
		Size: 100.5 MB (100478623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa1a8b658b784f659f7efda570d5ffcae601bba8a690796a4ae81f5c5277550`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b6ef671bd477fe8f63b7abc44109c2636f8224108541581fdd551fb054ec93`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:1180878f25f57d8761c3fc436a7e25bb7e07343653858b63050fa88952385c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74eafa66c1381bdd46acba9d12438322a74d4e4e5f238f55dedbbda860873f61`

```dockerfile
```

-	Layers:
	-	`sha256:4d08c542d5b23e3e68d57899cb694f5cd7d7454acad345198fc173638a179a78`  
		Last Modified: Tue, 12 Nov 2024 10:48:41 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:f6570237cf1c53b7fc9798f7d7d180fd85a810ec7508ddf678be907805478477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132279504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76828b8ec4ffe1c00bbb572cc26baf17fbba83775e2e3d304b682a579746b6b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c93e3e24b17f6f4677565573caa7c1fcb50037a15b0c78f697c14fec1bfe7f8`  
		Last Modified: Tue, 12 Nov 2024 03:08:20 GMT  
		Size: 102.1 MB (102132018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc93bf5d627266a3e6baee1921524e02dc602ba00b654a6b1c4acec1bfcbeae`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba71f3fb3528c4a90663ba66aa7ce5407d2acd9714e370fd3fbcd9eb7cf5526`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:24b3be81ddf3e057596748db5e20253c7f6c6d297be3700ed517574ee8b3ef10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec81166fd8290376a1f9ed06ddfd54d839dfff16886844dc3053955bb53631f9`

```dockerfile
```

-	Layers:
	-	`sha256:422ba87ca39da1f044b674ae8bc931cc96ba1729b26fee285d45c5071094d056`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:23fa67728036d3fa71b0e8d14ecbcc0790ff417cdea386bc0f1f59ea08c54fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138071252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dc50f91816e6b79c2e34d97563e7192ae06ab99f6449de29c2a103f692fbdb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b40b8ec21666519f6048e9809c98d76cdb14cdd1f714124c728cdcde74b201`  
		Last Modified: Tue, 12 Nov 2024 08:16:03 GMT  
		Size: 104.9 MB (104943862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db6d1a8e68ac2829ce68950198a4a5d6bd31792b8f74a392f2a9ca2d0aed14`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb4cbd2942a8262cd4df9b8ff386bbea378dc638bc71d5add84a5825e1375aa`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:71547c8f59c36f7246f88890ac942f133fa911de88c5991e17bcbaf74c65f447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c1f525f9a4ffae1ed0e97818cd93877bad42950f6f42ec26828e94c4a3de20`

```dockerfile
```

-	Layers:
	-	`sha256:0788868b60f7f88bca46fb03d6186b3e94938faefe4fa9d7aa928e4d6c14e177`  
		Last Modified: Tue, 12 Nov 2024 08:16:00 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:01db2624b5765bf290eed9a2e85931a64f88b7036e7d5c0ae1794097e04cf6e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112730439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36f7f17ec67918459d161c53fcb045125407b045e4df3b449f5903053bde8f2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=7.6.1
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Sun, 10 Nov 2024 02:42:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VSM_NOPID=1
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.6.1 DIST_SHA512=a43ecdcc5a113b947d56a7f28d756199c82e702a0e98bbad635a5df4739c50aaf778143dee3acf57d586569b780615ed73996df71488e4f776fb515f206b7fca VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
USER varnish
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73895e6530429bd612b9331487ed4811ebd13bf2ac83e86bbb9420ea2779b2bc`  
		Last Modified: Tue, 12 Nov 2024 08:50:39 GMT  
		Size: 85.2 MB (85236779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8731a2370a6a81543907fc7a5ca55c7f89742f1f15ab0d4a6a79017a7c0fc7ab`  
		Last Modified: Tue, 12 Nov 2024 08:50:36 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a191d99ce02a230e9d85421b014d896f26f71503736d3696b654198161bc76`  
		Last Modified: Tue, 12 Nov 2024 08:50:37 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:673ebf6cf0d2a68417555ac882a255175d54bd39747b74c26845c61bd24b04e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe4d455733fd153e0ae17465ac077e05d2343f6531863707618d5063d219ee1`

```dockerfile
```

-	Layers:
	-	`sha256:cf0b77ed9acc0c7df48fbe09538ae5cd332afd2c72a896e0e64419dc124c6553`  
		Last Modified: Tue, 12 Nov 2024 08:50:36 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:b618e376341ca332583e924eff5f184098ff96600bfb46473ed184f8f2a61cdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:94a0b719b3e2640ded1e17857eb2f17dd52f981f9f438b072e739932b5f3d910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134853200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bee4e830916f6bf61c542a6ca360e4e739860721e8fe4dc0ae3f59d744ce059`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488cc84bf670e30574b1befbf0cd6925eb970dc7edb66339d5cd3b1bb30e4191`  
		Last Modified: Tue, 12 Nov 2024 02:14:01 GMT  
		Size: 105.7 MB (105723175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90d869b88149c7e067a143b4ba1e6c7fd811b4de90818e14cbe2b4c98f08b0`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f43dddd82b1799b259a52d84c8f97886ac435347592ea3d16620fc053e5ba2f`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:2c212cc3ee562ed0bc28a0fd59af348f37ceb4bcc9d597f6cecc236f926abaa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3ecccd4f353937ea748cb36599c9262502f8672808315c03cb94b5e51f2c12`

```dockerfile
```

-	Layers:
	-	`sha256:693b458079835e525c2325e20fa5a2f63e1fad9ef98cac1da5bb0d217f5f84b1`  
		Last Modified: Tue, 12 Nov 2024 02:13:58 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull varnish@sha256:313a647516a8b72bfab18b3d90290d52ddb51fae4f7011d88f6f61d525ff90d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129354645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2283dd3e564e52b6a551dcc405668a0de000267f5b05b64bc994addea1db1670`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485c9bf90a9b47fc9e115175e1438347317130056edda023687e2b8d1964e297`  
		Last Modified: Tue, 12 Nov 2024 10:53:15 GMT  
		Size: 100.2 MB (100195258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc95d7d18e652867e79c05434cec6f760630bc2e49896fd7dc49fb554e94ed9b`  
		Last Modified: Tue, 12 Nov 2024 10:53:11 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5923fb57e575a592fabbcec9b22a65e1d89d705b55cc286efe87b51d774041`  
		Last Modified: Tue, 12 Nov 2024 10:53:11 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:bacc180149f2fa20e1b9a5c1c59ea3c163d571fbe3ea7a5e05126449d18946ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d7564445cba3ec00c65d853472ed00f181fd1fb723b4811bd561b8f15db5d3`

```dockerfile
```

-	Layers:
	-	`sha256:52679d071576580797ce9d04ef9250cf0cb9d5cf7c6949945788560c45839d52`  
		Last Modified: Tue, 12 Nov 2024 10:53:11 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:305c470aa3ded14f764b1f41124b7671c2a6b6da6212e89691e475162e8014df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132015848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9e56880094fdd51985109b9cd6c3ca4c284b00969afc88c4ee475b9782b8ca`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd48256999b923e6a5a6939529b9e97e128448e2dc38e5a98226f9c2483b75e7`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 101.9 MB (101868368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178779e0dd46b7438ebf7a2a171ac4a6135b19b9314e50165261851c781b86e6`  
		Last Modified: Tue, 12 Nov 2024 02:14:00 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58aa1c556f9dbfcead83df9fc499ea78d38c9f4274c6506634659101326a3f4`  
		Last Modified: Tue, 12 Nov 2024 02:14:00 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:5a00c08c0e1059006be591813c815e366c428d89439dee428a0074898963ba22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03398597f16554f1cbb20fd418f774939e22db27ebdb04a27d06a0da7686fc5`

```dockerfile
```

-	Layers:
	-	`sha256:7d42e31fc94550053d0e1d64ae23d11da1fbc085f594d5aaae87d550fdabcd40`  
		Last Modified: Tue, 12 Nov 2024 02:14:00 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:9c5f38d08cf8ac979b28e55d30ba193bef196ae74854cee656900e23092ad734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137788869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed05ddb045976c21f3f59d42db251caec405e05430317746cc5f7ab035461d8c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b21e9096689a76a0e0cb9bf72040ecc6624d1be69a2e1f21a723b52aafb3c`  
		Last Modified: Tue, 12 Nov 2024 08:22:19 GMT  
		Size: 104.7 MB (104661479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4794496f5b55b28c84ebc111fa82dd0b6040610392d9d8a226e714ebc204b503`  
		Last Modified: Tue, 12 Nov 2024 08:22:13 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6698a62de09bc055930556e9fe57e1e2ea0c75f24acf1f6d23d0a931d624feec`  
		Last Modified: Tue, 12 Nov 2024 08:22:13 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:882d801335d297cc2fd2e4ab00849288f38d77e10dfcf86bac6b68227d74ec58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c975b09bc154554c02eb9a2caf76ce99f37751cc7f363a71d364118967352e`

```dockerfile
```

-	Layers:
	-	`sha256:4ec8b5f662b837363dc4c989f263629678518e880b93b31b44247116a72be65e`  
		Last Modified: Tue, 12 Nov 2024 08:22:13 GMT  
		Size: 18.8 KB (18842 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:96948e4610b7964e6db67d68abff531467e77c7260448407cb130ba0580691f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112446573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b59f5979e8749072f59210d597a4eaaa302260573c664f2133bcf3ddb4943a7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
CMD ["bash"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64e58c8b20bf75539cf7f1f804b16e5553bb1c7bdf0b7b89b4ae337fa8e81b2`  
		Last Modified: Tue, 12 Nov 2024 08:55:42 GMT  
		Size: 85.0 MB (84952911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92103b008c483694642898d758639f8d7c3484eaa82959196c0f41769a3f939d`  
		Last Modified: Tue, 12 Nov 2024 08:55:41 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3ba0561e0f89a79cb397c6c11d6bf6b7d38bcb8ddbda0a8b922b45eb0c6db9`  
		Last Modified: Tue, 12 Nov 2024 08:55:41 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:a2421848df597788940a00db58ec724a441bb8f655476fcd2fed5782c9d3e08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592e17482e7b45896b113979ae7a19c16397c4189c963dd152f8104a69efbf6d`

```dockerfile
```

-	Layers:
	-	`sha256:d3e19ea591bf8e2bee1dd63307d753e1a376b06dc60326880e6833a9ef5772e7`  
		Last Modified: Tue, 12 Nov 2024 08:55:41 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:bdb2d25c2abc7a40dab307580ec6b224bc583159d5e1c958e6490d645e6b5889
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:b88e87349ef0526e4c3c9ca342419cad272ae9d859e191dbc6b905f75d8f584b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75295019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b575452f4dbc566faa94f864acfbdb179386c138abe40cc9915e09ecff1571`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372b7c820710eb59ac6294c8d1bf020b6054fff084972627d39ea76fc7cc730a`  
		Last Modified: Tue, 12 Nov 2024 02:13:00 GMT  
		Size: 71.9 MB (71873252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f479569ba4eee3fba63e1c3f816b50bdcf4f066744c4bd0097f88f53af4839f`  
		Last Modified: Tue, 12 Nov 2024 02:12:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf86448644c977c6a76b0ce5d7e4af967be1b6f53d2232f3c6c9be422e44865e`  
		Last Modified: Tue, 12 Nov 2024 02:12:59 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:94c867e59bc863b7f4fe4ff0b6fbfd7f57f18f0dc0e76b1b75cba108e6e77bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cf59ab507654bbc1044a931afb77617ce5c4b390f3584352628aa914c73b65`

```dockerfile
```

-	Layers:
	-	`sha256:cde3780c4fc1a186faded0b7a02c286b675dbc292b491df0987c0beaf043856f`  
		Last Modified: Tue, 12 Nov 2024 02:12:59 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:253674c883bcfcb4a1f31b239f2c24e7a04db73e6ed93cc65b51e0e26ebecf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59056711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2506cc77824d3689ac65e41e67258e793a249356d53b88cd01aa72a862ac6a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bd5cb802d85c2e91c74445d25463939b0907216488f4851e74e1c702dd991c`  
		Last Modified: Tue, 12 Nov 2024 15:54:26 GMT  
		Size: 56.1 MB (56126931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc1f70712333298b8460020efce137c9f3b37524c3d35457bfd4fbc274271ee`  
		Last Modified: Tue, 12 Nov 2024 15:54:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a637ef13df496373fe769d481b8fcdd358d0a2e8ed259a99a4da9b1a2cc3924a`  
		Last Modified: Tue, 12 Nov 2024 15:54:27 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:828f64dde270181077e8075a682091daf054af6d99b5d8abb0f534ab786b8401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee28dbe0715d58aba783abbbaa9241295728ee4481c563be8b363b906d6955a1`

```dockerfile
```

-	Layers:
	-	`sha256:927ee010c38ad7110b9c618472cbeb1ad23ca2d5510355b0fa703fb599b507ba`  
		Last Modified: Tue, 12 Nov 2024 15:54:24 GMT  
		Size: 18.8 KB (18830 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:5b124902dd89c2420a1f911a752f430bf19313e3e18b815792c9758e39c26dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71884849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f379f32b28042de5e48af9c14a5a06d9ce38ed3af4b23f94d8f937d2d3bd101`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eeda6add61cff16b44d1a88d6ed0c519389906f9aa494add7a583a0a6dfbbd`  
		Last Modified: Tue, 12 Nov 2024 10:54:53 GMT  
		Size: 68.5 MB (68523556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dda850377a6ad5f54f6035bac4db6f6bd8457d78e8a65a0af2185cd2181c24`  
		Last Modified: Tue, 12 Nov 2024 10:54:51 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd69887e6e4a1fb9b8e4d849cfbf3f5ca49775c6ee373d04d42434dcc3f898c0`  
		Last Modified: Tue, 12 Nov 2024 10:54:51 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:987df32dfad2fbf229c6e462eca7c3b87207ea40f6ac4613d82471057ea69410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6146b5011321b518fe02b97459fd0768023d3bea266e5bdfd7a3a30c1ee6e6`

```dockerfile
```

-	Layers:
	-	`sha256:d3e0430312d540571589e2c3394223aca871baa1d24f9bdebc3ef643308cceb7`  
		Last Modified: Tue, 12 Nov 2024 10:54:51 GMT  
		Size: 18.9 KB (18855 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:74b46799a1437550ecef5b61ac7e66d95ad6d44ba748ae38e5e6d09d21e5ea66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77144543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fa6b8af0ddb441fd25f4feb96591eca4237743aa6e2fc85f583bbc7d0ca724`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e707f4676f8155f7af3467c0ac98ee79aa94abe48a3b20ee8c46a3e336b2f7dc`  
		Last Modified: Tue, 12 Nov 2024 02:13:11 GMT  
		Size: 73.9 MB (73888830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c01057ef20a199981392af38cb8ee25e15a9771d7e894f32e37d96856307e8`  
		Last Modified: Tue, 12 Nov 2024 02:13:09 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefde6ea9150f15fb457283144cb065f9c8e206794272d30d384716e897f5fdb`  
		Last Modified: Tue, 12 Nov 2024 02:13:09 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7b046a42b16fce1c6d97d986c9dc237689af1e23622eabfaf3ce45adee7a8636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c364eb2440d15f91c64952e3c8d3ae4e91345d8395081575484fc04066d9fb6`

```dockerfile
```

-	Layers:
	-	`sha256:0f7d8e747f6a04af94ffac3d2651bb786d0d5bc9601daa00cf3eedfbb2b73b89`  
		Last Modified: Tue, 12 Nov 2024 02:13:09 GMT  
		Size: 18.7 KB (18736 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:203426874009453571dbb4535c51e3660ca6c859fbc3322ff583f182a1d503ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72670810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdb5a0b7df6474ab21cc21174102ba749618a7934fd570a897a7d2928a30bf5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315d3daa8ba656231edb65340bf5373311e6520a6a4a77a7ddc98874600de571`  
		Last Modified: Tue, 12 Nov 2024 08:24:18 GMT  
		Size: 69.3 MB (69304263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b6a331cdc0580cd1d9b409a087fb509dd222f62e74498a640741da87752ce1`  
		Last Modified: Tue, 12 Nov 2024 08:24:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4129387d9100b5a099dd0e287fa8e518cea2fd43d789ebd3592ccfe8fd760d8e`  
		Last Modified: Tue, 12 Nov 2024 08:24:15 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6e0fc6f1ead4f281d104c2c6538fa43e0b68090c75ea989df8e94fd823ce9c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4516fb439c1e017c3367b1e817e3bac65c4adb1c0fb759dc647266a5439b5a`

```dockerfile
```

-	Layers:
	-	`sha256:0353503967374c9544a14d9477dd93cca528fc16bc6133418ce8b7d1d281337a`  
		Last Modified: Tue, 12 Nov 2024 08:24:14 GMT  
		Size: 18.8 KB (18800 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:280431fdc972bb57d70db6aba3fd865af9eeb3b2b539f279dd52ec5d5f22d65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66945128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191829c29028766d13169c317eb8dfdd60607e5c2c9a7b4378fe840ec2a796ee`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227ed073ea3a72fe745d5cf9086d188c5621272441c473087c9551d8fe016845`  
		Last Modified: Tue, 12 Nov 2024 08:57:47 GMT  
		Size: 63.7 MB (63689686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786c47033a0cdf1d9694e8f155195d486564713bbcc8c0afa25f10e8cc9cf5a4`  
		Last Modified: Tue, 12 Nov 2024 08:57:46 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdad625a2298295c47b0afe38537b97adfab617b746533d7813203e73ba2e6`  
		Last Modified: Tue, 12 Nov 2024 08:57:47 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1af76c98938d555bf70b17f809fc384184efd5dcb553252fa561c11cfeda0d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b774ff1a12a4ed11c894c7d291af79edf0f336d527b0b9123697b6488ef056`

```dockerfile
```

-	Layers:
	-	`sha256:2a25a9381e53150af50066c9cc8bcc9b8b94ba544f58e1ace2fc4908e90e929b`  
		Last Modified: Tue, 12 Nov 2024 08:57:46 GMT  
		Size: 18.8 KB (18763 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:stable`

```console
$ docker pull varnish@sha256:5316358e37d6483a9d871567fe040188e8b7fc5e428b5a05bafa3cea45d519ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:64aeae75a5e09d94db2c76895f130f5c052c39e0eb9c63b483021a69d4c28de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128656670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b94fc1fd2fe475b5f9ad3911e1be01e58c8931190ffadca398cd68343a0fb3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c487894b11ae490ed2019b5325b3f15ce8264a7f2668193a8376330c5aac73e`  
		Last Modified: Tue, 12 Nov 2024 02:13:08 GMT  
		Size: 99.5 MB (99527937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae224e44658b5574e45a2688885f4a0c9eeb5384c107f662c0e0eebd3f28ae8`  
		Last Modified: Tue, 12 Nov 2024 02:13:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:b333b90d72fbe742b7de9f179a1a76808d1693126090444ea2ff54af9c57a255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0548c5fa56eea15d4006a254f506faf603b0af9f9221e78ea7fa24a34b6fcdeb`

```dockerfile
```

-	Layers:
	-	`sha256:0a0e4192aa712731cafe7b8c5f79740ea638b2d38ccf116057d547098cb2a88d`  
		Last Modified: Tue, 12 Nov 2024 02:13:06 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:64869f8649218936d22fbc4ddac170fa656110142449f0c2a1fb5f5267fb824a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99067059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8faed3629ad3e6492ad5706a215925c220a6e34862d0f3cda68d4b0ae6889198`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8456a9b5aa6395e5bd4e0d827bd0199786266efef009523afdebcecd9951a00f`  
		Last Modified: Tue, 12 Nov 2024 15:58:13 GMT  
		Size: 74.3 MB (74347410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3502743e7a4885b252192550073c40c3d05ceb83c44064ac6796510cfb6b9a5`  
		Last Modified: Tue, 12 Nov 2024 15:58:11 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:5f0d72757437b64ee1a3c80df979868e544eb384f4fb590e5db0ae967ceaabff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e599a23ce279cbd2c4813430f6977c69171fa8037fa7b65e0c3c107e3162b3`

```dockerfile
```

-	Layers:
	-	`sha256:5160c1321f23efb99a42de03d1215594467e7b280037b0a7ed07b5fde3b8e9f8`  
		Last Modified: Tue, 12 Nov 2024 15:58:11 GMT  
		Size: 12.7 KB (12733 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:13060403b287be57e729c8c7a32d91064d053531f048ace88bc0cb55214a1fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123444270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e51986dfd32b22e41cb76677e09b2adac44994cca787825e68575a582fe2b19`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d483cab88ce3581e81c671bdbedee568fe2d602a18330b40776c6167df407bb0`  
		Last Modified: Tue, 12 Nov 2024 10:56:57 GMT  
		Size: 94.3 MB (94286175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ebc8794c007f9d635580a20ae6573877e00b8f3a8041a1bb7462e3c42788b8`  
		Last Modified: Tue, 12 Nov 2024 10:56:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:764356b1568f4e67f4b1251ba1968e3042d8233bc750731cafd8463f64016628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d102cb1d9e10a14e729f90fc3bc826702e0487a92406dc4904e7fa079fb17f`

```dockerfile
```

-	Layers:
	-	`sha256:3c08a032f3396b103a97c5bab64e3d19c0ea4417054d633e1edefdd41d0c0247`  
		Last Modified: Tue, 12 Nov 2024 10:56:54 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:9e44f5f6611a706a296ac8eb79a8f3fc24bf660535a26737537d7df64dcf9183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125834427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d0f68a59169a073f7e9a13262a13ef9ab278c9f26f16eaa20989eb450cae32`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867085a972406fae8a8329d78c27fbd0627185530d7c34e8deb90d3aa745189b`  
		Last Modified: Tue, 12 Nov 2024 02:13:27 GMT  
		Size: 95.7 MB (95688237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c02d919c6bdcfa5b509588ac1fab36fbb3ca112216438ac05264938564b6da`  
		Last Modified: Tue, 12 Nov 2024 02:13:24 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:a6e4f7796d9edac4849d087dc2392fd40f320f86dfd6102192ea3e485d452703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca167cb9e7d623d92ae1f70c9360a12e7679a5ece1c28737a0feef42e21193c`

```dockerfile
```

-	Layers:
	-	`sha256:89316ce791ee480dba1b5bb1c8dee974597a82174b9dbf9eb9f716c6336634d8`  
		Last Modified: Tue, 12 Nov 2024 02:13:24 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:806ba0a60018422bfc0e7988cd5f543f50d3353b9cea8de6f2969f11c7fcd557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131456053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d8a38a5ab3ace0c6670d059ac25eadc79275ae555453176228c48d4c66aa88`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25bdec4f657e8fbba9815ff7113c29239ffaaf6708efa25f009e634c61d5949`  
		Last Modified: Tue, 12 Nov 2024 08:27:51 GMT  
		Size: 98.3 MB (98329960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0570a365404c3c134a2b3020ca2943c01ed8874c91ada4690fbb3301384f9c`  
		Last Modified: Tue, 12 Nov 2024 08:27:48 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:1690f179714f2a0f0085d36d5e429db7fa6c3b75732111cc2c88e179b337f452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45fda85373e547abcc335bcdf3a2ced67ee04184050ff096b491e89bf22e716`

```dockerfile
```

-	Layers:
	-	`sha256:c7e87262c0785f1a05e3940da2daf1c465a40e3b9b24de0301103f72ca5b5bab`  
		Last Modified: Tue, 12 Nov 2024 08:27:47 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:2a93f5f6c28e0e74b83a73237b530b9193f6ceb87ea78150ad032487fd80a0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106222947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e841bbcea8c324181247a6a52921d2a07b561859c0c84a3bbbe52256235ef5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD rootfs.tar.xz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
CMD ["bash"]
# Sun, 10 Nov 2024 02:42:48 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Sun, 10 Nov 2024 02:42:48 GMT
ARG VARNISH_VERSION=6.0.13
# Sun, 10 Nov 2024 02:42:48 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Sun, 10 Nov 2024 02:42:48 GMT
ENV VARNISH_SIZE=100M
# Sun, 10 Nov 2024 02:42:48 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13 DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
WORKDIR /etc/varnish
# Sun, 10 Nov 2024 02:42:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sun, 10 Nov 2024 02:42:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Sun, 10 Nov 2024 02:42:48 GMT
CMD []
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427dcfa76abd1ed38c5a3a565bb1ba3fb0611ea06d61285aa2446b4ed5b7459`  
		Last Modified: Tue, 12 Nov 2024 09:00:00 GMT  
		Size: 78.7 MB (78730579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658c572f815bfab73a7ea7d0472638b0693a9889faa06c37927945fedce377d`  
		Last Modified: Tue, 12 Nov 2024 08:59:58 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:1381f215e33733e48b21f30b27edb085109c545a9a1a56909aad61d1891d2f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43375fa1bfd0730d623bb813021c83cc0b9aad4e335a7e9e5dbfcbd4f38f3e1`

```dockerfile
```

-	Layers:
	-	`sha256:a479eed989d6c882bfd7350767c63deca6eb6d124471ffd16b837c0b037ecb75`  
		Last Modified: Tue, 12 Nov 2024 08:59:58 GMT  
		Size: 12.7 KB (12664 bytes)  
		MIME: application/vnd.in-toto+json
