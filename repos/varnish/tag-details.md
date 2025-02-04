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
$ docker pull varnish@sha256:181939fa86e965ea5be859bf6d33133750691522c008d4f70acb6b028a09df46
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
$ docker pull varnish@sha256:7eab999ca9ba21e47d3ad7932cdddece413eb62131760028acdb606e94e7d097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127744114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbafa05faa65c7c1b9e5d1489df1f267628b18a558761571589a39e33b0efeb3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081782e116e5eed5271697edb555e187291ce5f8bb24b5a553c9206f86dadab1`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 99.5 MB (99531072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e138f6524b3e3c2020b242f5b79b2866a473387b4a7dffdc369c996bf711698`  
		Last Modified: Tue, 04 Feb 2025 04:38:17 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:dfc08938e97d7371a7aa9a16dc0038f42d9be1a652ba3f54145a8be393b22436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f72107e71a4952b63c4f0a8ac7aa9a0326584686102e21586ab8cb98c89311c`

```dockerfile
```

-	Layers:
	-	`sha256:2965fac2a2e017081031b82c8853f86174239a23d0dc90b4d82a67bb3f256d18`  
		Last Modified: Tue, 04 Feb 2025 04:38:17 GMT  
		Size: 12.7 KB (12664 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:f3eba1d3d82e6515432d2e62ec2951d1f445db43212f5489b18c67369748ada2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98265158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58377b8b5349d38eea94b8754ac3faaf9f77c7824625a14b39b1ca9d3c376f3d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623f1bad8156810b22b0edaa693ad4be604a3f3de28d34c6ad3b6eb689535803`  
		Last Modified: Tue, 14 Jan 2025 08:57:29 GMT  
		Size: 74.3 MB (74349820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc57c835e653933c1a75f0abf7c3c6b385749ff93de73bd74ac6140d6de12f25`  
		Last Modified: Tue, 14 Jan 2025 08:57:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:d54465dd21cc5025bd296b9dd630e0828daf8b323b039f8409598cc22624ca39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142dba2d13a72d70b22190383a71e968f7221caf2eaebc8d84d5be2db30017f6`

```dockerfile
```

-	Layers:
	-	`sha256:4d6b7224fc907f79d3026decacd2c58ce62755d0553f8b10ea40ba8396667072`  
		Last Modified: Tue, 14 Jan 2025 08:57:27 GMT  
		Size: 12.7 KB (12733 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:388c0741d4852895ca0e5fb292d4d71a3f47fe778710017e9ec8fbcc83197d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122335042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa19fcbeadbef7caf3f789400cf8aa99cf97433faad3dbc79ff8ea3a1e910d9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815e7350a51ff15dbd37103ac2c590a51aecc67ca0f7ef1ba80497e801b697f3`  
		Last Modified: Tue, 14 Jan 2025 06:59:16 GMT  
		Size: 94.3 MB (94293273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fb83dac11f68d3b9d6ffc6014f7064e95e8a4bfd4e7d9f429348d7433f87f2`  
		Last Modified: Tue, 14 Jan 2025 06:59:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:ecfee932175e8205ad1fa2ed0e67e8fdd2a3e0e24d7b754c01d8e45fd7a20f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3207beeb8a90aa9293188aba5ad76d3744362ae4f68df488984541669bd8196e`

```dockerfile
```

-	Layers:
	-	`sha256:8abdad0695d4e98ad541ac3ef1e335e604581f1484c181546dbf53bf105a9a3b`  
		Last Modified: Tue, 14 Jan 2025 06:59:13 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:61c4cd8f36067478027462988e93d012e297c951068f8df3a9d877e7b96a2c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124881588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62f7d80394fa02326ed9ba2b787be5fb09983f949b0cea746b302f32827eecf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b4418305a63b59ede7eb4dc3f5f915aecceb2546eb6cdf60d65081fe6f1649`  
		Last Modified: Tue, 04 Feb 2025 04:25:02 GMT  
		Size: 95.7 MB (95693393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1719dfc6f626afadd6b2a874fdc0c6cc87d513591fcc6421152759c453f5fd5`  
		Last Modified: Tue, 04 Feb 2025 04:25:00 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:8d47bec1318c45e301e5ca0a2e9293f66f737a305dc821d9842c7cebdff72fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655b25df2d14182da965a72adca522b43395abb95f1a5bed902f97751f087f0d`

```dockerfile
```

-	Layers:
	-	`sha256:cae5ee654d71dfb7c8cbc261f9fc3fd8c3558605afb138471a22b25a7b7ff506`  
		Last Modified: Tue, 04 Feb 2025 04:24:59 GMT  
		Size: 12.6 KB (12636 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:40cef478164f318e19d43450d12930f64092ded44d29d268339ada5b219eff31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130385950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ece843f84eb6f2546881506c0c0ac76c258829a6cb6ff9af1db6ac38028a8eb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b0fc273c4beb3aeb8252123196070e8712a5556c2abf1a479be94a0136d400`  
		Last Modified: Tue, 14 Jan 2025 05:29:04 GMT  
		Size: 98.3 MB (98340365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811487ce142300c995652dc861ebfd95fb8bd3ada20d8106867a3cc5ff0280a5`  
		Last Modified: Tue, 14 Jan 2025 05:29:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:c6f4c6b0d234a8d0aed90aa7696b478287d6a2e6e00f1b546ae1774e871195ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1434e9aae546019c74bdf96baa5c226874ddc0c8143f1f291f0fe7277bd45a6e`

```dockerfile
```

-	Layers:
	-	`sha256:fc18ea2fd0bb91f94d83eb7ab5feb465aafe09c0b63fca6b29eb0429eafd0ce9`  
		Last Modified: Tue, 14 Jan 2025 05:29:01 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:112f1331e4a4b811eebcf3d86202b7ef5e52c3191b113149750c64fd1a9f76ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105598496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622be870f743ed1c0c7a06281122a2d8de9b9f0ae7a774f9c2697b1065d20a4e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d85ab31aecc604366f0a97a38fd5ed12e3ce8659de9b0a170b669bbe54be601`  
		Last Modified: Tue, 14 Jan 2025 04:58:34 GMT  
		Size: 78.7 MB (78739019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae7f98d2b1033968b9c6a8052d2633b2ea0e3d621ac2deb7cc82de68a0ee767`  
		Last Modified: Tue, 14 Jan 2025 04:58:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:0980688787d4adf583fbda153f13760e33d65079c995b037d6ee933e752baca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f34e12f163cf3800437b56ac9d6222627e0068ffb5ce95baace42eea9006b1`

```dockerfile
```

-	Layers:
	-	`sha256:f86cd0c141117065b5179f61f9ce8504c1ac275e075e15fb1adbb4586875fc59`  
		Last Modified: Tue, 14 Jan 2025 04:58:32 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.13`

```console
$ docker pull varnish@sha256:181939fa86e965ea5be859bf6d33133750691522c008d4f70acb6b028a09df46
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
$ docker pull varnish@sha256:7eab999ca9ba21e47d3ad7932cdddece413eb62131760028acdb606e94e7d097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127744114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbafa05faa65c7c1b9e5d1489df1f267628b18a558761571589a39e33b0efeb3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081782e116e5eed5271697edb555e187291ce5f8bb24b5a553c9206f86dadab1`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 99.5 MB (99531072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e138f6524b3e3c2020b242f5b79b2866a473387b4a7dffdc369c996bf711698`  
		Last Modified: Tue, 04 Feb 2025 04:38:17 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:dfc08938e97d7371a7aa9a16dc0038f42d9be1a652ba3f54145a8be393b22436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f72107e71a4952b63c4f0a8ac7aa9a0326584686102e21586ab8cb98c89311c`

```dockerfile
```

-	Layers:
	-	`sha256:2965fac2a2e017081031b82c8853f86174239a23d0dc90b4d82a67bb3f256d18`  
		Last Modified: Tue, 04 Feb 2025 04:38:17 GMT  
		Size: 12.7 KB (12664 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; arm variant v7

```console
$ docker pull varnish@sha256:f3eba1d3d82e6515432d2e62ec2951d1f445db43212f5489b18c67369748ada2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98265158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58377b8b5349d38eea94b8754ac3faaf9f77c7824625a14b39b1ca9d3c376f3d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623f1bad8156810b22b0edaa693ad4be604a3f3de28d34c6ad3b6eb689535803`  
		Last Modified: Tue, 14 Jan 2025 08:57:29 GMT  
		Size: 74.3 MB (74349820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc57c835e653933c1a75f0abf7c3c6b385749ff93de73bd74ac6140d6de12f25`  
		Last Modified: Tue, 14 Jan 2025 08:57:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:d54465dd21cc5025bd296b9dd630e0828daf8b323b039f8409598cc22624ca39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142dba2d13a72d70b22190383a71e968f7221caf2eaebc8d84d5be2db30017f6`

```dockerfile
```

-	Layers:
	-	`sha256:4d6b7224fc907f79d3026decacd2c58ce62755d0553f8b10ea40ba8396667072`  
		Last Modified: Tue, 14 Jan 2025 08:57:27 GMT  
		Size: 12.7 KB (12733 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:388c0741d4852895ca0e5fb292d4d71a3f47fe778710017e9ec8fbcc83197d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122335042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa19fcbeadbef7caf3f789400cf8aa99cf97433faad3dbc79ff8ea3a1e910d9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815e7350a51ff15dbd37103ac2c590a51aecc67ca0f7ef1ba80497e801b697f3`  
		Last Modified: Tue, 14 Jan 2025 06:59:16 GMT  
		Size: 94.3 MB (94293273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fb83dac11f68d3b9d6ffc6014f7064e95e8a4bfd4e7d9f429348d7433f87f2`  
		Last Modified: Tue, 14 Jan 2025 06:59:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:ecfee932175e8205ad1fa2ed0e67e8fdd2a3e0e24d7b754c01d8e45fd7a20f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3207beeb8a90aa9293188aba5ad76d3744362ae4f68df488984541669bd8196e`

```dockerfile
```

-	Layers:
	-	`sha256:8abdad0695d4e98ad541ac3ef1e335e604581f1484c181546dbf53bf105a9a3b`  
		Last Modified: Tue, 14 Jan 2025 06:59:13 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; 386

```console
$ docker pull varnish@sha256:61c4cd8f36067478027462988e93d012e297c951068f8df3a9d877e7b96a2c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124881588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62f7d80394fa02326ed9ba2b787be5fb09983f949b0cea746b302f32827eecf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b4418305a63b59ede7eb4dc3f5f915aecceb2546eb6cdf60d65081fe6f1649`  
		Last Modified: Tue, 04 Feb 2025 04:25:02 GMT  
		Size: 95.7 MB (95693393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1719dfc6f626afadd6b2a874fdc0c6cc87d513591fcc6421152759c453f5fd5`  
		Last Modified: Tue, 04 Feb 2025 04:25:00 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:8d47bec1318c45e301e5ca0a2e9293f66f737a305dc821d9842c7cebdff72fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655b25df2d14182da965a72adca522b43395abb95f1a5bed902f97751f087f0d`

```dockerfile
```

-	Layers:
	-	`sha256:cae5ee654d71dfb7c8cbc261f9fc3fd8c3558605afb138471a22b25a7b7ff506`  
		Last Modified: Tue, 04 Feb 2025 04:24:59 GMT  
		Size: 12.6 KB (12636 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; ppc64le

```console
$ docker pull varnish@sha256:40cef478164f318e19d43450d12930f64092ded44d29d268339ada5b219eff31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130385950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ece843f84eb6f2546881506c0c0ac76c258829a6cb6ff9af1db6ac38028a8eb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b0fc273c4beb3aeb8252123196070e8712a5556c2abf1a479be94a0136d400`  
		Last Modified: Tue, 14 Jan 2025 05:29:04 GMT  
		Size: 98.3 MB (98340365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811487ce142300c995652dc861ebfd95fb8bd3ada20d8106867a3cc5ff0280a5`  
		Last Modified: Tue, 14 Jan 2025 05:29:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:c6f4c6b0d234a8d0aed90aa7696b478287d6a2e6e00f1b546ae1774e871195ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1434e9aae546019c74bdf96baa5c226874ddc0c8143f1f291f0fe7277bd45a6e`

```dockerfile
```

-	Layers:
	-	`sha256:fc18ea2fd0bb91f94d83eb7ab5feb465aafe09c0b63fca6b29eb0429eafd0ce9`  
		Last Modified: Tue, 14 Jan 2025 05:29:01 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.13` - linux; s390x

```console
$ docker pull varnish@sha256:112f1331e4a4b811eebcf3d86202b7ef5e52c3191b113149750c64fd1a9f76ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105598496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622be870f743ed1c0c7a06281122a2d8de9b9f0ae7a774f9c2697b1065d20a4e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d85ab31aecc604366f0a97a38fd5ed12e3ce8659de9b0a170b669bbe54be601`  
		Last Modified: Tue, 14 Jan 2025 04:58:34 GMT  
		Size: 78.7 MB (78739019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae7f98d2b1033968b9c6a8052d2633b2ea0e3d621ac2deb7cc82de68a0ee767`  
		Last Modified: Tue, 14 Jan 2025 04:58:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.13` - unknown; unknown

```console
$ docker pull varnish@sha256:0980688787d4adf583fbda153f13760e33d65079c995b037d6ee933e752baca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f34e12f163cf3800437b56ac9d6222627e0068ffb5ce95baace42eea9006b1`

```dockerfile
```

-	Layers:
	-	`sha256:f86cd0c141117065b5179f61f9ce8504c1ac275e075e15fb1adbb4586875fc59`  
		Last Modified: Tue, 14 Jan 2025 04:58:32 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7`

```console
$ docker pull varnish@sha256:fcc19990b5009e8d6872ecbab103e4e3b5d9e889bdf1d1dc295c185bf4fcb9b7
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
$ docker pull varnish@sha256:b87b0410c06db25d8a1eee7f1b1810c597a92b955351a5d9991a342f2efb01e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134241793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25e7979d0fe2da9c2e24402be0ffd0bd75756b4f02bce8afa7cedcb8ed36650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67ee532e82dfc81655928a069b82485465822cbf5c1542f69c6d34d2faf3648`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 106.0 MB (106027463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2958af66e2a26b4907cb4ac12a284d9c9037bb0675929e18c0684a07e175f3d4`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603feb9d9bd8c46d13cb279a37a354faa7d1121aa86b4f1989264bec05f080db`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:d69f84689c980cbd991fc051a2dcddc9efcc621a36fe697b1146b00b7d3ec696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdd72eff6cae3462e76c0cd730aa70e1172853fe5aa8bb65fb763776d47d370`

```dockerfile
```

-	Layers:
	-	`sha256:2513e43cba4d6a41c4cc145ae8c3232574ebbd10125c541e2160bd5ac987bdb7`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6c6a9f46639e61c0a1f61baf41f9d8745e6427ffb53c78f2dd15c44eee937209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104582434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466337ca1f1fbaace72e6a4643a8c3eec8d2d743e703e0004aefd901006b9cb8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e8b227058e9d3454106b69de6fe66ed17472d316ff1921b311633240d0ec9`  
		Last Modified: Tue, 14 Jan 2025 08:52:00 GMT  
		Size: 80.7 MB (80665801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef606ddc5460ca106eae7ae656ae0cd58d4ed4d51a760fa98f5eee9d2b83956a`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd367c2f86e70c54d56ae1340603abe7796a5009f884f3516a60201fc33811c7`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:db318c923596723ecf0789d3bc89d94eaea463170207a15a7a33b083e86d4a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f348855c155e8e496de72e8473741aa67df417539e48b6a5ff32acbbdd77049e`

```dockerfile
```

-	Layers:
	-	`sha256:041ac58bc5d4000faf092ee1cf0a347606281ab0da8aba370347b562b59e2385`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a1d3ada6bad3845372d3dcf432d32cbfb189e409cedb54d0f1a242e3776fc812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128523233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef025c412b02b3498e4f94b33ec1cada8b72226b953ad58c4ee179766ab4410d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626bc79106fc52a258b19e1b8cf9198fce3c923c7b95da70f12ad8e8f976bcdf`  
		Last Modified: Tue, 14 Jan 2025 06:54:31 GMT  
		Size: 100.5 MB (100480172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2beab08663c7aa35e561cca3ebb41cbc71ebe6de2617385520b1d0628cd7931`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be3e3459e06ed6b1bc3d7dd210e7db3bc4ec94a34345b9b8a6f3bbe00297ac`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:021c3f4b064f7e9cbc08600b787cdc2e5efb3cd884a9cf919c0b7250909904d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3dd6d1d3f06388322d2e9f03601d9d96bc45eb6eaf61b1b8880bdc5b15f7e0`

```dockerfile
```

-	Layers:
	-	`sha256:04bf3117b2f9ac01066455de1fff3460fcd52addba37c0810b20ac0646a2bb0b`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; 386

```console
$ docker pull varnish@sha256:6190cac5d9924878c2b8728f9592099581bb0a3f4d7d381f5f9f529817f5a9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131328178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aec168bc04f7cad8376f43f41a969143996ec48e484f1f4e9f30e3edf1a6738`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e55145e6767f7d9669a44c343e78f5f089496cfe29cb1171ff95a388e8d577b`  
		Last Modified: Tue, 04 Feb 2025 04:39:09 GMT  
		Size: 102.1 MB (102138693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1239ea0306c326a98823d354aa04ba633c23b14acfac4c4b0de83733522813`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833543a02a818ec2d1ea9d4b9e32d0f0222c832893edc139c8c5dbbc63753dd3`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:2b883f256313e43c6503d1000d37cda90cc5d82fa175d2112fa9cd5bebc3c406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c1b5e4fee186a04f342ccc16b9479323d788276943b0ec8375c42cf4684e4a`

```dockerfile
```

-	Layers:
	-	`sha256:644acc248591d721fcfb9b2001687945d76051de597b94c487ede0b73affe070`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; ppc64le

```console
$ docker pull varnish@sha256:023956b82e9a1d9c9bb184334f4b7b9199c66381c24f428c897f5d4a7400474c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137011865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748f3334be11673591b49c72941ef4d1cfa9237427d24bee54a5258588b71aef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bddbff44e0d90b074d9252780960e743d65647400597bdbdb723bd5f9bfe803`  
		Last Modified: Tue, 14 Jan 2025 05:17:46 GMT  
		Size: 105.0 MB (104964983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95ccf741d55e2393a51c73fd89317f3547d5adb7207dbde5537afc3658ae86`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882ddfad3345715772448bcf8f5c45dfe64cbea01e0ea80d3ba7c3b7017ade57`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:ccfa4ec81beea4b85eb4896509d2d04ff65ad6a685b0bc603e2f715d7b928a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa66aabb06da34b938cc62ea7b7a45196de3d0760ad94174a4a248bee7daa84d`

```dockerfile
```

-	Layers:
	-	`sha256:cecd8427a1bfba726b6d75bff2d19dadfce919cd4b4f62886d38f8a4cf02efba`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; s390x

```console
$ docker pull varnish@sha256:e2658e2b46db161c995e14a46b8c86e2b05dc52e2cd75659a137f647a0003ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112112393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0144263695361fa97ddcffd6c3c9e365b173d3762af5d764c3c42cd60689cdc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f774a4d8b78e92bed8a0db33c73b450dcc47592fda460bc69effd0c061b09`  
		Last Modified: Tue, 14 Jan 2025 04:53:05 GMT  
		Size: 85.3 MB (85251621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d03d5f51f4613e32fd2d3b277656f0203dd8009b2f6e316eddcebc5673a33`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3f67992ed74220778b755e60f7b81a6c917eb1adcd846f3f8afacd330ac60`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:0ed1c02bb35bcc48d4ba11375bd017df3aadeba9577ccd32dc79760544ab8cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f9efc6ce720fdc68b64ba55e6b126ded9de51d7b46334bd48b8042023cfd05`

```dockerfile
```

-	Layers:
	-	`sha256:3bca138d1c90f55120aa3f3e4314121ca90f7142456f54a8cc8c7d86640772fd`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7-alpine`

```console
$ docker pull varnish@sha256:9b5e8c88bb7bef1c29cf817d4d1f402f74ff00d3a075e91a955724aae3dbb79f
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
$ docker pull varnish@sha256:16fd26dbb255c2a652256854071c23d01fad26cb12ac4d26087499df439fb8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73505840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d380dea99cc921b87080ebfeea79c6e431ba52dbdc9196b5e55b1b8ae71c49b5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13071719e86df23adb2f6ecf6c55c18aac855d074b8214240002217e612986c1`  
		Last Modified: Wed, 08 Jan 2025 18:09:58 GMT  
		Size: 70.1 MB (70083556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9d5b7f9d16652100fa7245b6868d6996ce50b359576e257a717b27330b6ae`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d588b07acd892aaf65d6b2e19a3e4aed131407e43a2f4422d66703038dc37e`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:611cde6a197c9607883e5fbd8b64e6a64cf1071eecd9aaab307a6812e45def05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc5b12b26ce300632ee579cbe251c28ba1109818d7668df678e537d4ea4c127`

```dockerfile
```

-	Layers:
	-	`sha256:dd777c39e8a6d248795a40b4b01647c8caea28479a1110228e4d78482cdb8284`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7f140daf95d6e623f71ad1260cb33a81e820790da39329a4b8800ffa6d822ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57703582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c826bb7d37807c477283fcd1e5b44db4b96e497356c487e9aa4076ea435e647e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-armv7.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:a7e7294636d65e1e64be6d2a9e772d5c14442ce00c5a9d8d2fa587f09b5ece5c`  
		Last Modified: Wed, 08 Jan 2025 17:34:28 GMT  
		Size: 2.9 MB (2928493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f078b5e82a729479514897fe95bbb82df97dccdada7ad018f8e01fd3f6d130aa`  
		Last Modified: Wed, 08 Jan 2025 21:57:01 GMT  
		Size: 54.8 MB (54773047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7aa6c0f19e73c709554c56dee03e9679cd0ede758e94180850e32bf78bde44`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8e33f61cc03a4a81a723af523fc522d437087b6f7591880d385babf5f3190`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cc983d1e40f1092ee8ea6a2522092b6761ed4fecd8e49846d875a41853e51a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac62ac3d57662ee732c8c45f82e2cbc2ec73bf1e8c51b20073700c0fcc1e5a6`

```dockerfile
```

-	Layers:
	-	`sha256:c8217ea50488d51644c6cca912882fa1423c6a4d223648173b3f908c626588f4`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:34074cdb3faa15d09741acaed66177e0ed458e6d2168d1f978821d220d626457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70210461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462ae8170be93562c8970b277a272ab82d42971c94479c604c87c630da91bcf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38608fdb51d3fd48708d76faee21aabca1429332c418eaa5aecb9e7cab1514a6`  
		Last Modified: Wed, 08 Jan 2025 22:10:02 GMT  
		Size: 66.8 MB (66847886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f06b07c9c87c108a4a14e4a78d95f53b1f6939a6f65fc3c6f3f037d94bb705d`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f178fd795c4878d915832fbed244eb899faf8e19beee9ba9ac65a05f8ebce1ef`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3aba3b310385ff11eeb727e77e64dcf7f82bd8c1c0f0c396ece9d8562c220df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152b986e7e2661302e7596b28577519ec15cd89c9cd0e2cca5345e9850f93a6d`

```dockerfile
```

-	Layers:
	-	`sha256:ec0249217cf0578e145b31673267f9f1204461fcdd783b691c966d15cd5bd8ca`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 19.5 KB (19535 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:562434133d630a953b772286ad7a18f3a6696f725538bac875d67b1d76259594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75519686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a01041f2bb795cddf11cbf90e7247ea895989e68d445ec77f572fcb10a46f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-x86.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:ae1d9a0eea37f9fb4394d27e83eb58694cd0a74025c8c135051300a330d76686`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.3 MB (3254296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca213630b7b92898fea67a1d4fa8e80adb1fd6752a74c258e6400f2ee8073f2`  
		Last Modified: Wed, 08 Jan 2025 18:09:24 GMT  
		Size: 72.3 MB (72263349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bb948a2097e791a11fd570256b38c402deba49eae4d1b503a5537f885e2640`  
		Last Modified: Wed, 08 Jan 2025 18:09:21 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0ce85798168ae5deef79998cd0fea7b8e43c5207e21996a3b171d10d0fc4ec`  
		Last Modified: Wed, 08 Jan 2025 18:09:22 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:02a9653f559b15d9f62e59c37b59fce45822cdf0a574ae800ec8dd14bf2e31fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17933e8516c168b812417ff2c683330991d3e332d88eea49140ab9c8208e3099`

```dockerfile
```

-	Layers:
	-	`sha256:eae92baafec8ac7815e691dba3570aaf78e0b26e8afb23073c144ca044d188cc`  
		Last Modified: Wed, 08 Jan 2025 18:09:22 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b1fc8a6e49bc791694301145471985b68e3db986cebc579671457088dbe01b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d860b944fabe69b38f9241e520add98d86f8960c863c3ef04d76b6a2f5fd565c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-ppc64le.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:a1e53c81da67874250566308d64e6cf88d5d19fb3bdb55484bd7a41b4e42a126`  
		Last Modified: Wed, 08 Jan 2025 17:25:17 GMT  
		Size: 3.4 MB (3365646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2111caeab3d6550f1541b2aab62aa965d120f846336fcc65ae456a7261e0c092`  
		Last Modified: Wed, 08 Jan 2025 21:34:09 GMT  
		Size: 67.7 MB (67651734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e692af43ad518d0382cf5d2d720883b138934bcf4483540844d6ce2153d1c5b0`  
		Last Modified: Wed, 08 Jan 2025 21:34:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ae4b72f995f49677d04483a1483cd93454e4da829d4f2351c16cd29a9d4f91`  
		Last Modified: Wed, 08 Jan 2025 21:34:06 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5b08d61c40c1c8b3dd5d096cb8df59f0856de70e8a224ddf1b81c5f169975b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46aed5daaa83a08599696d8af042202221bdad6fc459e71096b1547dfb5c42f`

```dockerfile
```

-	Layers:
	-	`sha256:fe733115ad499f835228ad84a88a546714d82faa5beefe99c0a9613194296c8e`  
		Last Modified: Wed, 08 Jan 2025 21:34:05 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:cbb99c922969b843858afdac637caf34f7b745f77932ba94c1afbc194ec375ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65409956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9aa429d3cdb829a494d0b32b6d4004c86a23bbe48504352543aaddafd598e48`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-s390x.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:be00939408ff94e4fec4588babdfc5d58c5d13d897e8cc5dda295b4a6253bfa9`  
		Last Modified: Wed, 08 Jan 2025 17:26:42 GMT  
		Size: 3.3 MB (3254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454b6c666851ba2830e7e659674a9de36b79ca58087a4f9391bb6386c7a814a7`  
		Last Modified: Thu, 09 Jan 2025 07:15:53 GMT  
		Size: 62.2 MB (62153663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b2648b66c6f9626b79ab5954fcab817c10ad4ba6cc30627e0b6f03b9fcaba0`  
		Last Modified: Thu, 09 Jan 2025 07:15:51 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c713504fc9938345c4ddcb6a272dfe45cfda2f8bd952585de4a547f3b75a4d`  
		Last Modified: Thu, 09 Jan 2025 07:15:52 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2bee6a7927d1feed9abe45371c406102aa29847d8667017aad9d7187e1221710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca87ce880e71616e91f4545b11e60df4f30361803d9f06aea0ba84fdc2d5b1c`

```dockerfile
```

-	Layers:
	-	`sha256:ebb911b842dfb2bf726c36bd843d710c5cc80779fe83eabb56e1cbdb23588262`  
		Last Modified: Thu, 09 Jan 2025 07:15:51 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.5`

```console
$ docker pull varnish@sha256:1a667bcd6b64099acbd075b1c347393e3cdb7f76d0b054209ed5bd015142a72a
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

### `varnish:7.5` - linux; amd64

```console
$ docker pull varnish@sha256:9f8e5099ebe0d8c36e5275c92ac41941ac656b81ee99b2242f1bfd2eccf7a870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133947580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0ce3671cc93cda6b4fda1720db7d6f8f58c1f10ad062a16115db45009d2d8d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da20651324383642e77305fdc8e5ee80e40ed9110f7f7fa3a44ca0124caf6b`  
		Last Modified: Tue, 04 Feb 2025 04:26:04 GMT  
		Size: 105.7 MB (105733248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2958af66e2a26b4907cb4ac12a284d9c9037bb0675929e18c0684a07e175f3d4`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18fc8b1264f71a4e5fc52f2bc6e74d64d699c1b0450cf6ce424accae804cc05`  
		Last Modified: Tue, 04 Feb 2025 04:26:03 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5` - unknown; unknown

```console
$ docker pull varnish@sha256:1a5278c3c63de014ce017013bea0011b075c54752ff654276b6eab53026a8e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c3c464581b3f712bbb05dc82764f731c8f5c3ad4549e044e17ecaa7787d902`

```dockerfile
```

-	Layers:
	-	`sha256:b177209b0f766e9795f77d086a175574726188b79051e0e465987a5054710e81`  
		Last Modified: Tue, 04 Feb 2025 04:26:03 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5ea210e09979ca90b9deec1fbedb8695639ecbbb2979143fc3f424b4ad3e6e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104301434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34cb2867fc13015905b8fc0ae4f3e62435aafbca1d250855f0ddf48526fb39a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322188f9e166a922611c24675a020e8057d7fcf53d1053f2bb283b525bde340`  
		Last Modified: Tue, 14 Jan 2025 08:55:13 GMT  
		Size: 80.4 MB (80384802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7e54d0742912b656895a8c84766fd91aee92e87a36cf75770454fadae3cbc4`  
		Last Modified: Tue, 14 Jan 2025 08:55:11 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79c9133be42fc73eb284dce8bb90c975d2c44a550a7778ab14eaf7a2cf5bf6b`  
		Last Modified: Tue, 14 Jan 2025 08:55:11 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5` - unknown; unknown

```console
$ docker pull varnish@sha256:ed97e9ab2ba172f200ba9c78efb63d471ab67092172c33a2913f12d0885ae4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429c83cdc91ff1a0749468e28c605f6cddfab32508e1f07c6eb1282c0e9bc38b`

```dockerfile
```

-	Layers:
	-	`sha256:9f3449d9df625d81759852b8bb625b472977d62d8778b8d6e819cd48ccfd91cb`  
		Last Modified: Tue, 14 Jan 2025 08:55:11 GMT  
		Size: 18.9 KB (18869 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:fe9080130f5fb29baf07e52379a26bc14c30d9cf32979d78cd13d18013ef2254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128228781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7833533f9bcb4c5d332a1a3ade7827bc08c8029967d977581b87606e12d21596`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636e5cc10fbd69609472b5804793d18f5073426b3ff433573f8f3a5eb65f589f`  
		Last Modified: Tue, 14 Jan 2025 06:57:14 GMT  
		Size: 100.2 MB (100185716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dbc759d0ab91f3b54dbde468018717fa687e97be39ac824438c273df06e476`  
		Last Modified: Tue, 14 Jan 2025 06:57:11 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a998e2ce147a4d194fda8e8e26e48a60c2ead365dcac624740112ccadd67132`  
		Last Modified: Tue, 14 Jan 2025 06:57:11 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5` - unknown; unknown

```console
$ docker pull varnish@sha256:b429375d48b4f8f6f126178bf3bf93225f5803ca4c3aae6452e79509d4e32748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e64caa2ca00763e0182119c7e8d62ee25cbaf4f3e16bcf893f0e61e83b4931`

```dockerfile
```

-	Layers:
	-	`sha256:3cdcdb448e5aace0ba34f93e85edcba0b777a79f5b853069f3ecf2a992bb806b`  
		Last Modified: Tue, 14 Jan 2025 06:57:11 GMT  
		Size: 18.9 KB (18896 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5` - linux; 386

```console
$ docker pull varnish@sha256:32961a84374f32ce335c3c2ddc6b9b654c8dceb2681ee77352fd1b1bf8c2a4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131058305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6590994ca1a7c60f38f951597dff1f567e90c921411c9d25f7ea0a2362a5e00`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31381739b1cf1d2013ab05495584256c14f70ff0690459179356fb415eaace20`  
		Last Modified: Tue, 04 Feb 2025 04:26:04 GMT  
		Size: 101.9 MB (101868816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22882845a4dd3b8960abc19f5cbbfbae10af74e6657d93ee64322171a1138aba`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63cfb1491d67d2f05f2d7991a2b1800d36bbda089293f6659a0b8b489e95c60`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5` - unknown; unknown

```console
$ docker pull varnish@sha256:95bb88de67b2a8eafd754aad33701a7e7ebf11fa3ef9bc781b7ac22c3803bc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d057c2da4e156b6fee96bbbc7530fc6e4e5ec0e3cca758cd4ad56b383aa1c853`

```dockerfile
```

-	Layers:
	-	`sha256:bcf1cc90e51943acc8378004179404e8764fa3100f9da307356624fc646ac2e4`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5` - linux; ppc64le

```console
$ docker pull varnish@sha256:c63d68ac4edf4f9e85b41869e7a4ea1eabc3c3842b80a49440dbff4d90832ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136725124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cad6d46c54e6e579cde8f2d936ca9d971abfcda21f2591cdb79f5366871c39`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace8d768f1dade09fd3e91c83643659521032a1e92c02c0da8337ff66dee64b8`  
		Last Modified: Tue, 14 Jan 2025 05:22:23 GMT  
		Size: 104.7 MB (104678242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5141099321bb7ae35a96b984a4a20890824469d1f5018314ada77330e5748773`  
		Last Modified: Tue, 14 Jan 2025 05:22:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e62327219f02684eb6825d4ccdeae9e2ee7a95ed7a734114d6a341b57270d2`  
		Last Modified: Tue, 14 Jan 2025 05:22:20 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5` - unknown; unknown

```console
$ docker pull varnish@sha256:7e548236caca225ed5934d475c24ed217cf64885731a42e7e0cf729e538a6d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d35a6420e9e107b9084c8eb162d3cffc7f0178652f81dea7b637bf59a007974`

```dockerfile
```

-	Layers:
	-	`sha256:883e131f1e31ad90f3f2a7df1f85af292546026a8bf028b83977ccd5aaea37d6`  
		Last Modified: Tue, 14 Jan 2025 05:22:20 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5` - linux; s390x

```console
$ docker pull varnish@sha256:2d4583d536538799c8f25830d5bdee68f9f7703af927258252ee299787230d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111830956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca6a38fa7276d88267ff99384340cfc22e1ea21d63be9bf90375397d05a64c7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d12c8908d8b5e548aec881ce0406a770ed81368a86ef8517ba94d60c08f1e9f`  
		Last Modified: Tue, 14 Jan 2025 04:56:17 GMT  
		Size: 85.0 MB (84970183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2af03bf9135b8db4cd872ed5c313f5ceed5e29c99894a869316bb638a28b4c`  
		Last Modified: Tue, 14 Jan 2025 04:56:15 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93263ea9e4852d61c6a835a306352bae82471d357d8a27bfc75abc7ff9c7e92c`  
		Last Modified: Tue, 14 Jan 2025 04:56:15 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5` - unknown; unknown

```console
$ docker pull varnish@sha256:02c5bd30f948dfb748a66134376d29daa8bf6213f2dabf6d3ecfa7d8685b3296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b96bccf27e617aac980f69a15dddbb1fc84317f62f651e73929e17c391d777`

```dockerfile
```

-	Layers:
	-	`sha256:a5f4145b839dd98ff7ef445bd10ffb4a3c2cac5d51c80d64c040b68196f4204e`  
		Last Modified: Tue, 14 Jan 2025 04:56:15 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.5-alpine`

```console
$ docker pull varnish@sha256:89f543a45e065043a3f68ef5484032fc9193bb07ea0b8c743fe0c9428a3ef7ca
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
$ docker pull varnish@sha256:341b855a7562eb1d04d9d603ad4fffbc7669fc2a965fe8acf239d5c26fd28a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73218172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea286037dc158224459d418685572d5d09358502baf739de42009b22220fc77`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de97c78fb86cc03363e31797a2ee46200ad84519bb172e342c29aba6e07dfc0a`  
		Last Modified: Wed, 08 Jan 2025 18:10:15 GMT  
		Size: 69.8 MB (69795887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d78790b7f984baf3d970ee734e8d653dc3a30b7d00d0d4f7924f9476d402e8`  
		Last Modified: Wed, 08 Jan 2025 18:10:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9584ea80c9931437eda67089d6419bc64c1286736349bb9e3ac4cf7a3b229cd`  
		Last Modified: Wed, 08 Jan 2025 18:10:14 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a41d906bb50ef9f906950563d4c349cb4ee8c00f374ebf7c4e05714f93722539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b23ef427dc91faa8c1c6e2f1fdd14798fd6f948654d3de43d0b8e77ed9a50f6`

```dockerfile
```

-	Layers:
	-	`sha256:5427e28af6fef77db34da4b02b74576cb2df6b873be7e3e85eb3d29ea1437685`  
		Last Modified: Wed, 08 Jan 2025 18:10:14 GMT  
		Size: 18.8 KB (18763 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6d7864af6574ea9416bfd0f53336eafae86d33abfe0b46325e3829645a82279e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57420453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d4958b6c35f9c50acaed67b229eb124c708485b659f89863a8cb28fcbb76d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-armv7.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:a7e7294636d65e1e64be6d2a9e772d5c14442ce00c5a9d8d2fa587f09b5ece5c`  
		Last Modified: Wed, 08 Jan 2025 17:34:28 GMT  
		Size: 2.9 MB (2928493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d675b62f999bd70d6f7109ae83f0c587fb30c88e33fe61576ec99bed479b76c`  
		Last Modified: Wed, 08 Jan 2025 21:58:32 GMT  
		Size: 54.5 MB (54489915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377da637b70832463cabf407f8f7b3498baf84045afc7d7405879e07b121d35`  
		Last Modified: Wed, 08 Jan 2025 21:58:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6a07633aedab7dc1a4e501bf2f58bc0579f2350c418a31ea94bb6a0dfa3f14`  
		Last Modified: Wed, 08 Jan 2025 21:58:30 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a1bbf35e981b26f35976863f460dcf1031ce2f62427393ebdb361f2a7412506f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d56af7896b15516643a5ed917b4ebddf7432bded26e5af5bec735e325f3a943`

```dockerfile
```

-	Layers:
	-	`sha256:b7e5c45eba453f1b8862efb18fa3bb025f65351a47e7b312b1f6a45e5cad69ea`  
		Last Modified: Wed, 08 Jan 2025 21:58:30 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:30773f624f1e63023f73dfbba41e2882f4195aa1110f4413c85868c2b9645fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69925040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ee5046044834745bfcc1b7358de9e33fc5ae4e355cf371fef3cbce93f152f5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632054204c85a7143bd6fef15934e51228f04590e41565899d022be015f9191a`  
		Last Modified: Wed, 08 Jan 2025 22:11:23 GMT  
		Size: 66.6 MB (66562470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c0ecc0c6da66aa12545fd7af08e44da04b79702e1941ada9288cc07980a019`  
		Last Modified: Wed, 08 Jan 2025 22:11:20 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795187b75748cf54b0f558c3d7c16ae6ee13ae0e4def40c529ee65f35e0e5156`  
		Last Modified: Wed, 08 Jan 2025 22:11:20 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:56738ad0a92281302d414a21d953aa86b44deddd103d3d93d35c5a91489f9061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448897dd7f5eecd0a78b9338b0b6dabf5673d2299f6b8ab461edaaa56bf5901c`

```dockerfile
```

-	Layers:
	-	`sha256:c7a30de62a515d733b93c7b4eef43870481779121aefc8145b293942abe638db`  
		Last Modified: Wed, 08 Jan 2025 22:11:20 GMT  
		Size: 18.9 KB (18855 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5-alpine` - linux; 386

```console
$ docker pull varnish@sha256:9280770dd8c821b055e1171d823cc442e54a5a81606490a1a8c69f92c118ebff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75242237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0df770d763e39304212ce2b6776095229aaaf6f707c6ec35fa7d26520565092`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-x86.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:ae1d9a0eea37f9fb4394d27e83eb58694cd0a74025c8c135051300a330d76686`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.3 MB (3254296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565cb2a1d37b16c7cb73a5aea454bb6d637b2f0943f771b99cb6e4714448864c`  
		Last Modified: Wed, 08 Jan 2025 18:09:41 GMT  
		Size: 72.0 MB (71985901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a0e7967b42329e3d8b18fffcc5a8b48af05a6aa753e6cf0dcc15ef7a66e3b0`  
		Last Modified: Wed, 08 Jan 2025 18:09:38 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f4edd72a9da4f744a160ae7a8512192b0df34998a056bdc823b071e4eedd74`  
		Last Modified: Wed, 08 Jan 2025 18:09:39 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4ae2d31b7c6ab1e843e7475a48708d350e2a8427d3f33bdcbcd1a26e4bcb4999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5936b0e9be21e205ae60ef7e55120f1a02e6999ce6cd6899b945209d12d05ea`

```dockerfile
```

-	Layers:
	-	`sha256:c8ac87c90a88eb7e9b9957dcabd34a9aa1a1d184ec45c787ab57a0e86293f4de`  
		Last Modified: Wed, 08 Jan 2025 18:09:38 GMT  
		Size: 18.7 KB (18736 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:c0ba51a0f5b95cf795c9dd78c222f5d09936e0560c11b2e181c1f76d2911874c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70751061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205efd7fdfb2a471906d16258df15c898cd62230e155d8f37ea9c4b88374b6ff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-ppc64le.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:a1e53c81da67874250566308d64e6cf88d5d19fb3bdb55484bd7a41b4e42a126`  
		Last Modified: Wed, 08 Jan 2025 17:25:17 GMT  
		Size: 3.4 MB (3365646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c0cf4e3d832e836ec3498619c51b145b51afa395950ccfab417c99655196a3`  
		Last Modified: Wed, 08 Jan 2025 21:36:04 GMT  
		Size: 67.4 MB (67383366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689348f90ccb130675877d0c11a5c7aeebc9c58a30f2d19e289f4f40dae621a1`  
		Last Modified: Wed, 08 Jan 2025 21:36:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f29beff7316441713a23af54a36a9bf723df7079bf968dba903a1e86a2d4a5b`  
		Last Modified: Wed, 08 Jan 2025 21:36:01 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:82a483df9bdbcbe8e16a97eee66659e0b38094aa87c9bd9a098d2a3320c55e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abde29b2971cb4289c0470bf31629c5b1f49ca144a9e4052ef838f41fa9b30fc`

```dockerfile
```

-	Layers:
	-	`sha256:3770a61226ba1c99292a6b3882b0f32204b0758a8473b99e74403642ac1bef3c`  
		Last Modified: Wed, 08 Jan 2025 21:36:01 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:a58b9bf442235ffc294be3fe46cc886b9e641bc97ad4c8af88c6edc70920df77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65129234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5edc4e293f8e9c218f5bec0358089d56f55a5d98e6de772bec65a50ce683f29`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-s390x.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:be00939408ff94e4fec4588babdfc5d58c5d13d897e8cc5dda295b4a6253bfa9`  
		Last Modified: Wed, 08 Jan 2025 17:26:42 GMT  
		Size: 3.3 MB (3254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fb86a50486c3cbf360ddde20ea4bdf6f9bb868eb4fceb02b50bf86c5261b8a`  
		Last Modified: Wed, 08 Jan 2025 22:13:42 GMT  
		Size: 61.9 MB (61872941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775827bcd8189eea66566ffa6022995a34cb53b3e0d05a687de101f359fa4253`  
		Last Modified: Wed, 08 Jan 2025 22:13:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ea03c68cf47aec14da5f72a5cf4615265bab6aaaf2db5baa02ed8dec3cbcd9`  
		Last Modified: Wed, 08 Jan 2025 22:13:42 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:16cc7563d6c3d904a1171691862f0e6853c16f0bf6e0dc0c93236633c57231f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc334713869b42dcf283dda157003cbc42a615d9ef1a06b8c517a98d09d2c42`

```dockerfile
```

-	Layers:
	-	`sha256:1e41947d2117ddd56c851c4575cd6166f22339814a43af8b6e6450ba8f4e35f0`  
		Last Modified: Wed, 08 Jan 2025 22:13:41 GMT  
		Size: 18.8 KB (18762 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.5.0`

```console
$ docker pull varnish@sha256:1a667bcd6b64099acbd075b1c347393e3cdb7f76d0b054209ed5bd015142a72a
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

### `varnish:7.5.0` - linux; amd64

```console
$ docker pull varnish@sha256:9f8e5099ebe0d8c36e5275c92ac41941ac656b81ee99b2242f1bfd2eccf7a870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133947580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0ce3671cc93cda6b4fda1720db7d6f8f58c1f10ad062a16115db45009d2d8d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da20651324383642e77305fdc8e5ee80e40ed9110f7f7fa3a44ca0124caf6b`  
		Last Modified: Tue, 04 Feb 2025 04:26:04 GMT  
		Size: 105.7 MB (105733248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2958af66e2a26b4907cb4ac12a284d9c9037bb0675929e18c0684a07e175f3d4`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18fc8b1264f71a4e5fc52f2bc6e74d64d699c1b0450cf6ce424accae804cc05`  
		Last Modified: Tue, 04 Feb 2025 04:26:03 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0` - unknown; unknown

```console
$ docker pull varnish@sha256:1a5278c3c63de014ce017013bea0011b075c54752ff654276b6eab53026a8e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c3c464581b3f712bbb05dc82764f731c8f5c3ad4549e044e17ecaa7787d902`

```dockerfile
```

-	Layers:
	-	`sha256:b177209b0f766e9795f77d086a175574726188b79051e0e465987a5054710e81`  
		Last Modified: Tue, 04 Feb 2025 04:26:03 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5ea210e09979ca90b9deec1fbedb8695639ecbbb2979143fc3f424b4ad3e6e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104301434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34cb2867fc13015905b8fc0ae4f3e62435aafbca1d250855f0ddf48526fb39a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322188f9e166a922611c24675a020e8057d7fcf53d1053f2bb283b525bde340`  
		Last Modified: Tue, 14 Jan 2025 08:55:13 GMT  
		Size: 80.4 MB (80384802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7e54d0742912b656895a8c84766fd91aee92e87a36cf75770454fadae3cbc4`  
		Last Modified: Tue, 14 Jan 2025 08:55:11 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79c9133be42fc73eb284dce8bb90c975d2c44a550a7778ab14eaf7a2cf5bf6b`  
		Last Modified: Tue, 14 Jan 2025 08:55:11 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0` - unknown; unknown

```console
$ docker pull varnish@sha256:ed97e9ab2ba172f200ba9c78efb63d471ab67092172c33a2913f12d0885ae4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429c83cdc91ff1a0749468e28c605f6cddfab32508e1f07c6eb1282c0e9bc38b`

```dockerfile
```

-	Layers:
	-	`sha256:9f3449d9df625d81759852b8bb625b472977d62d8778b8d6e819cd48ccfd91cb`  
		Last Modified: Tue, 14 Jan 2025 08:55:11 GMT  
		Size: 18.9 KB (18869 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:fe9080130f5fb29baf07e52379a26bc14c30d9cf32979d78cd13d18013ef2254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128228781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7833533f9bcb4c5d332a1a3ade7827bc08c8029967d977581b87606e12d21596`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636e5cc10fbd69609472b5804793d18f5073426b3ff433573f8f3a5eb65f589f`  
		Last Modified: Tue, 14 Jan 2025 06:57:14 GMT  
		Size: 100.2 MB (100185716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dbc759d0ab91f3b54dbde468018717fa687e97be39ac824438c273df06e476`  
		Last Modified: Tue, 14 Jan 2025 06:57:11 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a998e2ce147a4d194fda8e8e26e48a60c2ead365dcac624740112ccadd67132`  
		Last Modified: Tue, 14 Jan 2025 06:57:11 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0` - unknown; unknown

```console
$ docker pull varnish@sha256:b429375d48b4f8f6f126178bf3bf93225f5803ca4c3aae6452e79509d4e32748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e64caa2ca00763e0182119c7e8d62ee25cbaf4f3e16bcf893f0e61e83b4931`

```dockerfile
```

-	Layers:
	-	`sha256:3cdcdb448e5aace0ba34f93e85edcba0b777a79f5b853069f3ecf2a992bb806b`  
		Last Modified: Tue, 14 Jan 2025 06:57:11 GMT  
		Size: 18.9 KB (18896 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0` - linux; 386

```console
$ docker pull varnish@sha256:32961a84374f32ce335c3c2ddc6b9b654c8dceb2681ee77352fd1b1bf8c2a4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131058305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6590994ca1a7c60f38f951597dff1f567e90c921411c9d25f7ea0a2362a5e00`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31381739b1cf1d2013ab05495584256c14f70ff0690459179356fb415eaace20`  
		Last Modified: Tue, 04 Feb 2025 04:26:04 GMT  
		Size: 101.9 MB (101868816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22882845a4dd3b8960abc19f5cbbfbae10af74e6657d93ee64322171a1138aba`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63cfb1491d67d2f05f2d7991a2b1800d36bbda089293f6659a0b8b489e95c60`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0` - unknown; unknown

```console
$ docker pull varnish@sha256:95bb88de67b2a8eafd754aad33701a7e7ebf11fa3ef9bc781b7ac22c3803bc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d057c2da4e156b6fee96bbbc7530fc6e4e5ec0e3cca758cd4ad56b383aa1c853`

```dockerfile
```

-	Layers:
	-	`sha256:bcf1cc90e51943acc8378004179404e8764fa3100f9da307356624fc646ac2e4`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:c63d68ac4edf4f9e85b41869e7a4ea1eabc3c3842b80a49440dbff4d90832ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136725124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cad6d46c54e6e579cde8f2d936ca9d971abfcda21f2591cdb79f5366871c39`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace8d768f1dade09fd3e91c83643659521032a1e92c02c0da8337ff66dee64b8`  
		Last Modified: Tue, 14 Jan 2025 05:22:23 GMT  
		Size: 104.7 MB (104678242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5141099321bb7ae35a96b984a4a20890824469d1f5018314ada77330e5748773`  
		Last Modified: Tue, 14 Jan 2025 05:22:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e62327219f02684eb6825d4ccdeae9e2ee7a95ed7a734114d6a341b57270d2`  
		Last Modified: Tue, 14 Jan 2025 05:22:20 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0` - unknown; unknown

```console
$ docker pull varnish@sha256:7e548236caca225ed5934d475c24ed217cf64885731a42e7e0cf729e538a6d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d35a6420e9e107b9084c8eb162d3cffc7f0178652f81dea7b637bf59a007974`

```dockerfile
```

-	Layers:
	-	`sha256:883e131f1e31ad90f3f2a7df1f85af292546026a8bf028b83977ccd5aaea37d6`  
		Last Modified: Tue, 14 Jan 2025 05:22:20 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0` - linux; s390x

```console
$ docker pull varnish@sha256:2d4583d536538799c8f25830d5bdee68f9f7703af927258252ee299787230d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111830956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca6a38fa7276d88267ff99384340cfc22e1ea21d63be9bf90375397d05a64c7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d12c8908d8b5e548aec881ce0406a770ed81368a86ef8517ba94d60c08f1e9f`  
		Last Modified: Tue, 14 Jan 2025 04:56:17 GMT  
		Size: 85.0 MB (84970183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2af03bf9135b8db4cd872ed5c313f5ceed5e29c99894a869316bb638a28b4c`  
		Last Modified: Tue, 14 Jan 2025 04:56:15 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93263ea9e4852d61c6a835a306352bae82471d357d8a27bfc75abc7ff9c7e92c`  
		Last Modified: Tue, 14 Jan 2025 04:56:15 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0` - unknown; unknown

```console
$ docker pull varnish@sha256:02c5bd30f948dfb748a66134376d29daa8bf6213f2dabf6d3ecfa7d8685b3296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b96bccf27e617aac980f69a15dddbb1fc84317f62f651e73929e17c391d777`

```dockerfile
```

-	Layers:
	-	`sha256:a5f4145b839dd98ff7ef445bd10ffb4a3c2cac5d51c80d64c040b68196f4204e`  
		Last Modified: Tue, 14 Jan 2025 04:56:15 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.5.0-alpine`

```console
$ docker pull varnish@sha256:89f543a45e065043a3f68ef5484032fc9193bb07ea0b8c743fe0c9428a3ef7ca
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
$ docker pull varnish@sha256:341b855a7562eb1d04d9d603ad4fffbc7669fc2a965fe8acf239d5c26fd28a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73218172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea286037dc158224459d418685572d5d09358502baf739de42009b22220fc77`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de97c78fb86cc03363e31797a2ee46200ad84519bb172e342c29aba6e07dfc0a`  
		Last Modified: Wed, 08 Jan 2025 18:10:15 GMT  
		Size: 69.8 MB (69795887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d78790b7f984baf3d970ee734e8d653dc3a30b7d00d0d4f7924f9476d402e8`  
		Last Modified: Wed, 08 Jan 2025 18:10:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9584ea80c9931437eda67089d6419bc64c1286736349bb9e3ac4cf7a3b229cd`  
		Last Modified: Wed, 08 Jan 2025 18:10:14 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a41d906bb50ef9f906950563d4c349cb4ee8c00f374ebf7c4e05714f93722539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b23ef427dc91faa8c1c6e2f1fdd14798fd6f948654d3de43d0b8e77ed9a50f6`

```dockerfile
```

-	Layers:
	-	`sha256:5427e28af6fef77db34da4b02b74576cb2df6b873be7e3e85eb3d29ea1437685`  
		Last Modified: Wed, 08 Jan 2025 18:10:14 GMT  
		Size: 18.8 KB (18763 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6d7864af6574ea9416bfd0f53336eafae86d33abfe0b46325e3829645a82279e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57420453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d4958b6c35f9c50acaed67b229eb124c708485b659f89863a8cb28fcbb76d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-armv7.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:a7e7294636d65e1e64be6d2a9e772d5c14442ce00c5a9d8d2fa587f09b5ece5c`  
		Last Modified: Wed, 08 Jan 2025 17:34:28 GMT  
		Size: 2.9 MB (2928493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d675b62f999bd70d6f7109ae83f0c587fb30c88e33fe61576ec99bed479b76c`  
		Last Modified: Wed, 08 Jan 2025 21:58:32 GMT  
		Size: 54.5 MB (54489915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377da637b70832463cabf407f8f7b3498baf84045afc7d7405879e07b121d35`  
		Last Modified: Wed, 08 Jan 2025 21:58:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6a07633aedab7dc1a4e501bf2f58bc0579f2350c418a31ea94bb6a0dfa3f14`  
		Last Modified: Wed, 08 Jan 2025 21:58:30 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a1bbf35e981b26f35976863f460dcf1031ce2f62427393ebdb361f2a7412506f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d56af7896b15516643a5ed917b4ebddf7432bded26e5af5bec735e325f3a943`

```dockerfile
```

-	Layers:
	-	`sha256:b7e5c45eba453f1b8862efb18fa3bb025f65351a47e7b312b1f6a45e5cad69ea`  
		Last Modified: Wed, 08 Jan 2025 21:58:30 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:30773f624f1e63023f73dfbba41e2882f4195aa1110f4413c85868c2b9645fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69925040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ee5046044834745bfcc1b7358de9e33fc5ae4e355cf371fef3cbce93f152f5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632054204c85a7143bd6fef15934e51228f04590e41565899d022be015f9191a`  
		Last Modified: Wed, 08 Jan 2025 22:11:23 GMT  
		Size: 66.6 MB (66562470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c0ecc0c6da66aa12545fd7af08e44da04b79702e1941ada9288cc07980a019`  
		Last Modified: Wed, 08 Jan 2025 22:11:20 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795187b75748cf54b0f558c3d7c16ae6ee13ae0e4def40c529ee65f35e0e5156`  
		Last Modified: Wed, 08 Jan 2025 22:11:20 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:56738ad0a92281302d414a21d953aa86b44deddd103d3d93d35c5a91489f9061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448897dd7f5eecd0a78b9338b0b6dabf5673d2299f6b8ab461edaaa56bf5901c`

```dockerfile
```

-	Layers:
	-	`sha256:c7a30de62a515d733b93c7b4eef43870481779121aefc8145b293942abe638db`  
		Last Modified: Wed, 08 Jan 2025 22:11:20 GMT  
		Size: 18.9 KB (18855 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:9280770dd8c821b055e1171d823cc442e54a5a81606490a1a8c69f92c118ebff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75242237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0df770d763e39304212ce2b6776095229aaaf6f707c6ec35fa7d26520565092`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-x86.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:ae1d9a0eea37f9fb4394d27e83eb58694cd0a74025c8c135051300a330d76686`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.3 MB (3254296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565cb2a1d37b16c7cb73a5aea454bb6d637b2f0943f771b99cb6e4714448864c`  
		Last Modified: Wed, 08 Jan 2025 18:09:41 GMT  
		Size: 72.0 MB (71985901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a0e7967b42329e3d8b18fffcc5a8b48af05a6aa753e6cf0dcc15ef7a66e3b0`  
		Last Modified: Wed, 08 Jan 2025 18:09:38 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f4edd72a9da4f744a160ae7a8512192b0df34998a056bdc823b071e4eedd74`  
		Last Modified: Wed, 08 Jan 2025 18:09:39 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4ae2d31b7c6ab1e843e7475a48708d350e2a8427d3f33bdcbcd1a26e4bcb4999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5936b0e9be21e205ae60ef7e55120f1a02e6999ce6cd6899b945209d12d05ea`

```dockerfile
```

-	Layers:
	-	`sha256:c8ac87c90a88eb7e9b9957dcabd34a9aa1a1d184ec45c787ab57a0e86293f4de`  
		Last Modified: Wed, 08 Jan 2025 18:09:38 GMT  
		Size: 18.7 KB (18736 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:c0ba51a0f5b95cf795c9dd78c222f5d09936e0560c11b2e181c1f76d2911874c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70751061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205efd7fdfb2a471906d16258df15c898cd62230e155d8f37ea9c4b88374b6ff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-ppc64le.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:a1e53c81da67874250566308d64e6cf88d5d19fb3bdb55484bd7a41b4e42a126`  
		Last Modified: Wed, 08 Jan 2025 17:25:17 GMT  
		Size: 3.4 MB (3365646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c0cf4e3d832e836ec3498619c51b145b51afa395950ccfab417c99655196a3`  
		Last Modified: Wed, 08 Jan 2025 21:36:04 GMT  
		Size: 67.4 MB (67383366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689348f90ccb130675877d0c11a5c7aeebc9c58a30f2d19e289f4f40dae621a1`  
		Last Modified: Wed, 08 Jan 2025 21:36:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f29beff7316441713a23af54a36a9bf723df7079bf968dba903a1e86a2d4a5b`  
		Last Modified: Wed, 08 Jan 2025 21:36:01 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:82a483df9bdbcbe8e16a97eee66659e0b38094aa87c9bd9a098d2a3320c55e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abde29b2971cb4289c0470bf31629c5b1f49ca144a9e4052ef838f41fa9b30fc`

```dockerfile
```

-	Layers:
	-	`sha256:3770a61226ba1c99292a6b3882b0f32204b0758a8473b99e74403642ac1bef3c`  
		Last Modified: Wed, 08 Jan 2025 21:36:01 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.5.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:a58b9bf442235ffc294be3fe46cc886b9e641bc97ad4c8af88c6edc70920df77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65129234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5edc4e293f8e9c218f5bec0358089d56f55a5d98e6de772bec65a50ce683f29`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-s390x.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:be00939408ff94e4fec4588babdfc5d58c5d13d897e8cc5dda295b4a6253bfa9`  
		Last Modified: Wed, 08 Jan 2025 17:26:42 GMT  
		Size: 3.3 MB (3254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fb86a50486c3cbf360ddde20ea4bdf6f9bb868eb4fceb02b50bf86c5261b8a`  
		Last Modified: Wed, 08 Jan 2025 22:13:42 GMT  
		Size: 61.9 MB (61872941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775827bcd8189eea66566ffa6022995a34cb53b3e0d05a687de101f359fa4253`  
		Last Modified: Wed, 08 Jan 2025 22:13:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ea03c68cf47aec14da5f72a5cf4615265bab6aaaf2db5baa02ed8dec3cbcd9`  
		Last Modified: Wed, 08 Jan 2025 22:13:42 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.5.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:16cc7563d6c3d904a1171691862f0e6853c16f0bf6e0dc0c93236633c57231f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc334713869b42dcf283dda157003cbc42a615d9ef1a06b8c517a98d09d2c42`

```dockerfile
```

-	Layers:
	-	`sha256:1e41947d2117ddd56c851c4575cd6166f22339814a43af8b6e6450ba8f4e35f0`  
		Last Modified: Wed, 08 Jan 2025 22:13:41 GMT  
		Size: 18.8 KB (18762 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6`

```console
$ docker pull varnish@sha256:fcc19990b5009e8d6872ecbab103e4e3b5d9e889bdf1d1dc295c185bf4fcb9b7
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
$ docker pull varnish@sha256:b87b0410c06db25d8a1eee7f1b1810c597a92b955351a5d9991a342f2efb01e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134241793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25e7979d0fe2da9c2e24402be0ffd0bd75756b4f02bce8afa7cedcb8ed36650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67ee532e82dfc81655928a069b82485465822cbf5c1542f69c6d34d2faf3648`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 106.0 MB (106027463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2958af66e2a26b4907cb4ac12a284d9c9037bb0675929e18c0684a07e175f3d4`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603feb9d9bd8c46d13cb279a37a354faa7d1121aa86b4f1989264bec05f080db`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:d69f84689c980cbd991fc051a2dcddc9efcc621a36fe697b1146b00b7d3ec696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdd72eff6cae3462e76c0cd730aa70e1172853fe5aa8bb65fb763776d47d370`

```dockerfile
```

-	Layers:
	-	`sha256:2513e43cba4d6a41c4cc145ae8c3232574ebbd10125c541e2160bd5ac987bdb7`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6c6a9f46639e61c0a1f61baf41f9d8745e6427ffb53c78f2dd15c44eee937209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104582434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466337ca1f1fbaace72e6a4643a8c3eec8d2d743e703e0004aefd901006b9cb8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e8b227058e9d3454106b69de6fe66ed17472d316ff1921b311633240d0ec9`  
		Last Modified: Tue, 14 Jan 2025 08:52:00 GMT  
		Size: 80.7 MB (80665801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef606ddc5460ca106eae7ae656ae0cd58d4ed4d51a760fa98f5eee9d2b83956a`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd367c2f86e70c54d56ae1340603abe7796a5009f884f3516a60201fc33811c7`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:db318c923596723ecf0789d3bc89d94eaea463170207a15a7a33b083e86d4a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f348855c155e8e496de72e8473741aa67df417539e48b6a5ff32acbbdd77049e`

```dockerfile
```

-	Layers:
	-	`sha256:041ac58bc5d4000faf092ee1cf0a347606281ab0da8aba370347b562b59e2385`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a1d3ada6bad3845372d3dcf432d32cbfb189e409cedb54d0f1a242e3776fc812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128523233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef025c412b02b3498e4f94b33ec1cada8b72226b953ad58c4ee179766ab4410d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626bc79106fc52a258b19e1b8cf9198fce3c923c7b95da70f12ad8e8f976bcdf`  
		Last Modified: Tue, 14 Jan 2025 06:54:31 GMT  
		Size: 100.5 MB (100480172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2beab08663c7aa35e561cca3ebb41cbc71ebe6de2617385520b1d0628cd7931`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be3e3459e06ed6b1bc3d7dd210e7db3bc4ec94a34345b9b8a6f3bbe00297ac`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:021c3f4b064f7e9cbc08600b787cdc2e5efb3cd884a9cf919c0b7250909904d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3dd6d1d3f06388322d2e9f03601d9d96bc45eb6eaf61b1b8880bdc5b15f7e0`

```dockerfile
```

-	Layers:
	-	`sha256:04bf3117b2f9ac01066455de1fff3460fcd52addba37c0810b20ac0646a2bb0b`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; 386

```console
$ docker pull varnish@sha256:6190cac5d9924878c2b8728f9592099581bb0a3f4d7d381f5f9f529817f5a9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131328178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aec168bc04f7cad8376f43f41a969143996ec48e484f1f4e9f30e3edf1a6738`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e55145e6767f7d9669a44c343e78f5f089496cfe29cb1171ff95a388e8d577b`  
		Last Modified: Tue, 04 Feb 2025 04:39:09 GMT  
		Size: 102.1 MB (102138693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1239ea0306c326a98823d354aa04ba633c23b14acfac4c4b0de83733522813`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833543a02a818ec2d1ea9d4b9e32d0f0222c832893edc139c8c5dbbc63753dd3`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:2b883f256313e43c6503d1000d37cda90cc5d82fa175d2112fa9cd5bebc3c406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c1b5e4fee186a04f342ccc16b9479323d788276943b0ec8375c42cf4684e4a`

```dockerfile
```

-	Layers:
	-	`sha256:644acc248591d721fcfb9b2001687945d76051de597b94c487ede0b73affe070`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; ppc64le

```console
$ docker pull varnish@sha256:023956b82e9a1d9c9bb184334f4b7b9199c66381c24f428c897f5d4a7400474c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137011865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748f3334be11673591b49c72941ef4d1cfa9237427d24bee54a5258588b71aef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bddbff44e0d90b074d9252780960e743d65647400597bdbdb723bd5f9bfe803`  
		Last Modified: Tue, 14 Jan 2025 05:17:46 GMT  
		Size: 105.0 MB (104964983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95ccf741d55e2393a51c73fd89317f3547d5adb7207dbde5537afc3658ae86`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882ddfad3345715772448bcf8f5c45dfe64cbea01e0ea80d3ba7c3b7017ade57`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:ccfa4ec81beea4b85eb4896509d2d04ff65ad6a685b0bc603e2f715d7b928a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa66aabb06da34b938cc62ea7b7a45196de3d0760ad94174a4a248bee7daa84d`

```dockerfile
```

-	Layers:
	-	`sha256:cecd8427a1bfba726b6d75bff2d19dadfce919cd4b4f62886d38f8a4cf02efba`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; s390x

```console
$ docker pull varnish@sha256:e2658e2b46db161c995e14a46b8c86e2b05dc52e2cd75659a137f647a0003ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112112393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0144263695361fa97ddcffd6c3c9e365b173d3762af5d764c3c42cd60689cdc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f774a4d8b78e92bed8a0db33c73b450dcc47592fda460bc69effd0c061b09`  
		Last Modified: Tue, 14 Jan 2025 04:53:05 GMT  
		Size: 85.3 MB (85251621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d03d5f51f4613e32fd2d3b277656f0203dd8009b2f6e316eddcebc5673a33`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3f67992ed74220778b755e60f7b81a6c917eb1adcd846f3f8afacd330ac60`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:0ed1c02bb35bcc48d4ba11375bd017df3aadeba9577ccd32dc79760544ab8cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f9efc6ce720fdc68b64ba55e6b126ded9de51d7b46334bd48b8042023cfd05`

```dockerfile
```

-	Layers:
	-	`sha256:3bca138d1c90f55120aa3f3e4314121ca90f7142456f54a8cc8c7d86640772fd`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6-alpine`

```console
$ docker pull varnish@sha256:9b5e8c88bb7bef1c29cf817d4d1f402f74ff00d3a075e91a955724aae3dbb79f
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
$ docker pull varnish@sha256:16fd26dbb255c2a652256854071c23d01fad26cb12ac4d26087499df439fb8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73505840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d380dea99cc921b87080ebfeea79c6e431ba52dbdc9196b5e55b1b8ae71c49b5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13071719e86df23adb2f6ecf6c55c18aac855d074b8214240002217e612986c1`  
		Last Modified: Wed, 08 Jan 2025 18:09:58 GMT  
		Size: 70.1 MB (70083556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9d5b7f9d16652100fa7245b6868d6996ce50b359576e257a717b27330b6ae`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d588b07acd892aaf65d6b2e19a3e4aed131407e43a2f4422d66703038dc37e`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:611cde6a197c9607883e5fbd8b64e6a64cf1071eecd9aaab307a6812e45def05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc5b12b26ce300632ee579cbe251c28ba1109818d7668df678e537d4ea4c127`

```dockerfile
```

-	Layers:
	-	`sha256:dd777c39e8a6d248795a40b4b01647c8caea28479a1110228e4d78482cdb8284`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7f140daf95d6e623f71ad1260cb33a81e820790da39329a4b8800ffa6d822ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57703582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c826bb7d37807c477283fcd1e5b44db4b96e497356c487e9aa4076ea435e647e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-armv7.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:a7e7294636d65e1e64be6d2a9e772d5c14442ce00c5a9d8d2fa587f09b5ece5c`  
		Last Modified: Wed, 08 Jan 2025 17:34:28 GMT  
		Size: 2.9 MB (2928493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f078b5e82a729479514897fe95bbb82df97dccdada7ad018f8e01fd3f6d130aa`  
		Last Modified: Wed, 08 Jan 2025 21:57:01 GMT  
		Size: 54.8 MB (54773047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7aa6c0f19e73c709554c56dee03e9679cd0ede758e94180850e32bf78bde44`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8e33f61cc03a4a81a723af523fc522d437087b6f7591880d385babf5f3190`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cc983d1e40f1092ee8ea6a2522092b6761ed4fecd8e49846d875a41853e51a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac62ac3d57662ee732c8c45f82e2cbc2ec73bf1e8c51b20073700c0fcc1e5a6`

```dockerfile
```

-	Layers:
	-	`sha256:c8217ea50488d51644c6cca912882fa1423c6a4d223648173b3f908c626588f4`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:34074cdb3faa15d09741acaed66177e0ed458e6d2168d1f978821d220d626457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70210461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462ae8170be93562c8970b277a272ab82d42971c94479c604c87c630da91bcf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38608fdb51d3fd48708d76faee21aabca1429332c418eaa5aecb9e7cab1514a6`  
		Last Modified: Wed, 08 Jan 2025 22:10:02 GMT  
		Size: 66.8 MB (66847886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f06b07c9c87c108a4a14e4a78d95f53b1f6939a6f65fc3c6f3f037d94bb705d`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f178fd795c4878d915832fbed244eb899faf8e19beee9ba9ac65a05f8ebce1ef`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3aba3b310385ff11eeb727e77e64dcf7f82bd8c1c0f0c396ece9d8562c220df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152b986e7e2661302e7596b28577519ec15cd89c9cd0e2cca5345e9850f93a6d`

```dockerfile
```

-	Layers:
	-	`sha256:ec0249217cf0578e145b31673267f9f1204461fcdd783b691c966d15cd5bd8ca`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 19.5 KB (19535 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; 386

```console
$ docker pull varnish@sha256:562434133d630a953b772286ad7a18f3a6696f725538bac875d67b1d76259594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75519686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a01041f2bb795cddf11cbf90e7247ea895989e68d445ec77f572fcb10a46f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-x86.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:ae1d9a0eea37f9fb4394d27e83eb58694cd0a74025c8c135051300a330d76686`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.3 MB (3254296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca213630b7b92898fea67a1d4fa8e80adb1fd6752a74c258e6400f2ee8073f2`  
		Last Modified: Wed, 08 Jan 2025 18:09:24 GMT  
		Size: 72.3 MB (72263349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bb948a2097e791a11fd570256b38c402deba49eae4d1b503a5537f885e2640`  
		Last Modified: Wed, 08 Jan 2025 18:09:21 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0ce85798168ae5deef79998cd0fea7b8e43c5207e21996a3b171d10d0fc4ec`  
		Last Modified: Wed, 08 Jan 2025 18:09:22 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:02a9653f559b15d9f62e59c37b59fce45822cdf0a574ae800ec8dd14bf2e31fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17933e8516c168b812417ff2c683330991d3e332d88eea49140ab9c8208e3099`

```dockerfile
```

-	Layers:
	-	`sha256:eae92baafec8ac7815e691dba3570aaf78e0b26e8afb23073c144ca044d188cc`  
		Last Modified: Wed, 08 Jan 2025 18:09:22 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b1fc8a6e49bc791694301145471985b68e3db986cebc579671457088dbe01b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d860b944fabe69b38f9241e520add98d86f8960c863c3ef04d76b6a2f5fd565c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-ppc64le.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:a1e53c81da67874250566308d64e6cf88d5d19fb3bdb55484bd7a41b4e42a126`  
		Last Modified: Wed, 08 Jan 2025 17:25:17 GMT  
		Size: 3.4 MB (3365646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2111caeab3d6550f1541b2aab62aa965d120f846336fcc65ae456a7261e0c092`  
		Last Modified: Wed, 08 Jan 2025 21:34:09 GMT  
		Size: 67.7 MB (67651734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e692af43ad518d0382cf5d2d720883b138934bcf4483540844d6ce2153d1c5b0`  
		Last Modified: Wed, 08 Jan 2025 21:34:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ae4b72f995f49677d04483a1483cd93454e4da829d4f2351c16cd29a9d4f91`  
		Last Modified: Wed, 08 Jan 2025 21:34:06 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5b08d61c40c1c8b3dd5d096cb8df59f0856de70e8a224ddf1b81c5f169975b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46aed5daaa83a08599696d8af042202221bdad6fc459e71096b1547dfb5c42f`

```dockerfile
```

-	Layers:
	-	`sha256:fe733115ad499f835228ad84a88a546714d82faa5beefe99c0a9613194296c8e`  
		Last Modified: Wed, 08 Jan 2025 21:34:05 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:cbb99c922969b843858afdac637caf34f7b745f77932ba94c1afbc194ec375ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65409956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9aa429d3cdb829a494d0b32b6d4004c86a23bbe48504352543aaddafd598e48`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-s390x.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:be00939408ff94e4fec4588babdfc5d58c5d13d897e8cc5dda295b4a6253bfa9`  
		Last Modified: Wed, 08 Jan 2025 17:26:42 GMT  
		Size: 3.3 MB (3254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454b6c666851ba2830e7e659674a9de36b79ca58087a4f9391bb6386c7a814a7`  
		Last Modified: Thu, 09 Jan 2025 07:15:53 GMT  
		Size: 62.2 MB (62153663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b2648b66c6f9626b79ab5954fcab817c10ad4ba6cc30627e0b6f03b9fcaba0`  
		Last Modified: Thu, 09 Jan 2025 07:15:51 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c713504fc9938345c4ddcb6a272dfe45cfda2f8bd952585de4a547f3b75a4d`  
		Last Modified: Thu, 09 Jan 2025 07:15:52 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2bee6a7927d1feed9abe45371c406102aa29847d8667017aad9d7187e1221710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca87ce880e71616e91f4545b11e60df4f30361803d9f06aea0ba84fdc2d5b1c`

```dockerfile
```

-	Layers:
	-	`sha256:ebb911b842dfb2bf726c36bd843d710c5cc80779fe83eabb56e1cbdb23588262`  
		Last Modified: Thu, 09 Jan 2025 07:15:51 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.1`

```console
$ docker pull varnish@sha256:fcc19990b5009e8d6872ecbab103e4e3b5d9e889bdf1d1dc295c185bf4fcb9b7
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
$ docker pull varnish@sha256:b87b0410c06db25d8a1eee7f1b1810c597a92b955351a5d9991a342f2efb01e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134241793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25e7979d0fe2da9c2e24402be0ffd0bd75756b4f02bce8afa7cedcb8ed36650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67ee532e82dfc81655928a069b82485465822cbf5c1542f69c6d34d2faf3648`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 106.0 MB (106027463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2958af66e2a26b4907cb4ac12a284d9c9037bb0675929e18c0684a07e175f3d4`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603feb9d9bd8c46d13cb279a37a354faa7d1121aa86b4f1989264bec05f080db`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:d69f84689c980cbd991fc051a2dcddc9efcc621a36fe697b1146b00b7d3ec696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdd72eff6cae3462e76c0cd730aa70e1172853fe5aa8bb65fb763776d47d370`

```dockerfile
```

-	Layers:
	-	`sha256:2513e43cba4d6a41c4cc145ae8c3232574ebbd10125c541e2160bd5ac987bdb7`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6c6a9f46639e61c0a1f61baf41f9d8745e6427ffb53c78f2dd15c44eee937209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104582434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466337ca1f1fbaace72e6a4643a8c3eec8d2d743e703e0004aefd901006b9cb8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e8b227058e9d3454106b69de6fe66ed17472d316ff1921b311633240d0ec9`  
		Last Modified: Tue, 14 Jan 2025 08:52:00 GMT  
		Size: 80.7 MB (80665801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef606ddc5460ca106eae7ae656ae0cd58d4ed4d51a760fa98f5eee9d2b83956a`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd367c2f86e70c54d56ae1340603abe7796a5009f884f3516a60201fc33811c7`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:db318c923596723ecf0789d3bc89d94eaea463170207a15a7a33b083e86d4a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f348855c155e8e496de72e8473741aa67df417539e48b6a5ff32acbbdd77049e`

```dockerfile
```

-	Layers:
	-	`sha256:041ac58bc5d4000faf092ee1cf0a347606281ab0da8aba370347b562b59e2385`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a1d3ada6bad3845372d3dcf432d32cbfb189e409cedb54d0f1a242e3776fc812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128523233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef025c412b02b3498e4f94b33ec1cada8b72226b953ad58c4ee179766ab4410d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626bc79106fc52a258b19e1b8cf9198fce3c923c7b95da70f12ad8e8f976bcdf`  
		Last Modified: Tue, 14 Jan 2025 06:54:31 GMT  
		Size: 100.5 MB (100480172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2beab08663c7aa35e561cca3ebb41cbc71ebe6de2617385520b1d0628cd7931`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be3e3459e06ed6b1bc3d7dd210e7db3bc4ec94a34345b9b8a6f3bbe00297ac`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:021c3f4b064f7e9cbc08600b787cdc2e5efb3cd884a9cf919c0b7250909904d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3dd6d1d3f06388322d2e9f03601d9d96bc45eb6eaf61b1b8880bdc5b15f7e0`

```dockerfile
```

-	Layers:
	-	`sha256:04bf3117b2f9ac01066455de1fff3460fcd52addba37c0810b20ac0646a2bb0b`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; 386

```console
$ docker pull varnish@sha256:6190cac5d9924878c2b8728f9592099581bb0a3f4d7d381f5f9f529817f5a9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131328178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aec168bc04f7cad8376f43f41a969143996ec48e484f1f4e9f30e3edf1a6738`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e55145e6767f7d9669a44c343e78f5f089496cfe29cb1171ff95a388e8d577b`  
		Last Modified: Tue, 04 Feb 2025 04:39:09 GMT  
		Size: 102.1 MB (102138693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1239ea0306c326a98823d354aa04ba633c23b14acfac4c4b0de83733522813`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833543a02a818ec2d1ea9d4b9e32d0f0222c832893edc139c8c5dbbc63753dd3`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:2b883f256313e43c6503d1000d37cda90cc5d82fa175d2112fa9cd5bebc3c406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c1b5e4fee186a04f342ccc16b9479323d788276943b0ec8375c42cf4684e4a`

```dockerfile
```

-	Layers:
	-	`sha256:644acc248591d721fcfb9b2001687945d76051de597b94c487ede0b73affe070`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; ppc64le

```console
$ docker pull varnish@sha256:023956b82e9a1d9c9bb184334f4b7b9199c66381c24f428c897f5d4a7400474c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137011865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748f3334be11673591b49c72941ef4d1cfa9237427d24bee54a5258588b71aef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bddbff44e0d90b074d9252780960e743d65647400597bdbdb723bd5f9bfe803`  
		Last Modified: Tue, 14 Jan 2025 05:17:46 GMT  
		Size: 105.0 MB (104964983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95ccf741d55e2393a51c73fd89317f3547d5adb7207dbde5537afc3658ae86`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882ddfad3345715772448bcf8f5c45dfe64cbea01e0ea80d3ba7c3b7017ade57`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:ccfa4ec81beea4b85eb4896509d2d04ff65ad6a685b0bc603e2f715d7b928a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa66aabb06da34b938cc62ea7b7a45196de3d0760ad94174a4a248bee7daa84d`

```dockerfile
```

-	Layers:
	-	`sha256:cecd8427a1bfba726b6d75bff2d19dadfce919cd4b4f62886d38f8a4cf02efba`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1` - linux; s390x

```console
$ docker pull varnish@sha256:e2658e2b46db161c995e14a46b8c86e2b05dc52e2cd75659a137f647a0003ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112112393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0144263695361fa97ddcffd6c3c9e365b173d3762af5d764c3c42cd60689cdc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f774a4d8b78e92bed8a0db33c73b450dcc47592fda460bc69effd0c061b09`  
		Last Modified: Tue, 14 Jan 2025 04:53:05 GMT  
		Size: 85.3 MB (85251621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d03d5f51f4613e32fd2d3b277656f0203dd8009b2f6e316eddcebc5673a33`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3f67992ed74220778b755e60f7b81a6c917eb1adcd846f3f8afacd330ac60`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1` - unknown; unknown

```console
$ docker pull varnish@sha256:0ed1c02bb35bcc48d4ba11375bd017df3aadeba9577ccd32dc79760544ab8cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f9efc6ce720fdc68b64ba55e6b126ded9de51d7b46334bd48b8042023cfd05`

```dockerfile
```

-	Layers:
	-	`sha256:3bca138d1c90f55120aa3f3e4314121ca90f7142456f54a8cc8c7d86640772fd`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.1-alpine`

```console
$ docker pull varnish@sha256:9b5e8c88bb7bef1c29cf817d4d1f402f74ff00d3a075e91a955724aae3dbb79f
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
$ docker pull varnish@sha256:16fd26dbb255c2a652256854071c23d01fad26cb12ac4d26087499df439fb8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73505840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d380dea99cc921b87080ebfeea79c6e431ba52dbdc9196b5e55b1b8ae71c49b5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13071719e86df23adb2f6ecf6c55c18aac855d074b8214240002217e612986c1`  
		Last Modified: Wed, 08 Jan 2025 18:09:58 GMT  
		Size: 70.1 MB (70083556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9d5b7f9d16652100fa7245b6868d6996ce50b359576e257a717b27330b6ae`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d588b07acd892aaf65d6b2e19a3e4aed131407e43a2f4422d66703038dc37e`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:611cde6a197c9607883e5fbd8b64e6a64cf1071eecd9aaab307a6812e45def05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc5b12b26ce300632ee579cbe251c28ba1109818d7668df678e537d4ea4c127`

```dockerfile
```

-	Layers:
	-	`sha256:dd777c39e8a6d248795a40b4b01647c8caea28479a1110228e4d78482cdb8284`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7f140daf95d6e623f71ad1260cb33a81e820790da39329a4b8800ffa6d822ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57703582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c826bb7d37807c477283fcd1e5b44db4b96e497356c487e9aa4076ea435e647e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-armv7.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:a7e7294636d65e1e64be6d2a9e772d5c14442ce00c5a9d8d2fa587f09b5ece5c`  
		Last Modified: Wed, 08 Jan 2025 17:34:28 GMT  
		Size: 2.9 MB (2928493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f078b5e82a729479514897fe95bbb82df97dccdada7ad018f8e01fd3f6d130aa`  
		Last Modified: Wed, 08 Jan 2025 21:57:01 GMT  
		Size: 54.8 MB (54773047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7aa6c0f19e73c709554c56dee03e9679cd0ede758e94180850e32bf78bde44`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8e33f61cc03a4a81a723af523fc522d437087b6f7591880d385babf5f3190`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cc983d1e40f1092ee8ea6a2522092b6761ed4fecd8e49846d875a41853e51a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac62ac3d57662ee732c8c45f82e2cbc2ec73bf1e8c51b20073700c0fcc1e5a6`

```dockerfile
```

-	Layers:
	-	`sha256:c8217ea50488d51644c6cca912882fa1423c6a4d223648173b3f908c626588f4`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:34074cdb3faa15d09741acaed66177e0ed458e6d2168d1f978821d220d626457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70210461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462ae8170be93562c8970b277a272ab82d42971c94479c604c87c630da91bcf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38608fdb51d3fd48708d76faee21aabca1429332c418eaa5aecb9e7cab1514a6`  
		Last Modified: Wed, 08 Jan 2025 22:10:02 GMT  
		Size: 66.8 MB (66847886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f06b07c9c87c108a4a14e4a78d95f53b1f6939a6f65fc3c6f3f037d94bb705d`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f178fd795c4878d915832fbed244eb899faf8e19beee9ba9ac65a05f8ebce1ef`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3aba3b310385ff11eeb727e77e64dcf7f82bd8c1c0f0c396ece9d8562c220df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152b986e7e2661302e7596b28577519ec15cd89c9cd0e2cca5345e9850f93a6d`

```dockerfile
```

-	Layers:
	-	`sha256:ec0249217cf0578e145b31673267f9f1204461fcdd783b691c966d15cd5bd8ca`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 19.5 KB (19535 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; 386

```console
$ docker pull varnish@sha256:562434133d630a953b772286ad7a18f3a6696f725538bac875d67b1d76259594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75519686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a01041f2bb795cddf11cbf90e7247ea895989e68d445ec77f572fcb10a46f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-x86.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:ae1d9a0eea37f9fb4394d27e83eb58694cd0a74025c8c135051300a330d76686`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.3 MB (3254296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca213630b7b92898fea67a1d4fa8e80adb1fd6752a74c258e6400f2ee8073f2`  
		Last Modified: Wed, 08 Jan 2025 18:09:24 GMT  
		Size: 72.3 MB (72263349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bb948a2097e791a11fd570256b38c402deba49eae4d1b503a5537f885e2640`  
		Last Modified: Wed, 08 Jan 2025 18:09:21 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0ce85798168ae5deef79998cd0fea7b8e43c5207e21996a3b171d10d0fc4ec`  
		Last Modified: Wed, 08 Jan 2025 18:09:22 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:02a9653f559b15d9f62e59c37b59fce45822cdf0a574ae800ec8dd14bf2e31fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17933e8516c168b812417ff2c683330991d3e332d88eea49140ab9c8208e3099`

```dockerfile
```

-	Layers:
	-	`sha256:eae92baafec8ac7815e691dba3570aaf78e0b26e8afb23073c144ca044d188cc`  
		Last Modified: Wed, 08 Jan 2025 18:09:22 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b1fc8a6e49bc791694301145471985b68e3db986cebc579671457088dbe01b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d860b944fabe69b38f9241e520add98d86f8960c863c3ef04d76b6a2f5fd565c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-ppc64le.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:a1e53c81da67874250566308d64e6cf88d5d19fb3bdb55484bd7a41b4e42a126`  
		Last Modified: Wed, 08 Jan 2025 17:25:17 GMT  
		Size: 3.4 MB (3365646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2111caeab3d6550f1541b2aab62aa965d120f846336fcc65ae456a7261e0c092`  
		Last Modified: Wed, 08 Jan 2025 21:34:09 GMT  
		Size: 67.7 MB (67651734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e692af43ad518d0382cf5d2d720883b138934bcf4483540844d6ce2153d1c5b0`  
		Last Modified: Wed, 08 Jan 2025 21:34:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ae4b72f995f49677d04483a1483cd93454e4da829d4f2351c16cd29a9d4f91`  
		Last Modified: Wed, 08 Jan 2025 21:34:06 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5b08d61c40c1c8b3dd5d096cb8df59f0856de70e8a224ddf1b81c5f169975b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46aed5daaa83a08599696d8af042202221bdad6fc459e71096b1547dfb5c42f`

```dockerfile
```

-	Layers:
	-	`sha256:fe733115ad499f835228ad84a88a546714d82faa5beefe99c0a9613194296c8e`  
		Last Modified: Wed, 08 Jan 2025 21:34:05 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.1-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:cbb99c922969b843858afdac637caf34f7b745f77932ba94c1afbc194ec375ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65409956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9aa429d3cdb829a494d0b32b6d4004c86a23bbe48504352543aaddafd598e48`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-s390x.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:be00939408ff94e4fec4588babdfc5d58c5d13d897e8cc5dda295b4a6253bfa9`  
		Last Modified: Wed, 08 Jan 2025 17:26:42 GMT  
		Size: 3.3 MB (3254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454b6c666851ba2830e7e659674a9de36b79ca58087a4f9391bb6386c7a814a7`  
		Last Modified: Thu, 09 Jan 2025 07:15:53 GMT  
		Size: 62.2 MB (62153663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b2648b66c6f9626b79ab5954fcab817c10ad4ba6cc30627e0b6f03b9fcaba0`  
		Last Modified: Thu, 09 Jan 2025 07:15:51 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c713504fc9938345c4ddcb6a272dfe45cfda2f8bd952585de4a547f3b75a4d`  
		Last Modified: Thu, 09 Jan 2025 07:15:52 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2bee6a7927d1feed9abe45371c406102aa29847d8667017aad9d7187e1221710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca87ce880e71616e91f4545b11e60df4f30361803d9f06aea0ba84fdc2d5b1c`

```dockerfile
```

-	Layers:
	-	`sha256:ebb911b842dfb2bf726c36bd843d710c5cc80779fe83eabb56e1cbdb23588262`  
		Last Modified: Thu, 09 Jan 2025 07:15:51 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:alpine`

```console
$ docker pull varnish@sha256:9b5e8c88bb7bef1c29cf817d4d1f402f74ff00d3a075e91a955724aae3dbb79f
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
$ docker pull varnish@sha256:16fd26dbb255c2a652256854071c23d01fad26cb12ac4d26087499df439fb8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73505840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d380dea99cc921b87080ebfeea79c6e431ba52dbdc9196b5e55b1b8ae71c49b5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13071719e86df23adb2f6ecf6c55c18aac855d074b8214240002217e612986c1`  
		Last Modified: Wed, 08 Jan 2025 18:09:58 GMT  
		Size: 70.1 MB (70083556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9d5b7f9d16652100fa7245b6868d6996ce50b359576e257a717b27330b6ae`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d588b07acd892aaf65d6b2e19a3e4aed131407e43a2f4422d66703038dc37e`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:611cde6a197c9607883e5fbd8b64e6a64cf1071eecd9aaab307a6812e45def05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc5b12b26ce300632ee579cbe251c28ba1109818d7668df678e537d4ea4c127`

```dockerfile
```

-	Layers:
	-	`sha256:dd777c39e8a6d248795a40b4b01647c8caea28479a1110228e4d78482cdb8284`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7f140daf95d6e623f71ad1260cb33a81e820790da39329a4b8800ffa6d822ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57703582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c826bb7d37807c477283fcd1e5b44db4b96e497356c487e9aa4076ea435e647e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-armv7.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:a7e7294636d65e1e64be6d2a9e772d5c14442ce00c5a9d8d2fa587f09b5ece5c`  
		Last Modified: Wed, 08 Jan 2025 17:34:28 GMT  
		Size: 2.9 MB (2928493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f078b5e82a729479514897fe95bbb82df97dccdada7ad018f8e01fd3f6d130aa`  
		Last Modified: Wed, 08 Jan 2025 21:57:01 GMT  
		Size: 54.8 MB (54773047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7aa6c0f19e73c709554c56dee03e9679cd0ede758e94180850e32bf78bde44`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8e33f61cc03a4a81a723af523fc522d437087b6f7591880d385babf5f3190`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cc983d1e40f1092ee8ea6a2522092b6761ed4fecd8e49846d875a41853e51a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac62ac3d57662ee732c8c45f82e2cbc2ec73bf1e8c51b20073700c0fcc1e5a6`

```dockerfile
```

-	Layers:
	-	`sha256:c8217ea50488d51644c6cca912882fa1423c6a4d223648173b3f908c626588f4`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:34074cdb3faa15d09741acaed66177e0ed458e6d2168d1f978821d220d626457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70210461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462ae8170be93562c8970b277a272ab82d42971c94479c604c87c630da91bcf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38608fdb51d3fd48708d76faee21aabca1429332c418eaa5aecb9e7cab1514a6`  
		Last Modified: Wed, 08 Jan 2025 22:10:02 GMT  
		Size: 66.8 MB (66847886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f06b07c9c87c108a4a14e4a78d95f53b1f6939a6f65fc3c6f3f037d94bb705d`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f178fd795c4878d915832fbed244eb899faf8e19beee9ba9ac65a05f8ebce1ef`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3aba3b310385ff11eeb727e77e64dcf7f82bd8c1c0f0c396ece9d8562c220df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152b986e7e2661302e7596b28577519ec15cd89c9cd0e2cca5345e9850f93a6d`

```dockerfile
```

-	Layers:
	-	`sha256:ec0249217cf0578e145b31673267f9f1204461fcdd783b691c966d15cd5bd8ca`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 19.5 KB (19535 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:562434133d630a953b772286ad7a18f3a6696f725538bac875d67b1d76259594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75519686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a01041f2bb795cddf11cbf90e7247ea895989e68d445ec77f572fcb10a46f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-x86.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:ae1d9a0eea37f9fb4394d27e83eb58694cd0a74025c8c135051300a330d76686`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.3 MB (3254296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca213630b7b92898fea67a1d4fa8e80adb1fd6752a74c258e6400f2ee8073f2`  
		Last Modified: Wed, 08 Jan 2025 18:09:24 GMT  
		Size: 72.3 MB (72263349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bb948a2097e791a11fd570256b38c402deba49eae4d1b503a5537f885e2640`  
		Last Modified: Wed, 08 Jan 2025 18:09:21 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0ce85798168ae5deef79998cd0fea7b8e43c5207e21996a3b171d10d0fc4ec`  
		Last Modified: Wed, 08 Jan 2025 18:09:22 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:02a9653f559b15d9f62e59c37b59fce45822cdf0a574ae800ec8dd14bf2e31fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17933e8516c168b812417ff2c683330991d3e332d88eea49140ab9c8208e3099`

```dockerfile
```

-	Layers:
	-	`sha256:eae92baafec8ac7815e691dba3570aaf78e0b26e8afb23073c144ca044d188cc`  
		Last Modified: Wed, 08 Jan 2025 18:09:22 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b1fc8a6e49bc791694301145471985b68e3db986cebc579671457088dbe01b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d860b944fabe69b38f9241e520add98d86f8960c863c3ef04d76b6a2f5fd565c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-ppc64le.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:a1e53c81da67874250566308d64e6cf88d5d19fb3bdb55484bd7a41b4e42a126`  
		Last Modified: Wed, 08 Jan 2025 17:25:17 GMT  
		Size: 3.4 MB (3365646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2111caeab3d6550f1541b2aab62aa965d120f846336fcc65ae456a7261e0c092`  
		Last Modified: Wed, 08 Jan 2025 21:34:09 GMT  
		Size: 67.7 MB (67651734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e692af43ad518d0382cf5d2d720883b138934bcf4483540844d6ce2153d1c5b0`  
		Last Modified: Wed, 08 Jan 2025 21:34:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ae4b72f995f49677d04483a1483cd93454e4da829d4f2351c16cd29a9d4f91`  
		Last Modified: Wed, 08 Jan 2025 21:34:06 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5b08d61c40c1c8b3dd5d096cb8df59f0856de70e8a224ddf1b81c5f169975b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46aed5daaa83a08599696d8af042202221bdad6fc459e71096b1547dfb5c42f`

```dockerfile
```

-	Layers:
	-	`sha256:fe733115ad499f835228ad84a88a546714d82faa5beefe99c0a9613194296c8e`  
		Last Modified: Wed, 08 Jan 2025 21:34:05 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:cbb99c922969b843858afdac637caf34f7b745f77932ba94c1afbc194ec375ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65409956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9aa429d3cdb829a494d0b32b6d4004c86a23bbe48504352543aaddafd598e48`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-s390x.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:be00939408ff94e4fec4588babdfc5d58c5d13d897e8cc5dda295b4a6253bfa9`  
		Last Modified: Wed, 08 Jan 2025 17:26:42 GMT  
		Size: 3.3 MB (3254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454b6c666851ba2830e7e659674a9de36b79ca58087a4f9391bb6386c7a814a7`  
		Last Modified: Thu, 09 Jan 2025 07:15:53 GMT  
		Size: 62.2 MB (62153663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b2648b66c6f9626b79ab5954fcab817c10ad4ba6cc30627e0b6f03b9fcaba0`  
		Last Modified: Thu, 09 Jan 2025 07:15:51 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c713504fc9938345c4ddcb6a272dfe45cfda2f8bd952585de4a547f3b75a4d`  
		Last Modified: Thu, 09 Jan 2025 07:15:52 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2bee6a7927d1feed9abe45371c406102aa29847d8667017aad9d7187e1221710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca87ce880e71616e91f4545b11e60df4f30361803d9f06aea0ba84fdc2d5b1c`

```dockerfile
```

-	Layers:
	-	`sha256:ebb911b842dfb2bf726c36bd843d710c5cc80779fe83eabb56e1cbdb23588262`  
		Last Modified: Thu, 09 Jan 2025 07:15:51 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:fcc19990b5009e8d6872ecbab103e4e3b5d9e889bdf1d1dc295c185bf4fcb9b7
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
$ docker pull varnish@sha256:b87b0410c06db25d8a1eee7f1b1810c597a92b955351a5d9991a342f2efb01e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134241793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25e7979d0fe2da9c2e24402be0ffd0bd75756b4f02bce8afa7cedcb8ed36650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67ee532e82dfc81655928a069b82485465822cbf5c1542f69c6d34d2faf3648`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 106.0 MB (106027463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2958af66e2a26b4907cb4ac12a284d9c9037bb0675929e18c0684a07e175f3d4`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603feb9d9bd8c46d13cb279a37a354faa7d1121aa86b4f1989264bec05f080db`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:d69f84689c980cbd991fc051a2dcddc9efcc621a36fe697b1146b00b7d3ec696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdd72eff6cae3462e76c0cd730aa70e1172853fe5aa8bb65fb763776d47d370`

```dockerfile
```

-	Layers:
	-	`sha256:2513e43cba4d6a41c4cc145ae8c3232574ebbd10125c541e2160bd5ac987bdb7`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6c6a9f46639e61c0a1f61baf41f9d8745e6427ffb53c78f2dd15c44eee937209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104582434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466337ca1f1fbaace72e6a4643a8c3eec8d2d743e703e0004aefd901006b9cb8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e8b227058e9d3454106b69de6fe66ed17472d316ff1921b311633240d0ec9`  
		Last Modified: Tue, 14 Jan 2025 08:52:00 GMT  
		Size: 80.7 MB (80665801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef606ddc5460ca106eae7ae656ae0cd58d4ed4d51a760fa98f5eee9d2b83956a`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd367c2f86e70c54d56ae1340603abe7796a5009f884f3516a60201fc33811c7`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:db318c923596723ecf0789d3bc89d94eaea463170207a15a7a33b083e86d4a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f348855c155e8e496de72e8473741aa67df417539e48b6a5ff32acbbdd77049e`

```dockerfile
```

-	Layers:
	-	`sha256:041ac58bc5d4000faf092ee1cf0a347606281ab0da8aba370347b562b59e2385`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a1d3ada6bad3845372d3dcf432d32cbfb189e409cedb54d0f1a242e3776fc812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128523233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef025c412b02b3498e4f94b33ec1cada8b72226b953ad58c4ee179766ab4410d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626bc79106fc52a258b19e1b8cf9198fce3c923c7b95da70f12ad8e8f976bcdf`  
		Last Modified: Tue, 14 Jan 2025 06:54:31 GMT  
		Size: 100.5 MB (100480172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2beab08663c7aa35e561cca3ebb41cbc71ebe6de2617385520b1d0628cd7931`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be3e3459e06ed6b1bc3d7dd210e7db3bc4ec94a34345b9b8a6f3bbe00297ac`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:021c3f4b064f7e9cbc08600b787cdc2e5efb3cd884a9cf919c0b7250909904d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3dd6d1d3f06388322d2e9f03601d9d96bc45eb6eaf61b1b8880bdc5b15f7e0`

```dockerfile
```

-	Layers:
	-	`sha256:04bf3117b2f9ac01066455de1fff3460fcd52addba37c0810b20ac0646a2bb0b`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:6190cac5d9924878c2b8728f9592099581bb0a3f4d7d381f5f9f529817f5a9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131328178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aec168bc04f7cad8376f43f41a969143996ec48e484f1f4e9f30e3edf1a6738`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e55145e6767f7d9669a44c343e78f5f089496cfe29cb1171ff95a388e8d577b`  
		Last Modified: Tue, 04 Feb 2025 04:39:09 GMT  
		Size: 102.1 MB (102138693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1239ea0306c326a98823d354aa04ba633c23b14acfac4c4b0de83733522813`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833543a02a818ec2d1ea9d4b9e32d0f0222c832893edc139c8c5dbbc63753dd3`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:2b883f256313e43c6503d1000d37cda90cc5d82fa175d2112fa9cd5bebc3c406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c1b5e4fee186a04f342ccc16b9479323d788276943b0ec8375c42cf4684e4a`

```dockerfile
```

-	Layers:
	-	`sha256:644acc248591d721fcfb9b2001687945d76051de597b94c487ede0b73affe070`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:023956b82e9a1d9c9bb184334f4b7b9199c66381c24f428c897f5d4a7400474c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137011865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748f3334be11673591b49c72941ef4d1cfa9237427d24bee54a5258588b71aef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bddbff44e0d90b074d9252780960e743d65647400597bdbdb723bd5f9bfe803`  
		Last Modified: Tue, 14 Jan 2025 05:17:46 GMT  
		Size: 105.0 MB (104964983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95ccf741d55e2393a51c73fd89317f3547d5adb7207dbde5537afc3658ae86`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882ddfad3345715772448bcf8f5c45dfe64cbea01e0ea80d3ba7c3b7017ade57`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:ccfa4ec81beea4b85eb4896509d2d04ff65ad6a685b0bc603e2f715d7b928a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa66aabb06da34b938cc62ea7b7a45196de3d0760ad94174a4a248bee7daa84d`

```dockerfile
```

-	Layers:
	-	`sha256:cecd8427a1bfba726b6d75bff2d19dadfce919cd4b4f62886d38f8a4cf02efba`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:e2658e2b46db161c995e14a46b8c86e2b05dc52e2cd75659a137f647a0003ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112112393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0144263695361fa97ddcffd6c3c9e365b173d3762af5d764c3c42cd60689cdc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f774a4d8b78e92bed8a0db33c73b450dcc47592fda460bc69effd0c061b09`  
		Last Modified: Tue, 14 Jan 2025 04:53:05 GMT  
		Size: 85.3 MB (85251621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d03d5f51f4613e32fd2d3b277656f0203dd8009b2f6e316eddcebc5673a33`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3f67992ed74220778b755e60f7b81a6c917eb1adcd846f3f8afacd330ac60`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:0ed1c02bb35bcc48d4ba11375bd017df3aadeba9577ccd32dc79760544ab8cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f9efc6ce720fdc68b64ba55e6b126ded9de51d7b46334bd48b8042023cfd05`

```dockerfile
```

-	Layers:
	-	`sha256:3bca138d1c90f55120aa3f3e4314121ca90f7142456f54a8cc8c7d86640772fd`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:9b5e8c88bb7bef1c29cf817d4d1f402f74ff00d3a075e91a955724aae3dbb79f
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
$ docker pull varnish@sha256:16fd26dbb255c2a652256854071c23d01fad26cb12ac4d26087499df439fb8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73505840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d380dea99cc921b87080ebfeea79c6e431ba52dbdc9196b5e55b1b8ae71c49b5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13071719e86df23adb2f6ecf6c55c18aac855d074b8214240002217e612986c1`  
		Last Modified: Wed, 08 Jan 2025 18:09:58 GMT  
		Size: 70.1 MB (70083556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9d5b7f9d16652100fa7245b6868d6996ce50b359576e257a717b27330b6ae`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d588b07acd892aaf65d6b2e19a3e4aed131407e43a2f4422d66703038dc37e`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:611cde6a197c9607883e5fbd8b64e6a64cf1071eecd9aaab307a6812e45def05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc5b12b26ce300632ee579cbe251c28ba1109818d7668df678e537d4ea4c127`

```dockerfile
```

-	Layers:
	-	`sha256:dd777c39e8a6d248795a40b4b01647c8caea28479a1110228e4d78482cdb8284`  
		Last Modified: Wed, 08 Jan 2025 18:09:57 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7f140daf95d6e623f71ad1260cb33a81e820790da39329a4b8800ffa6d822ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57703582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c826bb7d37807c477283fcd1e5b44db4b96e497356c487e9aa4076ea435e647e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-armv7.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:a7e7294636d65e1e64be6d2a9e772d5c14442ce00c5a9d8d2fa587f09b5ece5c`  
		Last Modified: Wed, 08 Jan 2025 17:34:28 GMT  
		Size: 2.9 MB (2928493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f078b5e82a729479514897fe95bbb82df97dccdada7ad018f8e01fd3f6d130aa`  
		Last Modified: Wed, 08 Jan 2025 21:57:01 GMT  
		Size: 54.8 MB (54773047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7aa6c0f19e73c709554c56dee03e9679cd0ede758e94180850e32bf78bde44`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8e33f61cc03a4a81a723af523fc522d437087b6f7591880d385babf5f3190`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5cc983d1e40f1092ee8ea6a2522092b6761ed4fecd8e49846d875a41853e51a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac62ac3d57662ee732c8c45f82e2cbc2ec73bf1e8c51b20073700c0fcc1e5a6`

```dockerfile
```

-	Layers:
	-	`sha256:c8217ea50488d51644c6cca912882fa1423c6a4d223648173b3f908c626588f4`  
		Last Modified: Wed, 08 Jan 2025 21:56:59 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:34074cdb3faa15d09741acaed66177e0ed458e6d2168d1f978821d220d626457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70210461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462ae8170be93562c8970b277a272ab82d42971c94479c604c87c630da91bcf0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38608fdb51d3fd48708d76faee21aabca1429332c418eaa5aecb9e7cab1514a6`  
		Last Modified: Wed, 08 Jan 2025 22:10:02 GMT  
		Size: 66.8 MB (66847886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f06b07c9c87c108a4a14e4a78d95f53b1f6939a6f65fc3c6f3f037d94bb705d`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f178fd795c4878d915832fbed244eb899faf8e19beee9ba9ac65a05f8ebce1ef`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:3aba3b310385ff11eeb727e77e64dcf7f82bd8c1c0f0c396ece9d8562c220df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152b986e7e2661302e7596b28577519ec15cd89c9cd0e2cca5345e9850f93a6d`

```dockerfile
```

-	Layers:
	-	`sha256:ec0249217cf0578e145b31673267f9f1204461fcdd783b691c966d15cd5bd8ca`  
		Last Modified: Wed, 08 Jan 2025 22:10:00 GMT  
		Size: 19.5 KB (19535 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:562434133d630a953b772286ad7a18f3a6696f725538bac875d67b1d76259594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75519686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a01041f2bb795cddf11cbf90e7247ea895989e68d445ec77f572fcb10a46f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-x86.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:ae1d9a0eea37f9fb4394d27e83eb58694cd0a74025c8c135051300a330d76686`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.3 MB (3254296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca213630b7b92898fea67a1d4fa8e80adb1fd6752a74c258e6400f2ee8073f2`  
		Last Modified: Wed, 08 Jan 2025 18:09:24 GMT  
		Size: 72.3 MB (72263349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bb948a2097e791a11fd570256b38c402deba49eae4d1b503a5537f885e2640`  
		Last Modified: Wed, 08 Jan 2025 18:09:21 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0ce85798168ae5deef79998cd0fea7b8e43c5207e21996a3b171d10d0fc4ec`  
		Last Modified: Wed, 08 Jan 2025 18:09:22 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:02a9653f559b15d9f62e59c37b59fce45822cdf0a574ae800ec8dd14bf2e31fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17933e8516c168b812417ff2c683330991d3e332d88eea49140ab9c8208e3099`

```dockerfile
```

-	Layers:
	-	`sha256:eae92baafec8ac7815e691dba3570aaf78e0b26e8afb23073c144ca044d188cc`  
		Last Modified: Wed, 08 Jan 2025 18:09:22 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b1fc8a6e49bc791694301145471985b68e3db986cebc579671457088dbe01b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d860b944fabe69b38f9241e520add98d86f8960c863c3ef04d76b6a2f5fd565c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-ppc64le.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:a1e53c81da67874250566308d64e6cf88d5d19fb3bdb55484bd7a41b4e42a126`  
		Last Modified: Wed, 08 Jan 2025 17:25:17 GMT  
		Size: 3.4 MB (3365646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2111caeab3d6550f1541b2aab62aa965d120f846336fcc65ae456a7261e0c092`  
		Last Modified: Wed, 08 Jan 2025 21:34:09 GMT  
		Size: 67.7 MB (67651734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e692af43ad518d0382cf5d2d720883b138934bcf4483540844d6ce2153d1c5b0`  
		Last Modified: Wed, 08 Jan 2025 21:34:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ae4b72f995f49677d04483a1483cd93454e4da829d4f2351c16cd29a9d4f91`  
		Last Modified: Wed, 08 Jan 2025 21:34:06 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5b08d61c40c1c8b3dd5d096cb8df59f0856de70e8a224ddf1b81c5f169975b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46aed5daaa83a08599696d8af042202221bdad6fc459e71096b1547dfb5c42f`

```dockerfile
```

-	Layers:
	-	`sha256:fe733115ad499f835228ad84a88a546714d82faa5beefe99c0a9613194296c8e`  
		Last Modified: Wed, 08 Jan 2025 21:34:05 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:cbb99c922969b843858afdac637caf34f7b745f77932ba94c1afbc194ec375ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65409956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9aa429d3cdb829a494d0b32b6d4004c86a23bbe48504352543aaddafd598e48`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
ADD alpine-minirootfs-3.19.6-s390x.tar.gz / # buildkit
# Sun, 10 Nov 2024 02:42:48 GMT
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
	-	`sha256:be00939408ff94e4fec4588babdfc5d58c5d13d897e8cc5dda295b4a6253bfa9`  
		Last Modified: Wed, 08 Jan 2025 17:26:42 GMT  
		Size: 3.3 MB (3254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454b6c666851ba2830e7e659674a9de36b79ca58087a4f9391bb6386c7a814a7`  
		Last Modified: Thu, 09 Jan 2025 07:15:53 GMT  
		Size: 62.2 MB (62153663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b2648b66c6f9626b79ab5954fcab817c10ad4ba6cc30627e0b6f03b9fcaba0`  
		Last Modified: Thu, 09 Jan 2025 07:15:51 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c713504fc9938345c4ddcb6a272dfe45cfda2f8bd952585de4a547f3b75a4d`  
		Last Modified: Thu, 09 Jan 2025 07:15:52 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2bee6a7927d1feed9abe45371c406102aa29847d8667017aad9d7187e1221710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca87ce880e71616e91f4545b11e60df4f30361803d9f06aea0ba84fdc2d5b1c`

```dockerfile
```

-	Layers:
	-	`sha256:ebb911b842dfb2bf726c36bd843d710c5cc80779fe83eabb56e1cbdb23588262`  
		Last Modified: Thu, 09 Jan 2025 07:15:51 GMT  
		Size: 19.4 KB (19419 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:fcc19990b5009e8d6872ecbab103e4e3b5d9e889bdf1d1dc295c185bf4fcb9b7
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
$ docker pull varnish@sha256:b87b0410c06db25d8a1eee7f1b1810c597a92b955351a5d9991a342f2efb01e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134241793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25e7979d0fe2da9c2e24402be0ffd0bd75756b4f02bce8afa7cedcb8ed36650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67ee532e82dfc81655928a069b82485465822cbf5c1542f69c6d34d2faf3648`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 106.0 MB (106027463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2958af66e2a26b4907cb4ac12a284d9c9037bb0675929e18c0684a07e175f3d4`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603feb9d9bd8c46d13cb279a37a354faa7d1121aa86b4f1989264bec05f080db`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:d69f84689c980cbd991fc051a2dcddc9efcc621a36fe697b1146b00b7d3ec696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdd72eff6cae3462e76c0cd730aa70e1172853fe5aa8bb65fb763776d47d370`

```dockerfile
```

-	Layers:
	-	`sha256:2513e43cba4d6a41c4cc145ae8c3232574ebbd10125c541e2160bd5ac987bdb7`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6c6a9f46639e61c0a1f61baf41f9d8745e6427ffb53c78f2dd15c44eee937209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104582434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466337ca1f1fbaace72e6a4643a8c3eec8d2d743e703e0004aefd901006b9cb8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e8b227058e9d3454106b69de6fe66ed17472d316ff1921b311633240d0ec9`  
		Last Modified: Tue, 14 Jan 2025 08:52:00 GMT  
		Size: 80.7 MB (80665801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef606ddc5460ca106eae7ae656ae0cd58d4ed4d51a760fa98f5eee9d2b83956a`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd367c2f86e70c54d56ae1340603abe7796a5009f884f3516a60201fc33811c7`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:db318c923596723ecf0789d3bc89d94eaea463170207a15a7a33b083e86d4a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f348855c155e8e496de72e8473741aa67df417539e48b6a5ff32acbbdd77049e`

```dockerfile
```

-	Layers:
	-	`sha256:041ac58bc5d4000faf092ee1cf0a347606281ab0da8aba370347b562b59e2385`  
		Last Modified: Tue, 14 Jan 2025 08:51:58 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a1d3ada6bad3845372d3dcf432d32cbfb189e409cedb54d0f1a242e3776fc812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128523233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef025c412b02b3498e4f94b33ec1cada8b72226b953ad58c4ee179766ab4410d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626bc79106fc52a258b19e1b8cf9198fce3c923c7b95da70f12ad8e8f976bcdf`  
		Last Modified: Tue, 14 Jan 2025 06:54:31 GMT  
		Size: 100.5 MB (100480172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2beab08663c7aa35e561cca3ebb41cbc71ebe6de2617385520b1d0628cd7931`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be3e3459e06ed6b1bc3d7dd210e7db3bc4ec94a34345b9b8a6f3bbe00297ac`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:021c3f4b064f7e9cbc08600b787cdc2e5efb3cd884a9cf919c0b7250909904d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3dd6d1d3f06388322d2e9f03601d9d96bc45eb6eaf61b1b8880bdc5b15f7e0`

```dockerfile
```

-	Layers:
	-	`sha256:04bf3117b2f9ac01066455de1fff3460fcd52addba37c0810b20ac0646a2bb0b`  
		Last Modified: Tue, 14 Jan 2025 06:54:28 GMT  
		Size: 19.6 KB (19563 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:6190cac5d9924878c2b8728f9592099581bb0a3f4d7d381f5f9f529817f5a9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131328178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aec168bc04f7cad8376f43f41a969143996ec48e484f1f4e9f30e3edf1a6738`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e55145e6767f7d9669a44c343e78f5f089496cfe29cb1171ff95a388e8d577b`  
		Last Modified: Tue, 04 Feb 2025 04:39:09 GMT  
		Size: 102.1 MB (102138693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1239ea0306c326a98823d354aa04ba633c23b14acfac4c4b0de83733522813`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833543a02a818ec2d1ea9d4b9e32d0f0222c832893edc139c8c5dbbc63753dd3`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:2b883f256313e43c6503d1000d37cda90cc5d82fa175d2112fa9cd5bebc3c406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c1b5e4fee186a04f342ccc16b9479323d788276943b0ec8375c42cf4684e4a`

```dockerfile
```

-	Layers:
	-	`sha256:644acc248591d721fcfb9b2001687945d76051de597b94c487ede0b73affe070`  
		Last Modified: Tue, 04 Feb 2025 04:39:07 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:023956b82e9a1d9c9bb184334f4b7b9199c66381c24f428c897f5d4a7400474c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137011865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748f3334be11673591b49c72941ef4d1cfa9237427d24bee54a5258588b71aef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bddbff44e0d90b074d9252780960e743d65647400597bdbdb723bd5f9bfe803`  
		Last Modified: Tue, 14 Jan 2025 05:17:46 GMT  
		Size: 105.0 MB (104964983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95ccf741d55e2393a51c73fd89317f3547d5adb7207dbde5537afc3658ae86`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882ddfad3345715772448bcf8f5c45dfe64cbea01e0ea80d3ba7c3b7017ade57`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:ccfa4ec81beea4b85eb4896509d2d04ff65ad6a685b0bc603e2f715d7b928a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa66aabb06da34b938cc62ea7b7a45196de3d0760ad94174a4a248bee7daa84d`

```dockerfile
```

-	Layers:
	-	`sha256:cecd8427a1bfba726b6d75bff2d19dadfce919cd4b4f62886d38f8a4cf02efba`  
		Last Modified: Tue, 14 Jan 2025 05:17:43 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:e2658e2b46db161c995e14a46b8c86e2b05dc52e2cd75659a137f647a0003ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112112393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0144263695361fa97ddcffd6c3c9e365b173d3762af5d764c3c42cd60689cdc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f774a4d8b78e92bed8a0db33c73b450dcc47592fda460bc69effd0c061b09`  
		Last Modified: Tue, 14 Jan 2025 04:53:05 GMT  
		Size: 85.3 MB (85251621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d03d5f51f4613e32fd2d3b277656f0203dd8009b2f6e316eddcebc5673a33`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f3f67992ed74220778b755e60f7b81a6c917eb1adcd846f3f8afacd330ac60`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:0ed1c02bb35bcc48d4ba11375bd017df3aadeba9577ccd32dc79760544ab8cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f9efc6ce720fdc68b64ba55e6b126ded9de51d7b46334bd48b8042023cfd05`

```dockerfile
```

-	Layers:
	-	`sha256:3bca138d1c90f55120aa3f3e4314121ca90f7142456f54a8cc8c7d86640772fd`  
		Last Modified: Tue, 14 Jan 2025 04:53:04 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:1a667bcd6b64099acbd075b1c347393e3cdb7f76d0b054209ed5bd015142a72a
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

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:9f8e5099ebe0d8c36e5275c92ac41941ac656b81ee99b2242f1bfd2eccf7a870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133947580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0ce3671cc93cda6b4fda1720db7d6f8f58c1f10ad062a16115db45009d2d8d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da20651324383642e77305fdc8e5ee80e40ed9110f7f7fa3a44ca0124caf6b`  
		Last Modified: Tue, 04 Feb 2025 04:26:04 GMT  
		Size: 105.7 MB (105733248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2958af66e2a26b4907cb4ac12a284d9c9037bb0675929e18c0684a07e175f3d4`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18fc8b1264f71a4e5fc52f2bc6e74d64d699c1b0450cf6ce424accae804cc05`  
		Last Modified: Tue, 04 Feb 2025 04:26:03 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:1a5278c3c63de014ce017013bea0011b075c54752ff654276b6eab53026a8e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c3c464581b3f712bbb05dc82764f731c8f5c3ad4549e044e17ecaa7787d902`

```dockerfile
```

-	Layers:
	-	`sha256:b177209b0f766e9795f77d086a175574726188b79051e0e465987a5054710e81`  
		Last Modified: Tue, 04 Feb 2025 04:26:03 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5ea210e09979ca90b9deec1fbedb8695639ecbbb2979143fc3f424b4ad3e6e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104301434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34cb2867fc13015905b8fc0ae4f3e62435aafbca1d250855f0ddf48526fb39a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322188f9e166a922611c24675a020e8057d7fcf53d1053f2bb283b525bde340`  
		Last Modified: Tue, 14 Jan 2025 08:55:13 GMT  
		Size: 80.4 MB (80384802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7e54d0742912b656895a8c84766fd91aee92e87a36cf75770454fadae3cbc4`  
		Last Modified: Tue, 14 Jan 2025 08:55:11 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79c9133be42fc73eb284dce8bb90c975d2c44a550a7778ab14eaf7a2cf5bf6b`  
		Last Modified: Tue, 14 Jan 2025 08:55:11 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:ed97e9ab2ba172f200ba9c78efb63d471ab67092172c33a2913f12d0885ae4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429c83cdc91ff1a0749468e28c605f6cddfab32508e1f07c6eb1282c0e9bc38b`

```dockerfile
```

-	Layers:
	-	`sha256:9f3449d9df625d81759852b8bb625b472977d62d8778b8d6e819cd48ccfd91cb`  
		Last Modified: Tue, 14 Jan 2025 08:55:11 GMT  
		Size: 18.9 KB (18869 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:fe9080130f5fb29baf07e52379a26bc14c30d9cf32979d78cd13d18013ef2254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128228781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7833533f9bcb4c5d332a1a3ade7827bc08c8029967d977581b87606e12d21596`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636e5cc10fbd69609472b5804793d18f5073426b3ff433573f8f3a5eb65f589f`  
		Last Modified: Tue, 14 Jan 2025 06:57:14 GMT  
		Size: 100.2 MB (100185716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dbc759d0ab91f3b54dbde468018717fa687e97be39ac824438c273df06e476`  
		Last Modified: Tue, 14 Jan 2025 06:57:11 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a998e2ce147a4d194fda8e8e26e48a60c2ead365dcac624740112ccadd67132`  
		Last Modified: Tue, 14 Jan 2025 06:57:11 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:b429375d48b4f8f6f126178bf3bf93225f5803ca4c3aae6452e79509d4e32748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e64caa2ca00763e0182119c7e8d62ee25cbaf4f3e16bcf893f0e61e83b4931`

```dockerfile
```

-	Layers:
	-	`sha256:3cdcdb448e5aace0ba34f93e85edcba0b777a79f5b853069f3ecf2a992bb806b`  
		Last Modified: Tue, 14 Jan 2025 06:57:11 GMT  
		Size: 18.9 KB (18896 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:32961a84374f32ce335c3c2ddc6b9b654c8dceb2681ee77352fd1b1bf8c2a4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131058305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6590994ca1a7c60f38f951597dff1f567e90c921411c9d25f7ea0a2362a5e00`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31381739b1cf1d2013ab05495584256c14f70ff0690459179356fb415eaace20`  
		Last Modified: Tue, 04 Feb 2025 04:26:04 GMT  
		Size: 101.9 MB (101868816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22882845a4dd3b8960abc19f5cbbfbae10af74e6657d93ee64322171a1138aba`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63cfb1491d67d2f05f2d7991a2b1800d36bbda089293f6659a0b8b489e95c60`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:95bb88de67b2a8eafd754aad33701a7e7ebf11fa3ef9bc781b7ac22c3803bc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d057c2da4e156b6fee96bbbc7530fc6e4e5ec0e3cca758cd4ad56b383aa1c853`

```dockerfile
```

-	Layers:
	-	`sha256:bcf1cc90e51943acc8378004179404e8764fa3100f9da307356624fc646ac2e4`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:c63d68ac4edf4f9e85b41869e7a4ea1eabc3c3842b80a49440dbff4d90832ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136725124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cad6d46c54e6e579cde8f2d936ca9d971abfcda21f2591cdb79f5366871c39`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace8d768f1dade09fd3e91c83643659521032a1e92c02c0da8337ff66dee64b8`  
		Last Modified: Tue, 14 Jan 2025 05:22:23 GMT  
		Size: 104.7 MB (104678242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5141099321bb7ae35a96b984a4a20890824469d1f5018314ada77330e5748773`  
		Last Modified: Tue, 14 Jan 2025 05:22:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e62327219f02684eb6825d4ccdeae9e2ee7a95ed7a734114d6a341b57270d2`  
		Last Modified: Tue, 14 Jan 2025 05:22:20 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:7e548236caca225ed5934d475c24ed217cf64885731a42e7e0cf729e538a6d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d35a6420e9e107b9084c8eb162d3cffc7f0178652f81dea7b637bf59a007974`

```dockerfile
```

-	Layers:
	-	`sha256:883e131f1e31ad90f3f2a7df1f85af292546026a8bf028b83977ccd5aaea37d6`  
		Last Modified: Tue, 14 Jan 2025 05:22:20 GMT  
		Size: 18.8 KB (18843 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:2d4583d536538799c8f25830d5bdee68f9f7703af927258252ee299787230d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111830956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca6a38fa7276d88267ff99384340cfc22e1ea21d63be9bf90375397d05a64c7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d12c8908d8b5e548aec881ce0406a770ed81368a86ef8517ba94d60c08f1e9f`  
		Last Modified: Tue, 14 Jan 2025 04:56:17 GMT  
		Size: 85.0 MB (84970183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2af03bf9135b8db4cd872ed5c313f5ceed5e29c99894a869316bb638a28b4c`  
		Last Modified: Tue, 14 Jan 2025 04:56:15 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93263ea9e4852d61c6a835a306352bae82471d357d8a27bfc75abc7ff9c7e92c`  
		Last Modified: Tue, 14 Jan 2025 04:56:15 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:02c5bd30f948dfb748a66134376d29daa8bf6213f2dabf6d3ecfa7d8685b3296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b96bccf27e617aac980f69a15dddbb1fc84317f62f651e73929e17c391d777`

```dockerfile
```

-	Layers:
	-	`sha256:a5f4145b839dd98ff7ef445bd10ffb4a3c2cac5d51c80d64c040b68196f4204e`  
		Last Modified: Tue, 14 Jan 2025 04:56:15 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:89f543a45e065043a3f68ef5484032fc9193bb07ea0b8c743fe0c9428a3ef7ca
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
$ docker pull varnish@sha256:341b855a7562eb1d04d9d603ad4fffbc7669fc2a965fe8acf239d5c26fd28a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73218172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea286037dc158224459d418685572d5d09358502baf739de42009b22220fc77`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de97c78fb86cc03363e31797a2ee46200ad84519bb172e342c29aba6e07dfc0a`  
		Last Modified: Wed, 08 Jan 2025 18:10:15 GMT  
		Size: 69.8 MB (69795887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d78790b7f984baf3d970ee734e8d653dc3a30b7d00d0d4f7924f9476d402e8`  
		Last Modified: Wed, 08 Jan 2025 18:10:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9584ea80c9931437eda67089d6419bc64c1286736349bb9e3ac4cf7a3b229cd`  
		Last Modified: Wed, 08 Jan 2025 18:10:14 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a41d906bb50ef9f906950563d4c349cb4ee8c00f374ebf7c4e05714f93722539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b23ef427dc91faa8c1c6e2f1fdd14798fd6f948654d3de43d0b8e77ed9a50f6`

```dockerfile
```

-	Layers:
	-	`sha256:5427e28af6fef77db34da4b02b74576cb2df6b873be7e3e85eb3d29ea1437685`  
		Last Modified: Wed, 08 Jan 2025 18:10:14 GMT  
		Size: 18.8 KB (18763 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:6d7864af6574ea9416bfd0f53336eafae86d33abfe0b46325e3829645a82279e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57420453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d4958b6c35f9c50acaed67b229eb124c708485b659f89863a8cb28fcbb76d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-armv7.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:a7e7294636d65e1e64be6d2a9e772d5c14442ce00c5a9d8d2fa587f09b5ece5c`  
		Last Modified: Wed, 08 Jan 2025 17:34:28 GMT  
		Size: 2.9 MB (2928493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d675b62f999bd70d6f7109ae83f0c587fb30c88e33fe61576ec99bed479b76c`  
		Last Modified: Wed, 08 Jan 2025 21:58:32 GMT  
		Size: 54.5 MB (54489915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377da637b70832463cabf407f8f7b3498baf84045afc7d7405879e07b121d35`  
		Last Modified: Wed, 08 Jan 2025 21:58:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6a07633aedab7dc1a4e501bf2f58bc0579f2350c418a31ea94bb6a0dfa3f14`  
		Last Modified: Wed, 08 Jan 2025 21:58:30 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a1bbf35e981b26f35976863f460dcf1031ce2f62427393ebdb361f2a7412506f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d56af7896b15516643a5ed917b4ebddf7432bded26e5af5bec735e325f3a943`

```dockerfile
```

-	Layers:
	-	`sha256:b7e5c45eba453f1b8862efb18fa3bb025f65351a47e7b312b1f6a45e5cad69ea`  
		Last Modified: Wed, 08 Jan 2025 21:58:30 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:30773f624f1e63023f73dfbba41e2882f4195aa1110f4413c85868c2b9645fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69925040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ee5046044834745bfcc1b7358de9e33fc5ae4e355cf371fef3cbce93f152f5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632054204c85a7143bd6fef15934e51228f04590e41565899d022be015f9191a`  
		Last Modified: Wed, 08 Jan 2025 22:11:23 GMT  
		Size: 66.6 MB (66562470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c0ecc0c6da66aa12545fd7af08e44da04b79702e1941ada9288cc07980a019`  
		Last Modified: Wed, 08 Jan 2025 22:11:20 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795187b75748cf54b0f558c3d7c16ae6ee13ae0e4def40c529ee65f35e0e5156`  
		Last Modified: Wed, 08 Jan 2025 22:11:20 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:56738ad0a92281302d414a21d953aa86b44deddd103d3d93d35c5a91489f9061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448897dd7f5eecd0a78b9338b0b6dabf5673d2299f6b8ab461edaaa56bf5901c`

```dockerfile
```

-	Layers:
	-	`sha256:c7a30de62a515d733b93c7b4eef43870481779121aefc8145b293942abe638db`  
		Last Modified: Wed, 08 Jan 2025 22:11:20 GMT  
		Size: 18.9 KB (18855 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:9280770dd8c821b055e1171d823cc442e54a5a81606490a1a8c69f92c118ebff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75242237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0df770d763e39304212ce2b6776095229aaaf6f707c6ec35fa7d26520565092`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-x86.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:ae1d9a0eea37f9fb4394d27e83eb58694cd0a74025c8c135051300a330d76686`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.3 MB (3254296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565cb2a1d37b16c7cb73a5aea454bb6d637b2f0943f771b99cb6e4714448864c`  
		Last Modified: Wed, 08 Jan 2025 18:09:41 GMT  
		Size: 72.0 MB (71985901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a0e7967b42329e3d8b18fffcc5a8b48af05a6aa753e6cf0dcc15ef7a66e3b0`  
		Last Modified: Wed, 08 Jan 2025 18:09:38 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f4edd72a9da4f744a160ae7a8512192b0df34998a056bdc823b071e4eedd74`  
		Last Modified: Wed, 08 Jan 2025 18:09:39 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4ae2d31b7c6ab1e843e7475a48708d350e2a8427d3f33bdcbcd1a26e4bcb4999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5936b0e9be21e205ae60ef7e55120f1a02e6999ce6cd6899b945209d12d05ea`

```dockerfile
```

-	Layers:
	-	`sha256:c8ac87c90a88eb7e9b9957dcabd34a9aa1a1d184ec45c787ab57a0e86293f4de`  
		Last Modified: Wed, 08 Jan 2025 18:09:38 GMT  
		Size: 18.7 KB (18736 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:c0ba51a0f5b95cf795c9dd78c222f5d09936e0560c11b2e181c1f76d2911874c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70751061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205efd7fdfb2a471906d16258df15c898cd62230e155d8f37ea9c4b88374b6ff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-ppc64le.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:a1e53c81da67874250566308d64e6cf88d5d19fb3bdb55484bd7a41b4e42a126`  
		Last Modified: Wed, 08 Jan 2025 17:25:17 GMT  
		Size: 3.4 MB (3365646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c0cf4e3d832e836ec3498619c51b145b51afa395950ccfab417c99655196a3`  
		Last Modified: Wed, 08 Jan 2025 21:36:04 GMT  
		Size: 67.4 MB (67383366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689348f90ccb130675877d0c11a5c7aeebc9c58a30f2d19e289f4f40dae621a1`  
		Last Modified: Wed, 08 Jan 2025 21:36:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f29beff7316441713a23af54a36a9bf723df7079bf968dba903a1e86a2d4a5b`  
		Last Modified: Wed, 08 Jan 2025 21:36:01 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:82a483df9bdbcbe8e16a97eee66659e0b38094aa87c9bd9a098d2a3320c55e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abde29b2971cb4289c0470bf31629c5b1f49ca144a9e4052ef838f41fa9b30fc`

```dockerfile
```

-	Layers:
	-	`sha256:3770a61226ba1c99292a6b3882b0f32204b0758a8473b99e74403642ac1bef3c`  
		Last Modified: Wed, 08 Jan 2025 21:36:01 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:a58b9bf442235ffc294be3fe46cc886b9e641bc97ad4c8af88c6edc70920df77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65129234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5edc4e293f8e9c218f5bec0358089d56f55a5d98e6de772bec65a50ce683f29`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
ADD alpine-minirootfs-3.19.6-s390x.tar.gz / # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
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
	-	`sha256:be00939408ff94e4fec4588babdfc5d58c5d13d897e8cc5dda295b4a6253bfa9`  
		Last Modified: Wed, 08 Jan 2025 17:26:42 GMT  
		Size: 3.3 MB (3254251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fb86a50486c3cbf360ddde20ea4bdf6f9bb868eb4fceb02b50bf86c5261b8a`  
		Last Modified: Wed, 08 Jan 2025 22:13:42 GMT  
		Size: 61.9 MB (61872941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775827bcd8189eea66566ffa6022995a34cb53b3e0d05a687de101f359fa4253`  
		Last Modified: Wed, 08 Jan 2025 22:13:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ea03c68cf47aec14da5f72a5cf4615265bab6aaaf2db5baa02ed8dec3cbcd9`  
		Last Modified: Wed, 08 Jan 2025 22:13:42 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:16cc7563d6c3d904a1171691862f0e6853c16f0bf6e0dc0c93236633c57231f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc334713869b42dcf283dda157003cbc42a615d9ef1a06b8c517a98d09d2c42`

```dockerfile
```

-	Layers:
	-	`sha256:1e41947d2117ddd56c851c4575cd6166f22339814a43af8b6e6450ba8f4e35f0`  
		Last Modified: Wed, 08 Jan 2025 22:13:41 GMT  
		Size: 18.8 KB (18762 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:stable`

```console
$ docker pull varnish@sha256:181939fa86e965ea5be859bf6d33133750691522c008d4f70acb6b028a09df46
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
$ docker pull varnish@sha256:7eab999ca9ba21e47d3ad7932cdddece413eb62131760028acdb606e94e7d097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127744114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbafa05faa65c7c1b9e5d1489df1f267628b18a558761571589a39e33b0efeb3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081782e116e5eed5271697edb555e187291ce5f8bb24b5a553c9206f86dadab1`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 99.5 MB (99531072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e138f6524b3e3c2020b242f5b79b2866a473387b4a7dffdc369c996bf711698`  
		Last Modified: Tue, 04 Feb 2025 04:38:17 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:dfc08938e97d7371a7aa9a16dc0038f42d9be1a652ba3f54145a8be393b22436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f72107e71a4952b63c4f0a8ac7aa9a0326584686102e21586ab8cb98c89311c`

```dockerfile
```

-	Layers:
	-	`sha256:2965fac2a2e017081031b82c8853f86174239a23d0dc90b4d82a67bb3f256d18`  
		Last Modified: Tue, 04 Feb 2025 04:38:17 GMT  
		Size: 12.7 KB (12664 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:f3eba1d3d82e6515432d2e62ec2951d1f445db43212f5489b18c67369748ada2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98265158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58377b8b5349d38eea94b8754ac3faaf9f77c7824625a14b39b1ca9d3c376f3d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623f1bad8156810b22b0edaa693ad4be604a3f3de28d34c6ad3b6eb689535803`  
		Last Modified: Tue, 14 Jan 2025 08:57:29 GMT  
		Size: 74.3 MB (74349820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc57c835e653933c1a75f0abf7c3c6b385749ff93de73bd74ac6140d6de12f25`  
		Last Modified: Tue, 14 Jan 2025 08:57:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:d54465dd21cc5025bd296b9dd630e0828daf8b323b039f8409598cc22624ca39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142dba2d13a72d70b22190383a71e968f7221caf2eaebc8d84d5be2db30017f6`

```dockerfile
```

-	Layers:
	-	`sha256:4d6b7224fc907f79d3026decacd2c58ce62755d0553f8b10ea40ba8396667072`  
		Last Modified: Tue, 14 Jan 2025 08:57:27 GMT  
		Size: 12.7 KB (12733 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:388c0741d4852895ca0e5fb292d4d71a3f47fe778710017e9ec8fbcc83197d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122335042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa19fcbeadbef7caf3f789400cf8aa99cf97433faad3dbc79ff8ea3a1e910d9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815e7350a51ff15dbd37103ac2c590a51aecc67ca0f7ef1ba80497e801b697f3`  
		Last Modified: Tue, 14 Jan 2025 06:59:16 GMT  
		Size: 94.3 MB (94293273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fb83dac11f68d3b9d6ffc6014f7064e95e8a4bfd4e7d9f429348d7433f87f2`  
		Last Modified: Tue, 14 Jan 2025 06:59:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:ecfee932175e8205ad1fa2ed0e67e8fdd2a3e0e24d7b754c01d8e45fd7a20f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3207beeb8a90aa9293188aba5ad76d3744362ae4f68df488984541669bd8196e`

```dockerfile
```

-	Layers:
	-	`sha256:8abdad0695d4e98ad541ac3ef1e335e604581f1484c181546dbf53bf105a9a3b`  
		Last Modified: Tue, 14 Jan 2025 06:59:13 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:61c4cd8f36067478027462988e93d012e297c951068f8df3a9d877e7b96a2c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124881588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62f7d80394fa02326ed9ba2b787be5fb09983f949b0cea746b302f32827eecf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b4418305a63b59ede7eb4dc3f5f915aecceb2546eb6cdf60d65081fe6f1649`  
		Last Modified: Tue, 04 Feb 2025 04:25:02 GMT  
		Size: 95.7 MB (95693393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1719dfc6f626afadd6b2a874fdc0c6cc87d513591fcc6421152759c453f5fd5`  
		Last Modified: Tue, 04 Feb 2025 04:25:00 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:8d47bec1318c45e301e5ca0a2e9293f66f737a305dc821d9842c7cebdff72fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655b25df2d14182da965a72adca522b43395abb95f1a5bed902f97751f087f0d`

```dockerfile
```

-	Layers:
	-	`sha256:cae5ee654d71dfb7c8cbc261f9fc3fd8c3558605afb138471a22b25a7b7ff506`  
		Last Modified: Tue, 04 Feb 2025 04:24:59 GMT  
		Size: 12.6 KB (12636 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:40cef478164f318e19d43450d12930f64092ded44d29d268339ada5b219eff31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130385950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ece843f84eb6f2546881506c0c0ac76c258829a6cb6ff9af1db6ac38028a8eb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b0fc273c4beb3aeb8252123196070e8712a5556c2abf1a479be94a0136d400`  
		Last Modified: Tue, 14 Jan 2025 05:29:04 GMT  
		Size: 98.3 MB (98340365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811487ce142300c995652dc861ebfd95fb8bd3ada20d8106867a3cc5ff0280a5`  
		Last Modified: Tue, 14 Jan 2025 05:29:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:c6f4c6b0d234a8d0aed90aa7696b478287d6a2e6e00f1b546ae1774e871195ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1434e9aae546019c74bdf96baa5c226874ddc0c8143f1f291f0fe7277bd45a6e`

```dockerfile
```

-	Layers:
	-	`sha256:fc18ea2fd0bb91f94d83eb7ab5feb465aafe09c0b63fca6b29eb0429eafd0ce9`  
		Last Modified: Tue, 14 Jan 2025 05:29:01 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:112f1331e4a4b811eebcf3d86202b7ef5e52c3191b113149750c64fd1a9f76ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105598496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622be870f743ed1c0c7a06281122a2d8de9b9f0ae7a774f9c2697b1065d20a4e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d85ab31aecc604366f0a97a38fd5ed12e3ce8659de9b0a170b669bbe54be601`  
		Last Modified: Tue, 14 Jan 2025 04:58:34 GMT  
		Size: 78.7 MB (78739019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae7f98d2b1033968b9c6a8052d2633b2ea0e3d621ac2deb7cc82de68a0ee767`  
		Last Modified: Tue, 14 Jan 2025 04:58:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:0980688787d4adf583fbda153f13760e33d65079c995b037d6ee933e752baca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f34e12f163cf3800437b56ac9d6222627e0068ffb5ce95baace42eea9006b1`

```dockerfile
```

-	Layers:
	-	`sha256:f86cd0c141117065b5179f61f9ce8504c1ac275e075e15fb1adbb4586875fc59`  
		Last Modified: Tue, 14 Jan 2025 04:58:32 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json
