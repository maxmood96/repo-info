## `varnish:stable`

```console
$ docker pull varnish@sha256:79ca64274ab3d806a5a0154e4d1e009e5b6b86de62b4eb343c45ca0f27ffc7d7
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
$ docker pull varnish@sha256:998cc70dc7f4abf643c0c1582cbd5acf3cd3ff5446dae6cc1082a4dcd7d5fb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127744768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e484cbfce116b5df464b394c1872039fa65871e6a90543730b990019401b2f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922ae497461083b96eb2cc5ba40ca476e97c5026737e8fa5489000be4d50fa02`  
		Last Modified: Tue, 14 Jan 2025 02:19:18 GMT  
		Size: 99.5 MB (99531614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7918d48792ccf62bc425b845e480cfe20f9df7ab2a1e12fd5d94e1f92c39ff1a`  
		Last Modified: Tue, 14 Jan 2025 20:45:59 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:956800144873f9bcc7f47ea26408cf9135efc8f841ddd62e875729e34a95428a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894108b82fbf0ebc1b0609bf0e4c70b86595d0e1bdcb496f0c45082857f25ff3`

```dockerfile
```

-	Layers:
	-	`sha256:2918ea335373d685ba044bee9e9a24737b47ff1bd731a3bf2026dec7caea05a9`  
		Last Modified: Tue, 14 Jan 2025 02:19:16 GMT  
		Size: 12.7 KB (12665 bytes)  
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
		Last Modified: Tue, 14 Jan 2025 20:33:55 GMT  
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
		Last Modified: Wed, 15 Jan 2025 00:51:56 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:48:31 GMT  
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
$ docker pull varnish@sha256:d20444a2feb98ab11711ba65e9a9a35102f991e1ca0380f14a58b64188b24307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124881891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a0a64db00037b42a82000b408c73d18756f3896bc9e3c039f5930919602c75`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Sun, 10 Nov 2024 02:42:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
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
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81363fe535d89b9e89433f5100ad13faa2694dcda9fa50a9af4648b62601237`  
		Last Modified: Wed, 15 Jan 2025 00:53:52 GMT  
		Size: 95.7 MB (95693557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c43de37c9386ea3b01556c3e48bf7cedb4e973cc9c006fb59e07662429576`  
		Last Modified: Tue, 14 Jan 2025 02:18:17 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:7157fbb631b232c8df5511b9b5570eed15ff74fe7a9968552d6be8bb005eb867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95b7a50020d63a3aa65bbd5d7e44fe36c171134c37605c07fcb71d91316c97c`

```dockerfile
```

-	Layers:
	-	`sha256:52fd5c87166375d7da8f201bd617d2f066c9c1ee69ab30bb4c8fa81830fd4e14`  
		Last Modified: Wed, 15 Jan 2025 00:55:36 GMT  
		Size: 12.6 KB (12638 bytes)  
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
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:36:29 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d85ab31aecc604366f0a97a38fd5ed12e3ce8659de9b0a170b669bbe54be601`  
		Last Modified: Wed, 15 Jan 2025 00:57:42 GMT  
		Size: 78.7 MB (78739019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae7f98d2b1033968b9c6a8052d2633b2ea0e3d621ac2deb7cc82de68a0ee767`  
		Last Modified: Wed, 15 Jan 2025 00:59:18 GMT  
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
