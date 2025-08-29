<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.16`](#varnish6016)
-	[`varnish:7`](#varnish7)
-	[`varnish:7-alpine`](#varnish7-alpine)
-	[`varnish:7.6`](#varnish76)
-	[`varnish:7.6-alpine`](#varnish76-alpine)
-	[`varnish:7.6.5`](#varnish765)
-	[`varnish:7.6.5-alpine`](#varnish765-alpine)
-	[`varnish:7.7`](#varnish77)
-	[`varnish:7.7-alpine`](#varnish77-alpine)
-	[`varnish:7.7.3`](#varnish773)
-	[`varnish:7.7.3-alpine`](#varnish773-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:aa957772ed72442badfc97503c7060712e882cf0a7c040d2123573882a90109b
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
$ docker pull varnish@sha256:7cbd3be8de1473ab7d729e2012007525a32dab1c32f01c66750a76c2dd6a3dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103551153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee7a302b300e0cb28da3f0880ae89e521db3f03ba8249d567a01a52c87ad28e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fb9407627d2a9673f9f2996eaefe14a925c79c1d6760a3bde4f7dac638edc8`  
		Last Modified: Tue, 26 Aug 2025 16:51:05 GMT  
		Size: 75.3 MB (75320140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c8bc1dd94e689fb630ab2b2a2aab8ea10c3a98fc336e39c91ed99ead7034ba`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 726.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:cfa7954490ec481b365f10b95e49c759856ea3ed871b62e4f3ad3389b73a81a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3706ba5ff3090a5ae767c72196968b3985e0e33ced0bd740df008593e1642394`

```dockerfile
```

-	Layers:
	-	`sha256:924ba8f8c4217d028b2f271cdbfe266029ee64ece4214470a2274aa4a6907ede`  
		Last Modified: Tue, 26 Aug 2025 18:19:31 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:67a552aaf0a0bf11116498591becce6ad57e528d4b447459e2138cc8858e77cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75973152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584645e54dd6e80ac1b2b9683f0c5b6533ce57e5a8b5bb136f9aa9b65b4bdd84`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694e45c2ad1ef6dbad25ffc201a18db57ac9b1f77c3963b7253079914477ddc`  
		Last Modified: Tue, 26 Aug 2025 16:54:20 GMT  
		Size: 52.0 MB (52033469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3e2473be879b601edfcf51083f41cc2c5a52f77f88b33aa96ca7e00754017e`  
		Last Modified: Tue, 26 Aug 2025 16:54:14 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:8a8c4e092458ba65ade061405ce3b0db4d1c90e5c00d579856a60aeebdc83470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e42311eb05fdf74621332f9c5ed20f71b0929d5f7d49de57df10a1b2f5fd012`

```dockerfile
```

-	Layers:
	-	`sha256:26460142477d0a1b71cde5a5ea3b590142211fc13d2aa4f9d11dec9898ef06d6`  
		Last Modified: Tue, 26 Aug 2025 18:19:35 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7947f456530af586dd14fc9b2ee5e323b3937a7813f17b8f5bc2eac64f7d321f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98372014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3973020c0ead804b1fc21b077ce805dbbb560aba29ab7b7b708a4c8ccbc08996`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fa0bf97d17bbeea81d2494c7f6ea7802aaa88cd8b8b476210467e1416c35e7`  
		Last Modified: Tue, 26 Aug 2025 16:59:55 GMT  
		Size: 70.3 MB (70289258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46723a79ce1a6afa1d880e4f0e59b65181a0327ff1ee22ad41e84ba426d2cd8`  
		Last Modified: Tue, 26 Aug 2025 16:59:51 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:3b30836516d8ef42543dd00040504764a4c4484d6a00d64ec8987ed0528ad47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579f165fc8ae5c798a4e2701e9479d82bbedaa55f3dd6201d6fe6c5f3728aaf8`

```dockerfile
```

-	Layers:
	-	`sha256:0519eb52a002246bc5923205d8e4b70f6978f3b2ecdfa4a23a9f736b593978f4`  
		Last Modified: Tue, 26 Aug 2025 18:19:38 GMT  
		Size: 12.8 KB (12785 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:2c5e6985d41327cbc8643b452c59764e1613f50a3b117cde8b684b50fdc50950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101012369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e63ef78a68ea4bf792399c15bdde269e88a61aa5c416925cc36c11dd66ad66`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102c072a05728f7a803239b2eb5dc78890f98f54a8014c8cbd1e6dd030c6fc9b`  
		Last Modified: Tue, 26 Aug 2025 16:51:06 GMT  
		Size: 71.8 MB (71799009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf2c5b223c5b80c6b598516e2900c4dc71f99d9796f990a1a2e3f5dc0e7da99`  
		Last Modified: Tue, 26 Aug 2025 16:50:52 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:800c990346e164b99d62c806c6e052adee15320e0d6dc5f809a8e06a41714f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbd36ff74ebe940838ed9965e0970fa1ae0bd79c0ca889995c365cf801c9137`

```dockerfile
```

-	Layers:
	-	`sha256:1ea1c351e16e7da1014311d822b69f527c6175936cf287a735e29da5ebeb9109`  
		Last Modified: Tue, 26 Aug 2025 18:19:42 GMT  
		Size: 12.7 KB (12666 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:e6b5ae618eacb7eb0133f5eb3181be22375c4b10e66899c71e17c3a24082e52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105453540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85e1e44c3fd0ad39dfe8fae37252892dd8e135a2511c415a7a2f96c6e93b09a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ea7a8002f28a34c01ba581d94952206b784a0f318fb381fc172c4b7480e157`  
		Last Modified: Tue, 26 Aug 2025 17:10:14 GMT  
		Size: 73.4 MB (73379366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5be6e400d7be941426e0d23d914b2621bd09a36a4e2ace6e8932d088497fda5`  
		Last Modified: Tue, 26 Aug 2025 17:09:59 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:aba0a640ac2b97154eecdff5b12c43f8d1a49aeb2a8329e1d9ec77a9f379ac74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c43528322730971f228ad2a545313b36fa5ab25716895e933e9d018d8048c8a`

```dockerfile
```

-	Layers:
	-	`sha256:d4859fc31065cc14ac9281aea1869b5bc5a134c4470f9259d499303d4f4af48f`  
		Last Modified: Tue, 26 Aug 2025 18:19:45 GMT  
		Size: 12.7 KB (12730 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:54424b955926c93cdb7c182553512dff290fd0eb4a0af9d68241d8ef9e0e7eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81339059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dae65dbb781c3a9d21184450a7784cf5eb3b7905f7671bb8a1e21d3efaedac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8088d9284f19de0c8967cbf0a62ab5e1d64ba1ddf753a30f29fd51e37f7ddb7`  
		Last Modified: Tue, 26 Aug 2025 18:20:19 GMT  
		Size: 54.5 MB (54450468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663a3924ff7952fc97c3a5dc37c8fbd957d14231999ff14d0c6eebb7f9f77868`  
		Last Modified: Tue, 26 Aug 2025 17:36:49 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:caf935fe01dacf82f134899bd70342c4cc73b59ace7f8dfd85ce24bea14a9f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c74b115bc1ce0225884fc3a7e1f201e20fe235665e96a88d74f88b61683086e`

```dockerfile
```

-	Layers:
	-	`sha256:ceaf024d37a6a7c15996bff2dd71860f2f7df3d73802dbf47330c3d0bea61e0f`  
		Last Modified: Tue, 26 Aug 2025 18:19:48 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.16`

```console
$ docker pull varnish@sha256:aa957772ed72442badfc97503c7060712e882cf0a7c040d2123573882a90109b
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

### `varnish:6.0.16` - linux; amd64

```console
$ docker pull varnish@sha256:7cbd3be8de1473ab7d729e2012007525a32dab1c32f01c66750a76c2dd6a3dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103551153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee7a302b300e0cb28da3f0880ae89e521db3f03ba8249d567a01a52c87ad28e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fb9407627d2a9673f9f2996eaefe14a925c79c1d6760a3bde4f7dac638edc8`  
		Last Modified: Tue, 26 Aug 2025 16:51:05 GMT  
		Size: 75.3 MB (75320140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c8bc1dd94e689fb630ab2b2a2aab8ea10c3a98fc336e39c91ed99ead7034ba`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 726.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:cfa7954490ec481b365f10b95e49c759856ea3ed871b62e4f3ad3389b73a81a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3706ba5ff3090a5ae767c72196968b3985e0e33ced0bd740df008593e1642394`

```dockerfile
```

-	Layers:
	-	`sha256:924ba8f8c4217d028b2f271cdbfe266029ee64ece4214470a2274aa4a6907ede`  
		Last Modified: Tue, 26 Aug 2025 18:19:31 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; arm variant v7

```console
$ docker pull varnish@sha256:67a552aaf0a0bf11116498591becce6ad57e528d4b447459e2138cc8858e77cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75973152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584645e54dd6e80ac1b2b9683f0c5b6533ce57e5a8b5bb136f9aa9b65b4bdd84`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694e45c2ad1ef6dbad25ffc201a18db57ac9b1f77c3963b7253079914477ddc`  
		Last Modified: Tue, 26 Aug 2025 16:54:20 GMT  
		Size: 52.0 MB (52033469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3e2473be879b601edfcf51083f41cc2c5a52f77f88b33aa96ca7e00754017e`  
		Last Modified: Tue, 26 Aug 2025 16:54:14 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:8a8c4e092458ba65ade061405ce3b0db4d1c90e5c00d579856a60aeebdc83470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e42311eb05fdf74621332f9c5ed20f71b0929d5f7d49de57df10a1b2f5fd012`

```dockerfile
```

-	Layers:
	-	`sha256:26460142477d0a1b71cde5a5ea3b590142211fc13d2aa4f9d11dec9898ef06d6`  
		Last Modified: Tue, 26 Aug 2025 18:19:35 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7947f456530af586dd14fc9b2ee5e323b3937a7813f17b8f5bc2eac64f7d321f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98372014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3973020c0ead804b1fc21b077ce805dbbb560aba29ab7b7b708a4c8ccbc08996`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fa0bf97d17bbeea81d2494c7f6ea7802aaa88cd8b8b476210467e1416c35e7`  
		Last Modified: Tue, 26 Aug 2025 16:59:55 GMT  
		Size: 70.3 MB (70289258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46723a79ce1a6afa1d880e4f0e59b65181a0327ff1ee22ad41e84ba426d2cd8`  
		Last Modified: Tue, 26 Aug 2025 16:59:51 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:3b30836516d8ef42543dd00040504764a4c4484d6a00d64ec8987ed0528ad47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579f165fc8ae5c798a4e2701e9479d82bbedaa55f3dd6201d6fe6c5f3728aaf8`

```dockerfile
```

-	Layers:
	-	`sha256:0519eb52a002246bc5923205d8e4b70f6978f3b2ecdfa4a23a9f736b593978f4`  
		Last Modified: Tue, 26 Aug 2025 18:19:38 GMT  
		Size: 12.8 KB (12785 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; 386

```console
$ docker pull varnish@sha256:2c5e6985d41327cbc8643b452c59764e1613f50a3b117cde8b684b50fdc50950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101012369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e63ef78a68ea4bf792399c15bdde269e88a61aa5c416925cc36c11dd66ad66`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102c072a05728f7a803239b2eb5dc78890f98f54a8014c8cbd1e6dd030c6fc9b`  
		Last Modified: Tue, 26 Aug 2025 16:51:06 GMT  
		Size: 71.8 MB (71799009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf2c5b223c5b80c6b598516e2900c4dc71f99d9796f990a1a2e3f5dc0e7da99`  
		Last Modified: Tue, 26 Aug 2025 16:50:52 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:800c990346e164b99d62c806c6e052adee15320e0d6dc5f809a8e06a41714f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbd36ff74ebe940838ed9965e0970fa1ae0bd79c0ca889995c365cf801c9137`

```dockerfile
```

-	Layers:
	-	`sha256:1ea1c351e16e7da1014311d822b69f527c6175936cf287a735e29da5ebeb9109`  
		Last Modified: Tue, 26 Aug 2025 18:19:42 GMT  
		Size: 12.7 KB (12666 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; ppc64le

```console
$ docker pull varnish@sha256:e6b5ae618eacb7eb0133f5eb3181be22375c4b10e66899c71e17c3a24082e52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105453540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85e1e44c3fd0ad39dfe8fae37252892dd8e135a2511c415a7a2f96c6e93b09a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ea7a8002f28a34c01ba581d94952206b784a0f318fb381fc172c4b7480e157`  
		Last Modified: Tue, 26 Aug 2025 17:10:14 GMT  
		Size: 73.4 MB (73379366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5be6e400d7be941426e0d23d914b2621bd09a36a4e2ace6e8932d088497fda5`  
		Last Modified: Tue, 26 Aug 2025 17:09:59 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:aba0a640ac2b97154eecdff5b12c43f8d1a49aeb2a8329e1d9ec77a9f379ac74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c43528322730971f228ad2a545313b36fa5ab25716895e933e9d018d8048c8a`

```dockerfile
```

-	Layers:
	-	`sha256:d4859fc31065cc14ac9281aea1869b5bc5a134c4470f9259d499303d4f4af48f`  
		Last Modified: Tue, 26 Aug 2025 18:19:45 GMT  
		Size: 12.7 KB (12730 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; s390x

```console
$ docker pull varnish@sha256:54424b955926c93cdb7c182553512dff290fd0eb4a0af9d68241d8ef9e0e7eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81339059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dae65dbb781c3a9d21184450a7784cf5eb3b7905f7671bb8a1e21d3efaedac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8088d9284f19de0c8967cbf0a62ab5e1d64ba1ddf753a30f29fd51e37f7ddb7`  
		Last Modified: Tue, 26 Aug 2025 18:20:19 GMT  
		Size: 54.5 MB (54450468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663a3924ff7952fc97c3a5dc37c8fbd957d14231999ff14d0c6eebb7f9f77868`  
		Last Modified: Tue, 26 Aug 2025 17:36:49 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:caf935fe01dacf82f134899bd70342c4cc73b59ace7f8dfd85ce24bea14a9f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c74b115bc1ce0225884fc3a7e1f201e20fe235665e96a88d74f88b61683086e`

```dockerfile
```

-	Layers:
	-	`sha256:ceaf024d37a6a7c15996bff2dd71860f2f7df3d73802dbf47330c3d0bea61e0f`  
		Last Modified: Tue, 26 Aug 2025 18:19:48 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7`

```console
$ docker pull varnish@sha256:86655495a7ac80e7fda84f19f1eee579435fc22204562c34db13fbaf4102f436
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
$ docker pull varnish@sha256:782bd500bdb785fdb7985580fa0b73900fe962f2d6add4ab0946e2e1f69ab556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116340261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d16006e8ae81f8f4f1cef1f748768ea880de2571a18c956ab825f14ab43964`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd0391d5883cb827d680d347a739b3ac285458ef597837bda7523f0a973f2a0`  
		Last Modified: Fri, 29 Aug 2025 18:58:02 GMT  
		Size: 86.6 MB (86564929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f18a62a208f5f2eb2041475b3216fe4a1c7b8504500ecab7ea3cc68a7f482e8`  
		Last Modified: Fri, 29 Aug 2025 18:57:56 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b91bb588fd3ef1a72ee515f842eaef66d07efac4f7532be94eaaffab957db5a`  
		Last Modified: Fri, 29 Aug 2025 18:57:56 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:e9ebb92bd3223ea842c0dba0b5e7b617f0e40a44dc3e6f278fb8d41ec5c569c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7ca5fb0a6e2724c258065f33f5234ec33b438c0e2595ad17f194c0541fd540`

```dockerfile
```

-	Layers:
	-	`sha256:eb95f7f1490761e6d482aa0115f80ec0ad51f34293f9c6bc0f57dc6e7be44580`  
		Last Modified: Fri, 29 Aug 2025 21:19:35 GMT  
		Size: 19.7 KB (19659 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:68553fd4fac212872a82a9bca4f90aa0fc69638094c46c365f791db6db74d8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87147139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ea9b8a9b4396797a250bed48de5272f14681811ecd7e368deb2cc144949fc5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab1630934ea323c0d50cad725c7dc5f676c44f7a37a7c722547b3f8329a540a`  
		Last Modified: Fri, 29 Aug 2025 18:57:52 GMT  
		Size: 60.9 MB (60937606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c629879bc4ea3aea6aa633a3d7637e4e66fe14911635796f3561a26fd4907a`  
		Last Modified: Fri, 29 Aug 2025 18:57:44 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2ca73afdb667b1da50b2ea4d322fcd05513a1911e2180eb861163501ca2856`  
		Last Modified: Fri, 29 Aug 2025 18:57:44 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:a5603bef1c4cdb0221c96fb8fa2ab6b88e8d5c677ac5f8bea234ea23c2217b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ff7de3d1eba34853220a869769d6c88bea927eb496790491ad9b454d5bfcb5`

```dockerfile
```

-	Layers:
	-	`sha256:009e4efa2775778a8bb24ee0501047432be01274e856457fdd7411ddb3cbf444`  
		Last Modified: Fri, 29 Aug 2025 21:19:38 GMT  
		Size: 19.7 KB (19743 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:87e15ca38843e689554f2dac5f8df19676dc4360ec484c367710a0275ba2cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110518057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35c1a9ea2a4ea53bdd656f6df8a6a591d583ae479a541e5bf9347939e87cb04`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095ad00879fa642ecdc94b591fafeb1acb212eff67e42d43e95a0e34fcd79182`  
		Last Modified: Fri, 29 Aug 2025 18:57:55 GMT  
		Size: 80.4 MB (80379967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6844b8a704384fdb04db8dcf95cba67fd2c38388f9bfb8d5135199b792d20`  
		Last Modified: Fri, 29 Aug 2025 18:57:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b4f6076a264c3d34d430c878c986ee818ad85c4dc0443f3b8a67b58de1e2f4`  
		Last Modified: Fri, 29 Aug 2025 18:57:45 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:907b29abed401a16407383031774c0e121cb5d5afcc701f7242f24cfb230bbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66ddfba9ba0b7ff583cf8ee5d35099f251fd77e0a2bc364020d17c83a34fe99`

```dockerfile
```

-	Layers:
	-	`sha256:33d1899c4bb8d5f0a4d251575b523821bb8673bb60f18783991b9b31d97a9af9`  
		Last Modified: Fri, 29 Aug 2025 21:19:42 GMT  
		Size: 19.8 KB (19775 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; 386

```console
$ docker pull varnish@sha256:9880404747e278ecd087f5c6eab6bf8412c5b0ba50e991d6485083f61c34c1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114474612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaad62c8bff104e799093949a5bc72dcd1384b6e4388ae6f5c22a60d2830496c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045a468e3f64ef6078d1ad0e91b3c7c3410eba4b86e0f19e58de4a79c943fbe4`  
		Last Modified: Fri, 29 Aug 2025 18:58:09 GMT  
		Size: 83.2 MB (83183184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd71a380ffd5bdf2c24926cc53a053ce7702bcc2cd91ddc403cae22324d9013`  
		Last Modified: Fri, 29 Aug 2025 18:58:03 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7e5688565f7d12c50095b16053ccd03b6bbd73eccbc3ad67630e5af409894`  
		Last Modified: Fri, 29 Aug 2025 18:58:03 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:91b2780598d19fbfd5c2338ca231d9f798365da615c4b783a2c02eb230cf5340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ed2508357c088e800ceb6ab07a53c0d770560c6445f872add3ffaaa706e172`

```dockerfile
```

-	Layers:
	-	`sha256:9d50147cb40bae096e956219787393ef28d1de2bad15ebe6f44b95d5de4b4f42`  
		Last Modified: Fri, 29 Aug 2025 21:19:45 GMT  
		Size: 19.6 KB (19623 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; ppc64le

```console
$ docker pull varnish@sha256:fb93b07d38aa9c60ef29f22da422d0bf4db0ab2a36fb584e15da11e2fc855b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111785588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cc1ecc30191b0e4f6019dd9e57152f7ceeb6cef146cd1f71f6912df8fe2a41`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeaa7de33323e9da003d76c1a5cc0bb86f35d215429e0d9f20b652378d97952`  
		Last Modified: Fri, 29 Aug 2025 19:00:08 GMT  
		Size: 78.2 MB (78189327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e630fc6d39e8589329e37f5a61e56e9ebfc7eeca0d40411c39bcc2bfccaae5e`  
		Last Modified: Fri, 29 Aug 2025 18:59:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ad6337d770f926d12752f7f661984d17f9c36353f6a8ebb231a5ad950de3b`  
		Last Modified: Fri, 29 Aug 2025 18:59:58 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:6533ac132bd0b294ecfc3638cc8b04c2ab50ca74d45046cfffa7d442aefd5f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ad9d848ff9f848e7dee20ff109298b8e870674df25d11405b571e816436923`

```dockerfile
```

-	Layers:
	-	`sha256:2de9a81e8b94b8729ba0c57f208af387d8dc241d788317f3097bf40bd0628bec`  
		Last Modified: Fri, 29 Aug 2025 21:19:48 GMT  
		Size: 19.7 KB (19707 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; s390x

```console
$ docker pull varnish@sha256:316e16056f396da312924e65681e867878b12ffbd091bec4b8bfbdcab3d2e757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93293676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644c7b17565ef9c3c605d4da40e1fde193cbb69da7fe5eec550f1ccc75788f0a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1660409013e5bbfdf7e7587ce45ef14ffbe6f4f1ddf9e2334a36aa2db6abc0e`  
		Last Modified: Fri, 29 Aug 2025 18:59:41 GMT  
		Size: 63.5 MB (63458571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075bbb82d37082573ab3e19d8791666edde05284ddf8f73f45bde1f03eed1d9`  
		Last Modified: Fri, 29 Aug 2025 18:59:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683e60bd286912e7a79cfb7dc558aef4ee7e621471a31ad8194f8e80357adc97`  
		Last Modified: Fri, 29 Aug 2025 18:59:33 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:99ce5f6dcbc57b14b71f0a9f3990b5f6a78c7e76cb46fa68e49feab34553fdc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd53bd2f0c8cf8cb92f86f286a45d39252faa5929bae160e1e0e5bfdc3e0021`

```dockerfile
```

-	Layers:
	-	`sha256:b4508a75879abdd43a4e164b930d4eb6ab29efba0488ae7ed5c37f3bc5c2afb5`  
		Last Modified: Fri, 29 Aug 2025 21:19:52 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7-alpine`

```console
$ docker pull varnish@sha256:0297e4e6f7ad8e91e4079ca4cb6376c0c6cd0816a603f9783d6d180418a5ace3
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
$ docker pull varnish@sha256:968def097e04e840a52a0cb40523f6cacd02479fe1a103aa1f4faf7020a486b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (82993733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c796b0bf4f6d6821900c2b96f9582996ec10f4f95e899e8ae26e07702148ff3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8688839e5a15188a72647a6852b7152ef71c649b254a011229a90a62fbed8fa`  
		Last Modified: Tue, 26 Aug 2025 16:51:07 GMT  
		Size: 79.2 MB (79191987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd3ba927190043e8f707e6fbd55db714f6ac35cbab88b3eeddfdc1d840bbfd`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0f04afb274482621be87eefe109335897a4ebe2d1356e3796b6ec13f7f2972`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:709a0910bc16cef04b2c634e8e1a9509f6f9d413f8774bf7047aad42b295fea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9d84eee2afb88887b41c9affc9147bd2db2e6d68070444d70b697ff6cc98f8`

```dockerfile
```

-	Layers:
	-	`sha256:35a32c7db6c318b475a81a7c92e3a96e4c331f31f14454cb7028d5768e880e71`  
		Last Modified: Tue, 26 Aug 2025 18:20:08 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:36313eff0334c42ea63ea530d129fd890b761c6a5fc6f3e4b0b791db0d0a2ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64456549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5063718db8c89c5c461727031efaa74768e5b3c1f6e767ca1cf041d4c83cedf9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae3a3450a898d7d7936a3449f5213067234680cc45f3c4dd8f008c7773f78cc`  
		Last Modified: Tue, 26 Aug 2025 17:32:17 GMT  
		Size: 61.2 MB (61235455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e2bc7a31f1eb52a19ed696c0b64c8e7df06c9ced0074bcc2c6484f6ad392a7`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304012d451fc4a526211049f43cc247c6f5565043478a91325056f52f8460652`  
		Last Modified: Tue, 26 Aug 2025 16:53:16 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:99789fd7694d7a402ae33b0d7ebbcf050020c9e7ebb1860b42099fb85a215796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa12d2a02e6aad7f79d2946e4ac6338e60254980ab67d201502ed9c2c97edf87`

```dockerfile
```

-	Layers:
	-	`sha256:a7e234a9b635e5b641a9c4bfba4a4bf34f743409faa16595478e49e0704f0367`  
		Last Modified: Tue, 26 Aug 2025 18:20:12 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:6bea3798e0b800d4b6247ce3665ba08e129ff7da73ecc13df8fa9bbdffac6822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80275423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a471b03fd084177f8b271299dc3945678572500224adaa9c8118d6e66e4d26`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4b9c79e8f0d02f79a5b5986ebbeb895a5f1752ed163e203317cdc36729b386`  
		Last Modified: Tue, 26 Aug 2025 16:53:20 GMT  
		Size: 76.1 MB (76142615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cdc7619db5c8841bd4974b23b8bd4245c5077f14582530fd9db0e8a59ca0c1`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aed738cbed2c0ea53daa581f1639bd962a3d050ae5600e2e382f710df03870`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:05157ea69a9a6d3ae3be9a75ebfa4134cf0d66132050502419874cc7e76e873c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aef9306982c345cb47205fc2a23f2d9b7c11799193e2a0671a52cc948a6f1cc`

```dockerfile
```

-	Layers:
	-	`sha256:a9a1d37c8443d12093423197a6946305dc2506e30d6e330a9a45d4f331c28072`  
		Last Modified: Tue, 26 Aug 2025 18:20:16 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:ea9aa4a49f609489b627aed9356a5873cbbdb96e02c249e6ec51ce97aa8f7e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85001515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c9237f024910b41b25a64734d559f0d5c513ba4caaba586658fbc4fdb23d7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2ed555a42edaaa80f0729b321774d3bff810ae570d3b3be84f458544f1650a`  
		Last Modified: Tue, 26 Aug 2025 16:51:40 GMT  
		Size: 81.4 MB (81384451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc952cfe554ff9395699f7f3435db2ede214f1f2ddb49051b3fcc2d7d9574e3c`  
		Last Modified: Tue, 26 Aug 2025 16:51:30 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42d19e5629e404b539dea7a92dd4e1c28fb152ac4fd387f335112d967fa42bf`  
		Last Modified: Tue, 26 Aug 2025 16:51:24 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1ca2dfd325862cf53869f98b54b6f269ff3825c7252e5b75a53ee4d34e31056d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580baac8e15bdc972db7c72085205331fa315a8f8220664084639bbaa46e484f`

```dockerfile
```

-	Layers:
	-	`sha256:4420a9c08aeaace20f6102f79d7704bd2d2d759ad92e107297a5e3b71f8c6b35`  
		Last Modified: Tue, 26 Aug 2025 18:20:20 GMT  
		Size: 19.4 KB (19431 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:82af53ff59713b0b3586af4f2977b2d5ab7df673be720e9037f0df2f5c726749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78963604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e699f34e611ec9aeac4b9938dcf600cb3d115e33cdc619e45b1006461b9ef15f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7d2a57f1ef9f97b49b6fff28a7126d97e7198d9c67b1f4d38730c945b55a7`  
		Last Modified: Tue, 26 Aug 2025 17:44:40 GMT  
		Size: 75.2 MB (75234430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bbc6a66435fbe346aedb5478520c0031df4d574bfe13b98d36123bd0cb1522`  
		Last Modified: Tue, 26 Aug 2025 16:57:41 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455ca0fa6d5a336db59bff2f1f594bb7899650b7763648479f824021cffa2a7`  
		Last Modified: Tue, 26 Aug 2025 16:57:44 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:582db1db9c028422995048d09a52f5f13e30d4a775813f9e7722c3c2105907f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3351982c781fc09f6de5ff55d9239383b65c53221e66d9276d7d3b08204962`

```dockerfile
```

-	Layers:
	-	`sha256:962692efb06cc7405e9986b44b7931d8c5120419ab4aace742096f778b04db3c`  
		Last Modified: Tue, 26 Aug 2025 18:20:23 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:7112d826a48691fd016859332f9fee9f351e69dbc356b59861aecf05372c7621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73520274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f1caf4dd71bd936b7e54525ae5ae07a1da8ae4899f5e60d3b22e024f31aff0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495f345eb737fe5e7f7d583c0f6630cf80a4d67b95ae9bd76902dde2dba9d51b`  
		Last Modified: Tue, 26 Aug 2025 17:04:01 GMT  
		Size: 69.9 MB (69873239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c307bbaffedd8c00cddb99e59f7d3697e3e731371404ac5e8955508c13d7a93`  
		Last Modified: Tue, 26 Aug 2025 17:03:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415def403d1cc7b5626e73089336be57199faba9279eb128d414f71dae0fad10`  
		Last Modified: Tue, 26 Aug 2025 17:03:52 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6b5f52d363112af7587ab99319549299d91a096b9a38dace51b58f53be34cbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74086b67192616f0b1ee67becd30f028625db9af6ee7fe3897946a283917d80`

```dockerfile
```

-	Layers:
	-	`sha256:921ec808b8a72d9cbe23454e94ef9fb544514404bf06c731e043eed5f4e2025b`  
		Last Modified: Tue, 26 Aug 2025 18:20:27 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6`

```console
$ docker pull varnish@sha256:2862d218eaf5174ed6c49d05cdec7c541ac1cd187eff4525857a72e20532cf39
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
$ docker pull varnish@sha256:45296ae674b736210082997b7c92da397841d1b21196a7f10d9cf5614a61d8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116169441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94fece8572b82c77fa999a9ccf45183eb0ababb78b941c08a8006f14fc7d0f0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aafdc0f6845c6314758ea5569b830d13c704e4189855dafb5cbdc30b9169991`  
		Last Modified: Fri, 29 Aug 2025 18:58:02 GMT  
		Size: 86.4 MB (86394109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ac55296cc05f4f50014679cd428d83c67bb46c4c226898f5a7783ecc0600b`  
		Last Modified: Fri, 29 Aug 2025 18:57:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f32565fad2ea9070650b9b05ff19f924c6493c601cc3958918694e5f4e150e`  
		Last Modified: Fri, 29 Aug 2025 18:57:55 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:3806a133bb59adf5a8b56ee1c34c23fa3c07c7d5eb5b92d9102205def82ba2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079ac8dae3eced627c6b98a34fb082e3c966fc3aa1ca001ecf0f2bb00d0484bc`

```dockerfile
```

-	Layers:
	-	`sha256:e33a69edbbad8d863cae61e0a295cb7c61e461e870f5de66530c76d4b16130f0`  
		Last Modified: Fri, 29 Aug 2025 21:19:51 GMT  
		Size: 19.1 KB (19075 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm variant v7

```console
$ docker pull varnish@sha256:905e492b4e13eb2216f2f7be0e6f0eb98f6dab06a21bd6211ec56ded65e46a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86981619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e693710bbc6b9a8085271f2a15abae7c9b2efb4eba4e9db0beac0dfd1c46dd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1d4dd19271e3d461300ca6edbd2f656818c6c3122611f8fb62ffa8e3da5ed4`  
		Last Modified: Fri, 29 Aug 2025 19:00:55 GMT  
		Size: 60.8 MB (60772084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4746b95aa20b62727e54e73688f9e148c9b15e047d1a4cdac39dd1c8356bab70`  
		Last Modified: Fri, 29 Aug 2025 19:00:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4444a7b8087b688e02877dbd3a852ebd2748592c8466d92392d4309aa3b58d0`  
		Last Modified: Fri, 29 Aug 2025 19:00:42 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:feeaf6e2216511f5cb0931304b8cc4ad9fd78fc60277a7f21f54573ea5b5351a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c63228a3d2f58f0204922e78f1554c95d832be32519d9704cab53205159eba1`

```dockerfile
```

-	Layers:
	-	`sha256:569114f4cb82d4b50d18d99e1ca84fe00b7d9d6fad4a133168924a7ec0c826fc`  
		Last Modified: Fri, 29 Aug 2025 21:19:54 GMT  
		Size: 19.1 KB (19143 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:da7bf990f6f149f133218eaba42fda8f69d5c7d908f65deb6103e3d6d83472e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110350109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5d5e9cd9206075ebc9797665e6bb2f3f2ce2f88c2018f3ae5a0a8f1eaa6346`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e19e1a0efaedfe6217ed6bdf97d04d1b5b6cc3aa4a0f669711965a64be863a`  
		Last Modified: Fri, 29 Aug 2025 19:00:24 GMT  
		Size: 80.2 MB (80212023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8654c06c0ddb58abe0f594dca4fcdb1728cbe2e1d0caef544ba713fe7a2d529`  
		Last Modified: Fri, 29 Aug 2025 19:00:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3f62c8866ff29110155eceb7a782254918b48828d870a48e691d67a83e3f91`  
		Last Modified: Fri, 29 Aug 2025 19:00:11 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:422a5d4fc5d7016171bf07ed7e576ed64246e05d374655bb32339d8b393195db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad6a88f8ad6c6a75b72da680a295cc214d53376c4aefecc2826744a357d14bc`

```dockerfile
```

-	Layers:
	-	`sha256:592b08a80afb3bd747f044210fbe7084608be8cde41c318ffb61de7ae47d6cf2`  
		Last Modified: Fri, 29 Aug 2025 21:19:57 GMT  
		Size: 19.2 KB (19167 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; 386

```console
$ docker pull varnish@sha256:9b49c255a79105f56f9f5930bcbd148523616237ddd78656e3c61458513d62e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114331197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4116ea46ebe15c9fea54ea1919c19987809aa823bacb07b1e4166c4a1a2d6f7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b653d48e2ed0ae22132c116eeca0327ea1253db2ee63f7506f7db701030256be`  
		Last Modified: Fri, 29 Aug 2025 18:58:50 GMT  
		Size: 83.0 MB (83039775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ac55296cc05f4f50014679cd428d83c67bb46c4c226898f5a7783ecc0600b`  
		Last Modified: Fri, 29 Aug 2025 18:57:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccdd71e25e36e6758a960942ca184e20826dc86cb04b04b3dbb79ca43ab4c10`  
		Last Modified: Fri, 29 Aug 2025 18:58:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:03dc1fb688bec5b31b14c0fb39e85e423737a222c2fb7b515f1cc0bdd6af2af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba3f6cbb7e8ef245c726b1211b502a9a017c0c30a3fa46707aa4da405e25740`

```dockerfile
```

-	Layers:
	-	`sha256:a44a961b7acc357e6833e76c5a61a7dfc154ccb0d4fa806338360892871b9cd8`  
		Last Modified: Fri, 29 Aug 2025 21:20:01 GMT  
		Size: 19.0 KB (19048 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; ppc64le

```console
$ docker pull varnish@sha256:501a25b09de46b5f821a4e43eace76ac3c59a1362c4f00a1f51525fadd32af7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111630089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d8372da09852672b9e8816ad943089c72905e765f71e364b566d8a21154130`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc13e4d48b41dfde630a9184655d018075902d953333b8347d5e348aa2874b87`  
		Last Modified: Fri, 29 Aug 2025 19:05:06 GMT  
		Size: 78.0 MB (78033829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169a0308b68f5f63e4c023d0c237261658b1eb70ed4e8b25f52b9b368da9b2f`  
		Last Modified: Fri, 29 Aug 2025 19:04:42 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a89a4d3f2bba8425dff2502e1a9b435355b176779a746e8e641f331ac3fdab`  
		Last Modified: Fri, 29 Aug 2025 19:04:42 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:44c717ee96fe1d79666cef219924bc97d7f5b5c3a6003a4b9641ec16ea92d4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e5eca42e31c466851d0633577843ac2652ddb028674e38bffb915937215a74`

```dockerfile
```

-	Layers:
	-	`sha256:78fca917015de0b7d224792b961841e954aaef88c18e016747b0715d79a0f604`  
		Last Modified: Fri, 29 Aug 2025 21:20:04 GMT  
		Size: 19.1 KB (19113 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; s390x

```console
$ docker pull varnish@sha256:2909c1b4f47f219d0ed74649743f21b8be5a06c35eaddbe908c8ba00f8c743b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93129994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49672459310fe0bb3e4d4efaf09c70046db0cb27cded27c50d68ca3f142284e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176a7536be148e977a8fdc806980aa397eaf18445c550378857fcf89f803c2ac`  
		Last Modified: Fri, 29 Aug 2025 19:02:40 GMT  
		Size: 63.3 MB (63294891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a31f08be4a52e37428db003901e499cb1dbf9a15270aa06d7797ad13e67c39`  
		Last Modified: Fri, 29 Aug 2025 19:02:36 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd2421d3d30817464293d1d84d3eedc207d3286aa8053b81012857a25c65f7d`  
		Last Modified: Fri, 29 Aug 2025 19:02:36 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:61d2019a87faf880b4aa272a56f6d19485b2f1be336f00a96f408975507f2063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f20c86647a60b61f3bb2231c7999f7b2afe10a3645fd31e0f785fdd382a648`

```dockerfile
```

-	Layers:
	-	`sha256:c713214ddad6a75eb6c994aa47b946374068799725ab8856885bf7df602a7b28`  
		Last Modified: Fri, 29 Aug 2025 21:20:07 GMT  
		Size: 19.1 KB (19075 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6-alpine`

```console
$ docker pull varnish@sha256:eb21e9f988be93f33ff9a0025d0a00617d49f3cc0cf59e0f2167bde7724eae6a
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
$ docker pull varnish@sha256:eb59c7c733b51c1b939cbf9ff520c263bc0c9299508d387e2c19d9df44ca052e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82842456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ba779d3e802e8d23096c4540664cc96d8536959d5b074aa304623851eb7b6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d21ba25e42c221c38da4178d142633a0f4b5df2ea8c3f3d106f42d0b10b443`  
		Last Modified: Tue, 26 Aug 2025 16:51:04 GMT  
		Size: 79.0 MB (79040710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da539f12306b86eb6f4852b5fc70b75a09cef49e31798ad611f63cc267c02be4`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4cd983d1fb0f0789a1a89e664b291a4a4661ccc517311755de1f6948133737`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:cca42d774f271c82579cabffc4db3bfc1035ac3771304e71f720aec531157efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b7b3c041668a547dc1bbb7950733445e113d810c45c9270e7a06ec1477f0bb`

```dockerfile
```

-	Layers:
	-	`sha256:352b25a10911cee1af8da5fbe36f12ae99a4566e98353faca1c19a1dba719b8a`  
		Last Modified: Tue, 26 Aug 2025 18:20:34 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a45549c23c64999161d2144378f8972638bb135b9ae2a82f7a9c677827bf5ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64309206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2054d8cf53e95e19697765491d67a689b3bf8bbd4c17141d0793f38d883f13`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df002cf37151e7b0fa6b77dce491cac03f0f43e0787475b1164effafe412756`  
		Last Modified: Tue, 26 Aug 2025 16:52:10 GMT  
		Size: 61.1 MB (61088108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8f13ade0c407bc30c2d0943af75f6686574b0f26d379104e3c205bf45afc9a`  
		Last Modified: Tue, 26 Aug 2025 16:52:04 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1122e1df195890d89e2ce223091d4fdbf016c09a99097ad0d2800e51f1c1b614`  
		Last Modified: Tue, 26 Aug 2025 16:52:08 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e2ab0e3e19ebf7c6ca62c6b44d5ebcf558dae64f334ad28c878643af087cdd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cf4ba26c47448e64139df64da0a0b9fe67159038b3408e9b09817f12aeef0e`

```dockerfile
```

-	Layers:
	-	`sha256:ce92da7aee86b3186c4df792b992aad5793b0bd68a2cf58e2c87edf2d1ca25c1`  
		Last Modified: Tue, 26 Aug 2025 18:20:39 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cc7a4c790e15bf6bf5226b0d410417ec9f531d5a753110a66b5ab276c31d529f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80124371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcffa3fc8649cd6ecd6bf2901185697844222260efa02f05e99731db0afe6372`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61af1543a395f4ec8e503d693e122083a940bf2bb76d515063e5143006014daf`  
		Last Modified: Tue, 26 Aug 2025 18:21:12 GMT  
		Size: 76.0 MB (75991566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12d13ffdec5777bc9a087e7b6a7648c20098407baf88c27c9e7fe4aac7d8762`  
		Last Modified: Tue, 26 Aug 2025 17:10:48 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829db24f940156af11f84479793cc2a0a0cfe14343815b44983b6afde47268a1`  
		Last Modified: Tue, 26 Aug 2025 17:10:51 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:0ccbeff7dbfb12f5d18c9f0cd5717acfb9ad1edf5aa9e6b00ad5b3b40c42d048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eb6f4dd4f15da4e733fba7d1e89c9f575efa966c077245df747443c718e3f9`

```dockerfile
```

-	Layers:
	-	`sha256:2a51627e99e6e144059176acd8432da0742e66b7680ad3e45c9b5b7b842abd83`  
		Last Modified: Tue, 26 Aug 2025 18:20:42 GMT  
		Size: 18.9 KB (18910 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; 386

```console
$ docker pull varnish@sha256:79de57822067c316205cf516f35730d9a48eba17a18438068b7f040a24ac3b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84867078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5504cbcd55267abd7eb20a78d9b5a7b750049aa4bc605904f43a56800e28e91b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8566fc257dd8fe62b706fceeac74d505c8d4f452f47443ab24c056b45d36a39`  
		Last Modified: Tue, 26 Aug 2025 16:51:00 GMT  
		Size: 81.3 MB (81250013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c902672d8239c81bbf78276bf948224102a95c14aa1c3425a2cd8d61ac8e72`  
		Last Modified: Tue, 26 Aug 2025 16:50:52 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b659f1d057b1bc172c204ef2be2e113d569f720ff55a3eede5412aa84a492b`  
		Last Modified: Tue, 26 Aug 2025 16:50:53 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:18c78749465acc21014ef75082ab645316c03195ac2240e39400c554dc25c080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745deeff47c188553c23284121381997db93b89c2f4f6a3ef25a5fde1cd3a4cc`

```dockerfile
```

-	Layers:
	-	`sha256:a0fa618125b27a4ad09d1553205573bf7cc3d05fe296ae1a5916418c2bef17b2`  
		Last Modified: Tue, 26 Aug 2025 18:20:46 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:edff5c8cf592568cd0c8a1791adb5a4c7038630e2396a74f30fbc286cc02d57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78817937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4e4f81bdc94adfb2b152c4986a786099e213c8872a0a447de1940eec8b36b9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41580bfa7bb549e94995896f5201eb9cea1494505ab84bd2126449b3a80d8788`  
		Last Modified: Tue, 26 Aug 2025 17:05:11 GMT  
		Size: 75.1 MB (75088762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf19c428ddd5472d5705df46e95a523161488ca0d2e70ca9bebd0089f1c233e`  
		Last Modified: Tue, 26 Aug 2025 17:05:02 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf0cd2ebebd5e2b3680f333eeeea9e24af8c1deab3442ac0419289d59b88528`  
		Last Modified: Tue, 26 Aug 2025 17:05:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a97e2c5ce5f5ae8715cfb5aa54bd600ceda8d156a4d95fe1b69ffe7160544d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd36779ff7171b497584aecf1336f80b2271cbe770dfffecab9b37499691c10d`

```dockerfile
```

-	Layers:
	-	`sha256:4e868d107d4ec0f88f2515d8c0e461129f2d4c2412b6465284b4d66c9941ba81`  
		Last Modified: Tue, 26 Aug 2025 18:20:49 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:6bc7c34f4a8c82a84964269ceb7da23eadc1bfbc06e1dd164456a4a7c5a8f064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73373120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7df50cfa2eacca4e44264105844791df8f7c91eb09af124a198445860554b81`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d347e847918994143d8709387f507640aec9549648f4ab8dd0dafaf35cda058`  
		Last Modified: Tue, 26 Aug 2025 17:17:15 GMT  
		Size: 69.7 MB (69726086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564bf67e3d60e0acd5d9612a5dc1bea2c8e30ed426161ea842a2c7203a7aa9f8`  
		Last Modified: Tue, 26 Aug 2025 17:17:08 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e8e125440740ba86e9c177b062cd9e2f77e2e8a5baecdf2b9627697318b17e`  
		Last Modified: Tue, 26 Aug 2025 17:17:08 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2040c4c901971ec2aa62d7f20a30a283a3855e4e980e1567c742de35e05f9d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb0b839668077db2d493c4e6f89335931c594587b4958d1d9f5c3171fab912c`

```dockerfile
```

-	Layers:
	-	`sha256:94a86035ec439c327f30139139dfafa0ae939c638319e9658f08da45c2eed1a3`  
		Last Modified: Tue, 26 Aug 2025 18:20:53 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.5`

```console
$ docker pull varnish@sha256:2862d218eaf5174ed6c49d05cdec7c541ac1cd187eff4525857a72e20532cf39
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

### `varnish:7.6.5` - linux; amd64

```console
$ docker pull varnish@sha256:45296ae674b736210082997b7c92da397841d1b21196a7f10d9cf5614a61d8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116169441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94fece8572b82c77fa999a9ccf45183eb0ababb78b941c08a8006f14fc7d0f0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aafdc0f6845c6314758ea5569b830d13c704e4189855dafb5cbdc30b9169991`  
		Last Modified: Fri, 29 Aug 2025 18:58:02 GMT  
		Size: 86.4 MB (86394109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ac55296cc05f4f50014679cd428d83c67bb46c4c226898f5a7783ecc0600b`  
		Last Modified: Fri, 29 Aug 2025 18:57:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f32565fad2ea9070650b9b05ff19f924c6493c601cc3958918694e5f4e150e`  
		Last Modified: Fri, 29 Aug 2025 18:57:55 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5` - unknown; unknown

```console
$ docker pull varnish@sha256:3806a133bb59adf5a8b56ee1c34c23fa3c07c7d5eb5b92d9102205def82ba2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079ac8dae3eced627c6b98a34fb082e3c966fc3aa1ca001ecf0f2bb00d0484bc`

```dockerfile
```

-	Layers:
	-	`sha256:e33a69edbbad8d863cae61e0a295cb7c61e461e870f5de66530c76d4b16130f0`  
		Last Modified: Fri, 29 Aug 2025 21:19:51 GMT  
		Size: 19.1 KB (19075 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5` - linux; arm variant v7

```console
$ docker pull varnish@sha256:905e492b4e13eb2216f2f7be0e6f0eb98f6dab06a21bd6211ec56ded65e46a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86981619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e693710bbc6b9a8085271f2a15abae7c9b2efb4eba4e9db0beac0dfd1c46dd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1d4dd19271e3d461300ca6edbd2f656818c6c3122611f8fb62ffa8e3da5ed4`  
		Last Modified: Fri, 29 Aug 2025 19:00:55 GMT  
		Size: 60.8 MB (60772084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4746b95aa20b62727e54e73688f9e148c9b15e047d1a4cdac39dd1c8356bab70`  
		Last Modified: Fri, 29 Aug 2025 19:00:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4444a7b8087b688e02877dbd3a852ebd2748592c8466d92392d4309aa3b58d0`  
		Last Modified: Fri, 29 Aug 2025 19:00:42 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5` - unknown; unknown

```console
$ docker pull varnish@sha256:feeaf6e2216511f5cb0931304b8cc4ad9fd78fc60277a7f21f54573ea5b5351a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c63228a3d2f58f0204922e78f1554c95d832be32519d9704cab53205159eba1`

```dockerfile
```

-	Layers:
	-	`sha256:569114f4cb82d4b50d18d99e1ca84fe00b7d9d6fad4a133168924a7ec0c826fc`  
		Last Modified: Fri, 29 Aug 2025 21:19:54 GMT  
		Size: 19.1 KB (19143 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:da7bf990f6f149f133218eaba42fda8f69d5c7d908f65deb6103e3d6d83472e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110350109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5d5e9cd9206075ebc9797665e6bb2f3f2ce2f88c2018f3ae5a0a8f1eaa6346`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e19e1a0efaedfe6217ed6bdf97d04d1b5b6cc3aa4a0f669711965a64be863a`  
		Last Modified: Fri, 29 Aug 2025 19:00:24 GMT  
		Size: 80.2 MB (80212023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8654c06c0ddb58abe0f594dca4fcdb1728cbe2e1d0caef544ba713fe7a2d529`  
		Last Modified: Fri, 29 Aug 2025 19:00:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3f62c8866ff29110155eceb7a782254918b48828d870a48e691d67a83e3f91`  
		Last Modified: Fri, 29 Aug 2025 19:00:11 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5` - unknown; unknown

```console
$ docker pull varnish@sha256:422a5d4fc5d7016171bf07ed7e576ed64246e05d374655bb32339d8b393195db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad6a88f8ad6c6a75b72da680a295cc214d53376c4aefecc2826744a357d14bc`

```dockerfile
```

-	Layers:
	-	`sha256:592b08a80afb3bd747f044210fbe7084608be8cde41c318ffb61de7ae47d6cf2`  
		Last Modified: Fri, 29 Aug 2025 21:19:57 GMT  
		Size: 19.2 KB (19167 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5` - linux; 386

```console
$ docker pull varnish@sha256:9b49c255a79105f56f9f5930bcbd148523616237ddd78656e3c61458513d62e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114331197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4116ea46ebe15c9fea54ea1919c19987809aa823bacb07b1e4166c4a1a2d6f7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b653d48e2ed0ae22132c116eeca0327ea1253db2ee63f7506f7db701030256be`  
		Last Modified: Fri, 29 Aug 2025 18:58:50 GMT  
		Size: 83.0 MB (83039775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ac55296cc05f4f50014679cd428d83c67bb46c4c226898f5a7783ecc0600b`  
		Last Modified: Fri, 29 Aug 2025 18:57:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccdd71e25e36e6758a960942ca184e20826dc86cb04b04b3dbb79ca43ab4c10`  
		Last Modified: Fri, 29 Aug 2025 18:58:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5` - unknown; unknown

```console
$ docker pull varnish@sha256:03dc1fb688bec5b31b14c0fb39e85e423737a222c2fb7b515f1cc0bdd6af2af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba3f6cbb7e8ef245c726b1211b502a9a017c0c30a3fa46707aa4da405e25740`

```dockerfile
```

-	Layers:
	-	`sha256:a44a961b7acc357e6833e76c5a61a7dfc154ccb0d4fa806338360892871b9cd8`  
		Last Modified: Fri, 29 Aug 2025 21:20:01 GMT  
		Size: 19.0 KB (19048 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5` - linux; ppc64le

```console
$ docker pull varnish@sha256:501a25b09de46b5f821a4e43eace76ac3c59a1362c4f00a1f51525fadd32af7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111630089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d8372da09852672b9e8816ad943089c72905e765f71e364b566d8a21154130`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc13e4d48b41dfde630a9184655d018075902d953333b8347d5e348aa2874b87`  
		Last Modified: Fri, 29 Aug 2025 19:05:06 GMT  
		Size: 78.0 MB (78033829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169a0308b68f5f63e4c023d0c237261658b1eb70ed4e8b25f52b9b368da9b2f`  
		Last Modified: Fri, 29 Aug 2025 19:04:42 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a89a4d3f2bba8425dff2502e1a9b435355b176779a746e8e641f331ac3fdab`  
		Last Modified: Fri, 29 Aug 2025 19:04:42 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5` - unknown; unknown

```console
$ docker pull varnish@sha256:44c717ee96fe1d79666cef219924bc97d7f5b5c3a6003a4b9641ec16ea92d4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e5eca42e31c466851d0633577843ac2652ddb028674e38bffb915937215a74`

```dockerfile
```

-	Layers:
	-	`sha256:78fca917015de0b7d224792b961841e954aaef88c18e016747b0715d79a0f604`  
		Last Modified: Fri, 29 Aug 2025 21:20:04 GMT  
		Size: 19.1 KB (19113 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5` - linux; s390x

```console
$ docker pull varnish@sha256:2909c1b4f47f219d0ed74649743f21b8be5a06c35eaddbe908c8ba00f8c743b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93129994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49672459310fe0bb3e4d4efaf09c70046db0cb27cded27c50d68ca3f142284e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176a7536be148e977a8fdc806980aa397eaf18445c550378857fcf89f803c2ac`  
		Last Modified: Fri, 29 Aug 2025 19:02:40 GMT  
		Size: 63.3 MB (63294891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a31f08be4a52e37428db003901e499cb1dbf9a15270aa06d7797ad13e67c39`  
		Last Modified: Fri, 29 Aug 2025 19:02:36 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd2421d3d30817464293d1d84d3eedc207d3286aa8053b81012857a25c65f7d`  
		Last Modified: Fri, 29 Aug 2025 19:02:36 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5` - unknown; unknown

```console
$ docker pull varnish@sha256:61d2019a87faf880b4aa272a56f6d19485b2f1be336f00a96f408975507f2063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f20c86647a60b61f3bb2231c7999f7b2afe10a3645fd31e0f785fdd382a648`

```dockerfile
```

-	Layers:
	-	`sha256:c713214ddad6a75eb6c994aa47b946374068799725ab8856885bf7df602a7b28`  
		Last Modified: Fri, 29 Aug 2025 21:20:07 GMT  
		Size: 19.1 KB (19075 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.6.5-alpine`

```console
$ docker pull varnish@sha256:eb21e9f988be93f33ff9a0025d0a00617d49f3cc0cf59e0f2167bde7724eae6a
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

### `varnish:7.6.5-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:eb59c7c733b51c1b939cbf9ff520c263bc0c9299508d387e2c19d9df44ca052e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82842456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ba779d3e802e8d23096c4540664cc96d8536959d5b074aa304623851eb7b6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d21ba25e42c221c38da4178d142633a0f4b5df2ea8c3f3d106f42d0b10b443`  
		Last Modified: Tue, 26 Aug 2025 16:51:04 GMT  
		Size: 79.0 MB (79040710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da539f12306b86eb6f4852b5fc70b75a09cef49e31798ad611f63cc267c02be4`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4cd983d1fb0f0789a1a89e664b291a4a4661ccc517311755de1f6948133737`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:cca42d774f271c82579cabffc4db3bfc1035ac3771304e71f720aec531157efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b7b3c041668a547dc1bbb7950733445e113d810c45c9270e7a06ec1477f0bb`

```dockerfile
```

-	Layers:
	-	`sha256:352b25a10911cee1af8da5fbe36f12ae99a4566e98353faca1c19a1dba719b8a`  
		Last Modified: Tue, 26 Aug 2025 18:20:34 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a45549c23c64999161d2144378f8972638bb135b9ae2a82f7a9c677827bf5ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64309206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2054d8cf53e95e19697765491d67a689b3bf8bbd4c17141d0793f38d883f13`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df002cf37151e7b0fa6b77dce491cac03f0f43e0787475b1164effafe412756`  
		Last Modified: Tue, 26 Aug 2025 16:52:10 GMT  
		Size: 61.1 MB (61088108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8f13ade0c407bc30c2d0943af75f6686574b0f26d379104e3c205bf45afc9a`  
		Last Modified: Tue, 26 Aug 2025 16:52:04 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1122e1df195890d89e2ce223091d4fdbf016c09a99097ad0d2800e51f1c1b614`  
		Last Modified: Tue, 26 Aug 2025 16:52:08 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e2ab0e3e19ebf7c6ca62c6b44d5ebcf558dae64f334ad28c878643af087cdd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cf4ba26c47448e64139df64da0a0b9fe67159038b3408e9b09817f12aeef0e`

```dockerfile
```

-	Layers:
	-	`sha256:ce92da7aee86b3186c4df792b992aad5793b0bd68a2cf58e2c87edf2d1ca25c1`  
		Last Modified: Tue, 26 Aug 2025 18:20:39 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cc7a4c790e15bf6bf5226b0d410417ec9f531d5a753110a66b5ab276c31d529f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80124371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcffa3fc8649cd6ecd6bf2901185697844222260efa02f05e99731db0afe6372`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61af1543a395f4ec8e503d693e122083a940bf2bb76d515063e5143006014daf`  
		Last Modified: Tue, 26 Aug 2025 18:21:12 GMT  
		Size: 76.0 MB (75991566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12d13ffdec5777bc9a087e7b6a7648c20098407baf88c27c9e7fe4aac7d8762`  
		Last Modified: Tue, 26 Aug 2025 17:10:48 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829db24f940156af11f84479793cc2a0a0cfe14343815b44983b6afde47268a1`  
		Last Modified: Tue, 26 Aug 2025 17:10:51 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:0ccbeff7dbfb12f5d18c9f0cd5717acfb9ad1edf5aa9e6b00ad5b3b40c42d048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eb6f4dd4f15da4e733fba7d1e89c9f575efa966c077245df747443c718e3f9`

```dockerfile
```

-	Layers:
	-	`sha256:2a51627e99e6e144059176acd8432da0742e66b7680ad3e45c9b5b7b842abd83`  
		Last Modified: Tue, 26 Aug 2025 18:20:42 GMT  
		Size: 18.9 KB (18910 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5-alpine` - linux; 386

```console
$ docker pull varnish@sha256:79de57822067c316205cf516f35730d9a48eba17a18438068b7f040a24ac3b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84867078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5504cbcd55267abd7eb20a78d9b5a7b750049aa4bc605904f43a56800e28e91b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8566fc257dd8fe62b706fceeac74d505c8d4f452f47443ab24c056b45d36a39`  
		Last Modified: Tue, 26 Aug 2025 16:51:00 GMT  
		Size: 81.3 MB (81250013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c902672d8239c81bbf78276bf948224102a95c14aa1c3425a2cd8d61ac8e72`  
		Last Modified: Tue, 26 Aug 2025 16:50:52 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b659f1d057b1bc172c204ef2be2e113d569f720ff55a3eede5412aa84a492b`  
		Last Modified: Tue, 26 Aug 2025 16:50:53 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:18c78749465acc21014ef75082ab645316c03195ac2240e39400c554dc25c080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745deeff47c188553c23284121381997db93b89c2f4f6a3ef25a5fde1cd3a4cc`

```dockerfile
```

-	Layers:
	-	`sha256:a0fa618125b27a4ad09d1553205573bf7cc3d05fe296ae1a5916418c2bef17b2`  
		Last Modified: Tue, 26 Aug 2025 18:20:46 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:edff5c8cf592568cd0c8a1791adb5a4c7038630e2396a74f30fbc286cc02d57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78817937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4e4f81bdc94adfb2b152c4986a786099e213c8872a0a447de1940eec8b36b9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41580bfa7bb549e94995896f5201eb9cea1494505ab84bd2126449b3a80d8788`  
		Last Modified: Tue, 26 Aug 2025 17:05:11 GMT  
		Size: 75.1 MB (75088762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf19c428ddd5472d5705df46e95a523161488ca0d2e70ca9bebd0089f1c233e`  
		Last Modified: Tue, 26 Aug 2025 17:05:02 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf0cd2ebebd5e2b3680f333eeeea9e24af8c1deab3442ac0419289d59b88528`  
		Last Modified: Tue, 26 Aug 2025 17:05:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a97e2c5ce5f5ae8715cfb5aa54bd600ceda8d156a4d95fe1b69ffe7160544d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd36779ff7171b497584aecf1336f80b2271cbe770dfffecab9b37499691c10d`

```dockerfile
```

-	Layers:
	-	`sha256:4e868d107d4ec0f88f2515d8c0e461129f2d4c2412b6465284b4d66c9941ba81`  
		Last Modified: Tue, 26 Aug 2025 18:20:49 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:6bc7c34f4a8c82a84964269ceb7da23eadc1bfbc06e1dd164456a4a7c5a8f064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73373120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7df50cfa2eacca4e44264105844791df8f7c91eb09af124a198445860554b81`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d347e847918994143d8709387f507640aec9549648f4ab8dd0dafaf35cda058`  
		Last Modified: Tue, 26 Aug 2025 17:17:15 GMT  
		Size: 69.7 MB (69726086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564bf67e3d60e0acd5d9612a5dc1bea2c8e30ed426161ea842a2c7203a7aa9f8`  
		Last Modified: Tue, 26 Aug 2025 17:17:08 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e8e125440740ba86e9c177b062cd9e2f77e2e8a5baecdf2b9627697318b17e`  
		Last Modified: Tue, 26 Aug 2025 17:17:08 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2040c4c901971ec2aa62d7f20a30a283a3855e4e980e1567c742de35e05f9d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb0b839668077db2d493c4e6f89335931c594587b4958d1d9f5c3171fab912c`

```dockerfile
```

-	Layers:
	-	`sha256:94a86035ec439c327f30139139dfafa0ae939c638319e9658f08da45c2eed1a3`  
		Last Modified: Tue, 26 Aug 2025 18:20:53 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7`

```console
$ docker pull varnish@sha256:86655495a7ac80e7fda84f19f1eee579435fc22204562c34db13fbaf4102f436
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

### `varnish:7.7` - linux; amd64

```console
$ docker pull varnish@sha256:782bd500bdb785fdb7985580fa0b73900fe962f2d6add4ab0946e2e1f69ab556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116340261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d16006e8ae81f8f4f1cef1f748768ea880de2571a18c956ab825f14ab43964`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd0391d5883cb827d680d347a739b3ac285458ef597837bda7523f0a973f2a0`  
		Last Modified: Fri, 29 Aug 2025 18:58:02 GMT  
		Size: 86.6 MB (86564929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f18a62a208f5f2eb2041475b3216fe4a1c7b8504500ecab7ea3cc68a7f482e8`  
		Last Modified: Fri, 29 Aug 2025 18:57:56 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b91bb588fd3ef1a72ee515f842eaef66d07efac4f7532be94eaaffab957db5a`  
		Last Modified: Fri, 29 Aug 2025 18:57:56 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:e9ebb92bd3223ea842c0dba0b5e7b617f0e40a44dc3e6f278fb8d41ec5c569c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7ca5fb0a6e2724c258065f33f5234ec33b438c0e2595ad17f194c0541fd540`

```dockerfile
```

-	Layers:
	-	`sha256:eb95f7f1490761e6d482aa0115f80ec0ad51f34293f9c6bc0f57dc6e7be44580`  
		Last Modified: Fri, 29 Aug 2025 21:19:35 GMT  
		Size: 19.7 KB (19659 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:68553fd4fac212872a82a9bca4f90aa0fc69638094c46c365f791db6db74d8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87147139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ea9b8a9b4396797a250bed48de5272f14681811ecd7e368deb2cc144949fc5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab1630934ea323c0d50cad725c7dc5f676c44f7a37a7c722547b3f8329a540a`  
		Last Modified: Fri, 29 Aug 2025 18:57:52 GMT  
		Size: 60.9 MB (60937606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c629879bc4ea3aea6aa633a3d7637e4e66fe14911635796f3561a26fd4907a`  
		Last Modified: Fri, 29 Aug 2025 18:57:44 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2ca73afdb667b1da50b2ea4d322fcd05513a1911e2180eb861163501ca2856`  
		Last Modified: Fri, 29 Aug 2025 18:57:44 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:a5603bef1c4cdb0221c96fb8fa2ab6b88e8d5c677ac5f8bea234ea23c2217b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ff7de3d1eba34853220a869769d6c88bea927eb496790491ad9b454d5bfcb5`

```dockerfile
```

-	Layers:
	-	`sha256:009e4efa2775778a8bb24ee0501047432be01274e856457fdd7411ddb3cbf444`  
		Last Modified: Fri, 29 Aug 2025 21:19:38 GMT  
		Size: 19.7 KB (19743 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:87e15ca38843e689554f2dac5f8df19676dc4360ec484c367710a0275ba2cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110518057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35c1a9ea2a4ea53bdd656f6df8a6a591d583ae479a541e5bf9347939e87cb04`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095ad00879fa642ecdc94b591fafeb1acb212eff67e42d43e95a0e34fcd79182`  
		Last Modified: Fri, 29 Aug 2025 18:57:55 GMT  
		Size: 80.4 MB (80379967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6844b8a704384fdb04db8dcf95cba67fd2c38388f9bfb8d5135199b792d20`  
		Last Modified: Fri, 29 Aug 2025 18:57:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b4f6076a264c3d34d430c878c986ee818ad85c4dc0443f3b8a67b58de1e2f4`  
		Last Modified: Fri, 29 Aug 2025 18:57:45 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:907b29abed401a16407383031774c0e121cb5d5afcc701f7242f24cfb230bbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66ddfba9ba0b7ff583cf8ee5d35099f251fd77e0a2bc364020d17c83a34fe99`

```dockerfile
```

-	Layers:
	-	`sha256:33d1899c4bb8d5f0a4d251575b523821bb8673bb60f18783991b9b31d97a9af9`  
		Last Modified: Fri, 29 Aug 2025 21:19:42 GMT  
		Size: 19.8 KB (19775 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; 386

```console
$ docker pull varnish@sha256:9880404747e278ecd087f5c6eab6bf8412c5b0ba50e991d6485083f61c34c1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114474612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaad62c8bff104e799093949a5bc72dcd1384b6e4388ae6f5c22a60d2830496c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045a468e3f64ef6078d1ad0e91b3c7c3410eba4b86e0f19e58de4a79c943fbe4`  
		Last Modified: Fri, 29 Aug 2025 18:58:09 GMT  
		Size: 83.2 MB (83183184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd71a380ffd5bdf2c24926cc53a053ce7702bcc2cd91ddc403cae22324d9013`  
		Last Modified: Fri, 29 Aug 2025 18:58:03 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7e5688565f7d12c50095b16053ccd03b6bbd73eccbc3ad67630e5af409894`  
		Last Modified: Fri, 29 Aug 2025 18:58:03 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:91b2780598d19fbfd5c2338ca231d9f798365da615c4b783a2c02eb230cf5340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ed2508357c088e800ceb6ab07a53c0d770560c6445f872add3ffaaa706e172`

```dockerfile
```

-	Layers:
	-	`sha256:9d50147cb40bae096e956219787393ef28d1de2bad15ebe6f44b95d5de4b4f42`  
		Last Modified: Fri, 29 Aug 2025 21:19:45 GMT  
		Size: 19.6 KB (19623 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; ppc64le

```console
$ docker pull varnish@sha256:fb93b07d38aa9c60ef29f22da422d0bf4db0ab2a36fb584e15da11e2fc855b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111785588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cc1ecc30191b0e4f6019dd9e57152f7ceeb6cef146cd1f71f6912df8fe2a41`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeaa7de33323e9da003d76c1a5cc0bb86f35d215429e0d9f20b652378d97952`  
		Last Modified: Fri, 29 Aug 2025 19:00:08 GMT  
		Size: 78.2 MB (78189327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e630fc6d39e8589329e37f5a61e56e9ebfc7eeca0d40411c39bcc2bfccaae5e`  
		Last Modified: Fri, 29 Aug 2025 18:59:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ad6337d770f926d12752f7f661984d17f9c36353f6a8ebb231a5ad950de3b`  
		Last Modified: Fri, 29 Aug 2025 18:59:58 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:6533ac132bd0b294ecfc3638cc8b04c2ab50ca74d45046cfffa7d442aefd5f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ad9d848ff9f848e7dee20ff109298b8e870674df25d11405b571e816436923`

```dockerfile
```

-	Layers:
	-	`sha256:2de9a81e8b94b8729ba0c57f208af387d8dc241d788317f3097bf40bd0628bec`  
		Last Modified: Fri, 29 Aug 2025 21:19:48 GMT  
		Size: 19.7 KB (19707 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; s390x

```console
$ docker pull varnish@sha256:316e16056f396da312924e65681e867878b12ffbd091bec4b8bfbdcab3d2e757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93293676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644c7b17565ef9c3c605d4da40e1fde193cbb69da7fe5eec550f1ccc75788f0a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1660409013e5bbfdf7e7587ce45ef14ffbe6f4f1ddf9e2334a36aa2db6abc0e`  
		Last Modified: Fri, 29 Aug 2025 18:59:41 GMT  
		Size: 63.5 MB (63458571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075bbb82d37082573ab3e19d8791666edde05284ddf8f73f45bde1f03eed1d9`  
		Last Modified: Fri, 29 Aug 2025 18:59:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683e60bd286912e7a79cfb7dc558aef4ee7e621471a31ad8194f8e80357adc97`  
		Last Modified: Fri, 29 Aug 2025 18:59:33 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:99ce5f6dcbc57b14b71f0a9f3990b5f6a78c7e76cb46fa68e49feab34553fdc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd53bd2f0c8cf8cb92f86f286a45d39252faa5929bae160e1e0e5bfdc3e0021`

```dockerfile
```

-	Layers:
	-	`sha256:b4508a75879abdd43a4e164b930d4eb6ab29efba0488ae7ed5c37f3bc5c2afb5`  
		Last Modified: Fri, 29 Aug 2025 21:19:52 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7-alpine`

```console
$ docker pull varnish@sha256:0297e4e6f7ad8e91e4079ca4cb6376c0c6cd0816a603f9783d6d180418a5ace3
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

### `varnish:7.7-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:968def097e04e840a52a0cb40523f6cacd02479fe1a103aa1f4faf7020a486b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (82993733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c796b0bf4f6d6821900c2b96f9582996ec10f4f95e899e8ae26e07702148ff3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8688839e5a15188a72647a6852b7152ef71c649b254a011229a90a62fbed8fa`  
		Last Modified: Tue, 26 Aug 2025 16:51:07 GMT  
		Size: 79.2 MB (79191987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd3ba927190043e8f707e6fbd55db714f6ac35cbab88b3eeddfdc1d840bbfd`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0f04afb274482621be87eefe109335897a4ebe2d1356e3796b6ec13f7f2972`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:709a0910bc16cef04b2c634e8e1a9509f6f9d413f8774bf7047aad42b295fea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9d84eee2afb88887b41c9affc9147bd2db2e6d68070444d70b697ff6cc98f8`

```dockerfile
```

-	Layers:
	-	`sha256:35a32c7db6c318b475a81a7c92e3a96e4c331f31f14454cb7028d5768e880e71`  
		Last Modified: Tue, 26 Aug 2025 18:20:08 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:36313eff0334c42ea63ea530d129fd890b761c6a5fc6f3e4b0b791db0d0a2ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64456549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5063718db8c89c5c461727031efaa74768e5b3c1f6e767ca1cf041d4c83cedf9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae3a3450a898d7d7936a3449f5213067234680cc45f3c4dd8f008c7773f78cc`  
		Last Modified: Tue, 26 Aug 2025 17:32:17 GMT  
		Size: 61.2 MB (61235455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e2bc7a31f1eb52a19ed696c0b64c8e7df06c9ced0074bcc2c6484f6ad392a7`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304012d451fc4a526211049f43cc247c6f5565043478a91325056f52f8460652`  
		Last Modified: Tue, 26 Aug 2025 16:53:16 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:99789fd7694d7a402ae33b0d7ebbcf050020c9e7ebb1860b42099fb85a215796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa12d2a02e6aad7f79d2946e4ac6338e60254980ab67d201502ed9c2c97edf87`

```dockerfile
```

-	Layers:
	-	`sha256:a7e234a9b635e5b641a9c4bfba4a4bf34f743409faa16595478e49e0704f0367`  
		Last Modified: Tue, 26 Aug 2025 18:20:12 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:6bea3798e0b800d4b6247ce3665ba08e129ff7da73ecc13df8fa9bbdffac6822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80275423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a471b03fd084177f8b271299dc3945678572500224adaa9c8118d6e66e4d26`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4b9c79e8f0d02f79a5b5986ebbeb895a5f1752ed163e203317cdc36729b386`  
		Last Modified: Tue, 26 Aug 2025 16:53:20 GMT  
		Size: 76.1 MB (76142615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cdc7619db5c8841bd4974b23b8bd4245c5077f14582530fd9db0e8a59ca0c1`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aed738cbed2c0ea53daa581f1639bd962a3d050ae5600e2e382f710df03870`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:05157ea69a9a6d3ae3be9a75ebfa4134cf0d66132050502419874cc7e76e873c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aef9306982c345cb47205fc2a23f2d9b7c11799193e2a0671a52cc948a6f1cc`

```dockerfile
```

-	Layers:
	-	`sha256:a9a1d37c8443d12093423197a6946305dc2506e30d6e330a9a45d4f331c28072`  
		Last Modified: Tue, 26 Aug 2025 18:20:16 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:ea9aa4a49f609489b627aed9356a5873cbbdb96e02c249e6ec51ce97aa8f7e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85001515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c9237f024910b41b25a64734d559f0d5c513ba4caaba586658fbc4fdb23d7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2ed555a42edaaa80f0729b321774d3bff810ae570d3b3be84f458544f1650a`  
		Last Modified: Tue, 26 Aug 2025 16:51:40 GMT  
		Size: 81.4 MB (81384451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc952cfe554ff9395699f7f3435db2ede214f1f2ddb49051b3fcc2d7d9574e3c`  
		Last Modified: Tue, 26 Aug 2025 16:51:30 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42d19e5629e404b539dea7a92dd4e1c28fb152ac4fd387f335112d967fa42bf`  
		Last Modified: Tue, 26 Aug 2025 16:51:24 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1ca2dfd325862cf53869f98b54b6f269ff3825c7252e5b75a53ee4d34e31056d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580baac8e15bdc972db7c72085205331fa315a8f8220664084639bbaa46e484f`

```dockerfile
```

-	Layers:
	-	`sha256:4420a9c08aeaace20f6102f79d7704bd2d2d759ad92e107297a5e3b71f8c6b35`  
		Last Modified: Tue, 26 Aug 2025 18:20:20 GMT  
		Size: 19.4 KB (19431 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:82af53ff59713b0b3586af4f2977b2d5ab7df673be720e9037f0df2f5c726749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78963604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e699f34e611ec9aeac4b9938dcf600cb3d115e33cdc619e45b1006461b9ef15f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7d2a57f1ef9f97b49b6fff28a7126d97e7198d9c67b1f4d38730c945b55a7`  
		Last Modified: Tue, 26 Aug 2025 17:44:40 GMT  
		Size: 75.2 MB (75234430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bbc6a66435fbe346aedb5478520c0031df4d574bfe13b98d36123bd0cb1522`  
		Last Modified: Tue, 26 Aug 2025 16:57:41 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455ca0fa6d5a336db59bff2f1f594bb7899650b7763648479f824021cffa2a7`  
		Last Modified: Tue, 26 Aug 2025 16:57:44 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:582db1db9c028422995048d09a52f5f13e30d4a775813f9e7722c3c2105907f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3351982c781fc09f6de5ff55d9239383b65c53221e66d9276d7d3b08204962`

```dockerfile
```

-	Layers:
	-	`sha256:962692efb06cc7405e9986b44b7931d8c5120419ab4aace742096f778b04db3c`  
		Last Modified: Tue, 26 Aug 2025 18:20:23 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:7112d826a48691fd016859332f9fee9f351e69dbc356b59861aecf05372c7621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73520274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f1caf4dd71bd936b7e54525ae5ae07a1da8ae4899f5e60d3b22e024f31aff0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495f345eb737fe5e7f7d583c0f6630cf80a4d67b95ae9bd76902dde2dba9d51b`  
		Last Modified: Tue, 26 Aug 2025 17:04:01 GMT  
		Size: 69.9 MB (69873239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c307bbaffedd8c00cddb99e59f7d3697e3e731371404ac5e8955508c13d7a93`  
		Last Modified: Tue, 26 Aug 2025 17:03:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415def403d1cc7b5626e73089336be57199faba9279eb128d414f71dae0fad10`  
		Last Modified: Tue, 26 Aug 2025 17:03:52 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6b5f52d363112af7587ab99319549299d91a096b9a38dace51b58f53be34cbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74086b67192616f0b1ee67becd30f028625db9af6ee7fe3897946a283917d80`

```dockerfile
```

-	Layers:
	-	`sha256:921ec808b8a72d9cbe23454e94ef9fb544514404bf06c731e043eed5f4e2025b`  
		Last Modified: Tue, 26 Aug 2025 18:20:27 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.3`

```console
$ docker pull varnish@sha256:86655495a7ac80e7fda84f19f1eee579435fc22204562c34db13fbaf4102f436
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

### `varnish:7.7.3` - linux; amd64

```console
$ docker pull varnish@sha256:782bd500bdb785fdb7985580fa0b73900fe962f2d6add4ab0946e2e1f69ab556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116340261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d16006e8ae81f8f4f1cef1f748768ea880de2571a18c956ab825f14ab43964`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd0391d5883cb827d680d347a739b3ac285458ef597837bda7523f0a973f2a0`  
		Last Modified: Fri, 29 Aug 2025 18:58:02 GMT  
		Size: 86.6 MB (86564929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f18a62a208f5f2eb2041475b3216fe4a1c7b8504500ecab7ea3cc68a7f482e8`  
		Last Modified: Fri, 29 Aug 2025 18:57:56 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b91bb588fd3ef1a72ee515f842eaef66d07efac4f7532be94eaaffab957db5a`  
		Last Modified: Fri, 29 Aug 2025 18:57:56 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:e9ebb92bd3223ea842c0dba0b5e7b617f0e40a44dc3e6f278fb8d41ec5c569c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7ca5fb0a6e2724c258065f33f5234ec33b438c0e2595ad17f194c0541fd540`

```dockerfile
```

-	Layers:
	-	`sha256:eb95f7f1490761e6d482aa0115f80ec0ad51f34293f9c6bc0f57dc6e7be44580`  
		Last Modified: Fri, 29 Aug 2025 21:19:35 GMT  
		Size: 19.7 KB (19659 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; arm variant v7

```console
$ docker pull varnish@sha256:68553fd4fac212872a82a9bca4f90aa0fc69638094c46c365f791db6db74d8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87147139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ea9b8a9b4396797a250bed48de5272f14681811ecd7e368deb2cc144949fc5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab1630934ea323c0d50cad725c7dc5f676c44f7a37a7c722547b3f8329a540a`  
		Last Modified: Fri, 29 Aug 2025 18:57:52 GMT  
		Size: 60.9 MB (60937606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c629879bc4ea3aea6aa633a3d7637e4e66fe14911635796f3561a26fd4907a`  
		Last Modified: Fri, 29 Aug 2025 18:57:44 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2ca73afdb667b1da50b2ea4d322fcd05513a1911e2180eb861163501ca2856`  
		Last Modified: Fri, 29 Aug 2025 18:57:44 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:a5603bef1c4cdb0221c96fb8fa2ab6b88e8d5c677ac5f8bea234ea23c2217b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ff7de3d1eba34853220a869769d6c88bea927eb496790491ad9b454d5bfcb5`

```dockerfile
```

-	Layers:
	-	`sha256:009e4efa2775778a8bb24ee0501047432be01274e856457fdd7411ddb3cbf444`  
		Last Modified: Fri, 29 Aug 2025 21:19:38 GMT  
		Size: 19.7 KB (19743 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:87e15ca38843e689554f2dac5f8df19676dc4360ec484c367710a0275ba2cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110518057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35c1a9ea2a4ea53bdd656f6df8a6a591d583ae479a541e5bf9347939e87cb04`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095ad00879fa642ecdc94b591fafeb1acb212eff67e42d43e95a0e34fcd79182`  
		Last Modified: Fri, 29 Aug 2025 18:57:55 GMT  
		Size: 80.4 MB (80379967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6844b8a704384fdb04db8dcf95cba67fd2c38388f9bfb8d5135199b792d20`  
		Last Modified: Fri, 29 Aug 2025 18:57:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b4f6076a264c3d34d430c878c986ee818ad85c4dc0443f3b8a67b58de1e2f4`  
		Last Modified: Fri, 29 Aug 2025 18:57:45 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:907b29abed401a16407383031774c0e121cb5d5afcc701f7242f24cfb230bbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66ddfba9ba0b7ff583cf8ee5d35099f251fd77e0a2bc364020d17c83a34fe99`

```dockerfile
```

-	Layers:
	-	`sha256:33d1899c4bb8d5f0a4d251575b523821bb8673bb60f18783991b9b31d97a9af9`  
		Last Modified: Fri, 29 Aug 2025 21:19:42 GMT  
		Size: 19.8 KB (19775 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; 386

```console
$ docker pull varnish@sha256:9880404747e278ecd087f5c6eab6bf8412c5b0ba50e991d6485083f61c34c1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114474612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaad62c8bff104e799093949a5bc72dcd1384b6e4388ae6f5c22a60d2830496c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045a468e3f64ef6078d1ad0e91b3c7c3410eba4b86e0f19e58de4a79c943fbe4`  
		Last Modified: Fri, 29 Aug 2025 18:58:09 GMT  
		Size: 83.2 MB (83183184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd71a380ffd5bdf2c24926cc53a053ce7702bcc2cd91ddc403cae22324d9013`  
		Last Modified: Fri, 29 Aug 2025 18:58:03 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7e5688565f7d12c50095b16053ccd03b6bbd73eccbc3ad67630e5af409894`  
		Last Modified: Fri, 29 Aug 2025 18:58:03 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:91b2780598d19fbfd5c2338ca231d9f798365da615c4b783a2c02eb230cf5340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ed2508357c088e800ceb6ab07a53c0d770560c6445f872add3ffaaa706e172`

```dockerfile
```

-	Layers:
	-	`sha256:9d50147cb40bae096e956219787393ef28d1de2bad15ebe6f44b95d5de4b4f42`  
		Last Modified: Fri, 29 Aug 2025 21:19:45 GMT  
		Size: 19.6 KB (19623 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; ppc64le

```console
$ docker pull varnish@sha256:fb93b07d38aa9c60ef29f22da422d0bf4db0ab2a36fb584e15da11e2fc855b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111785588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cc1ecc30191b0e4f6019dd9e57152f7ceeb6cef146cd1f71f6912df8fe2a41`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeaa7de33323e9da003d76c1a5cc0bb86f35d215429e0d9f20b652378d97952`  
		Last Modified: Fri, 29 Aug 2025 19:00:08 GMT  
		Size: 78.2 MB (78189327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e630fc6d39e8589329e37f5a61e56e9ebfc7eeca0d40411c39bcc2bfccaae5e`  
		Last Modified: Fri, 29 Aug 2025 18:59:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ad6337d770f926d12752f7f661984d17f9c36353f6a8ebb231a5ad950de3b`  
		Last Modified: Fri, 29 Aug 2025 18:59:58 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:6533ac132bd0b294ecfc3638cc8b04c2ab50ca74d45046cfffa7d442aefd5f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ad9d848ff9f848e7dee20ff109298b8e870674df25d11405b571e816436923`

```dockerfile
```

-	Layers:
	-	`sha256:2de9a81e8b94b8729ba0c57f208af387d8dc241d788317f3097bf40bd0628bec`  
		Last Modified: Fri, 29 Aug 2025 21:19:48 GMT  
		Size: 19.7 KB (19707 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; s390x

```console
$ docker pull varnish@sha256:316e16056f396da312924e65681e867878b12ffbd091bec4b8bfbdcab3d2e757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93293676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644c7b17565ef9c3c605d4da40e1fde193cbb69da7fe5eec550f1ccc75788f0a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1660409013e5bbfdf7e7587ce45ef14ffbe6f4f1ddf9e2334a36aa2db6abc0e`  
		Last Modified: Fri, 29 Aug 2025 18:59:41 GMT  
		Size: 63.5 MB (63458571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075bbb82d37082573ab3e19d8791666edde05284ddf8f73f45bde1f03eed1d9`  
		Last Modified: Fri, 29 Aug 2025 18:59:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683e60bd286912e7a79cfb7dc558aef4ee7e621471a31ad8194f8e80357adc97`  
		Last Modified: Fri, 29 Aug 2025 18:59:33 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:99ce5f6dcbc57b14b71f0a9f3990b5f6a78c7e76cb46fa68e49feab34553fdc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd53bd2f0c8cf8cb92f86f286a45d39252faa5929bae160e1e0e5bfdc3e0021`

```dockerfile
```

-	Layers:
	-	`sha256:b4508a75879abdd43a4e164b930d4eb6ab29efba0488ae7ed5c37f3bc5c2afb5`  
		Last Modified: Fri, 29 Aug 2025 21:19:52 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7.7.3-alpine`

```console
$ docker pull varnish@sha256:0297e4e6f7ad8e91e4079ca4cb6376c0c6cd0816a603f9783d6d180418a5ace3
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

### `varnish:7.7.3-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:968def097e04e840a52a0cb40523f6cacd02479fe1a103aa1f4faf7020a486b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (82993733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c796b0bf4f6d6821900c2b96f9582996ec10f4f95e899e8ae26e07702148ff3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8688839e5a15188a72647a6852b7152ef71c649b254a011229a90a62fbed8fa`  
		Last Modified: Tue, 26 Aug 2025 16:51:07 GMT  
		Size: 79.2 MB (79191987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd3ba927190043e8f707e6fbd55db714f6ac35cbab88b3eeddfdc1d840bbfd`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0f04afb274482621be87eefe109335897a4ebe2d1356e3796b6ec13f7f2972`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:709a0910bc16cef04b2c634e8e1a9509f6f9d413f8774bf7047aad42b295fea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9d84eee2afb88887b41c9affc9147bd2db2e6d68070444d70b697ff6cc98f8`

```dockerfile
```

-	Layers:
	-	`sha256:35a32c7db6c318b475a81a7c92e3a96e4c331f31f14454cb7028d5768e880e71`  
		Last Modified: Tue, 26 Aug 2025 18:20:08 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:36313eff0334c42ea63ea530d129fd890b761c6a5fc6f3e4b0b791db0d0a2ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64456549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5063718db8c89c5c461727031efaa74768e5b3c1f6e767ca1cf041d4c83cedf9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae3a3450a898d7d7936a3449f5213067234680cc45f3c4dd8f008c7773f78cc`  
		Last Modified: Tue, 26 Aug 2025 17:32:17 GMT  
		Size: 61.2 MB (61235455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e2bc7a31f1eb52a19ed696c0b64c8e7df06c9ced0074bcc2c6484f6ad392a7`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304012d451fc4a526211049f43cc247c6f5565043478a91325056f52f8460652`  
		Last Modified: Tue, 26 Aug 2025 16:53:16 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:99789fd7694d7a402ae33b0d7ebbcf050020c9e7ebb1860b42099fb85a215796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa12d2a02e6aad7f79d2946e4ac6338e60254980ab67d201502ed9c2c97edf87`

```dockerfile
```

-	Layers:
	-	`sha256:a7e234a9b635e5b641a9c4bfba4a4bf34f743409faa16595478e49e0704f0367`  
		Last Modified: Tue, 26 Aug 2025 18:20:12 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:6bea3798e0b800d4b6247ce3665ba08e129ff7da73ecc13df8fa9bbdffac6822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80275423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a471b03fd084177f8b271299dc3945678572500224adaa9c8118d6e66e4d26`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4b9c79e8f0d02f79a5b5986ebbeb895a5f1752ed163e203317cdc36729b386`  
		Last Modified: Tue, 26 Aug 2025 16:53:20 GMT  
		Size: 76.1 MB (76142615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cdc7619db5c8841bd4974b23b8bd4245c5077f14582530fd9db0e8a59ca0c1`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aed738cbed2c0ea53daa581f1639bd962a3d050ae5600e2e382f710df03870`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:05157ea69a9a6d3ae3be9a75ebfa4134cf0d66132050502419874cc7e76e873c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aef9306982c345cb47205fc2a23f2d9b7c11799193e2a0671a52cc948a6f1cc`

```dockerfile
```

-	Layers:
	-	`sha256:a9a1d37c8443d12093423197a6946305dc2506e30d6e330a9a45d4f331c28072`  
		Last Modified: Tue, 26 Aug 2025 18:20:16 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3-alpine` - linux; 386

```console
$ docker pull varnish@sha256:ea9aa4a49f609489b627aed9356a5873cbbdb96e02c249e6ec51ce97aa8f7e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85001515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c9237f024910b41b25a64734d559f0d5c513ba4caaba586658fbc4fdb23d7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2ed555a42edaaa80f0729b321774d3bff810ae570d3b3be84f458544f1650a`  
		Last Modified: Tue, 26 Aug 2025 16:51:40 GMT  
		Size: 81.4 MB (81384451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc952cfe554ff9395699f7f3435db2ede214f1f2ddb49051b3fcc2d7d9574e3c`  
		Last Modified: Tue, 26 Aug 2025 16:51:30 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42d19e5629e404b539dea7a92dd4e1c28fb152ac4fd387f335112d967fa42bf`  
		Last Modified: Tue, 26 Aug 2025 16:51:24 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1ca2dfd325862cf53869f98b54b6f269ff3825c7252e5b75a53ee4d34e31056d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580baac8e15bdc972db7c72085205331fa315a8f8220664084639bbaa46e484f`

```dockerfile
```

-	Layers:
	-	`sha256:4420a9c08aeaace20f6102f79d7704bd2d2d759ad92e107297a5e3b71f8c6b35`  
		Last Modified: Tue, 26 Aug 2025 18:20:20 GMT  
		Size: 19.4 KB (19431 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:82af53ff59713b0b3586af4f2977b2d5ab7df673be720e9037f0df2f5c726749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78963604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e699f34e611ec9aeac4b9938dcf600cb3d115e33cdc619e45b1006461b9ef15f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7d2a57f1ef9f97b49b6fff28a7126d97e7198d9c67b1f4d38730c945b55a7`  
		Last Modified: Tue, 26 Aug 2025 17:44:40 GMT  
		Size: 75.2 MB (75234430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bbc6a66435fbe346aedb5478520c0031df4d574bfe13b98d36123bd0cb1522`  
		Last Modified: Tue, 26 Aug 2025 16:57:41 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455ca0fa6d5a336db59bff2f1f594bb7899650b7763648479f824021cffa2a7`  
		Last Modified: Tue, 26 Aug 2025 16:57:44 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:582db1db9c028422995048d09a52f5f13e30d4a775813f9e7722c3c2105907f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3351982c781fc09f6de5ff55d9239383b65c53221e66d9276d7d3b08204962`

```dockerfile
```

-	Layers:
	-	`sha256:962692efb06cc7405e9986b44b7931d8c5120419ab4aace742096f778b04db3c`  
		Last Modified: Tue, 26 Aug 2025 18:20:23 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:7112d826a48691fd016859332f9fee9f351e69dbc356b59861aecf05372c7621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73520274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f1caf4dd71bd936b7e54525ae5ae07a1da8ae4899f5e60d3b22e024f31aff0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495f345eb737fe5e7f7d583c0f6630cf80a4d67b95ae9bd76902dde2dba9d51b`  
		Last Modified: Tue, 26 Aug 2025 17:04:01 GMT  
		Size: 69.9 MB (69873239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c307bbaffedd8c00cddb99e59f7d3697e3e731371404ac5e8955508c13d7a93`  
		Last Modified: Tue, 26 Aug 2025 17:03:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415def403d1cc7b5626e73089336be57199faba9279eb128d414f71dae0fad10`  
		Last Modified: Tue, 26 Aug 2025 17:03:52 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6b5f52d363112af7587ab99319549299d91a096b9a38dace51b58f53be34cbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74086b67192616f0b1ee67becd30f028625db9af6ee7fe3897946a283917d80`

```dockerfile
```

-	Layers:
	-	`sha256:921ec808b8a72d9cbe23454e94ef9fb544514404bf06c731e043eed5f4e2025b`  
		Last Modified: Tue, 26 Aug 2025 18:20:27 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:alpine`

```console
$ docker pull varnish@sha256:0297e4e6f7ad8e91e4079ca4cb6376c0c6cd0816a603f9783d6d180418a5ace3
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
$ docker pull varnish@sha256:968def097e04e840a52a0cb40523f6cacd02479fe1a103aa1f4faf7020a486b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (82993733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c796b0bf4f6d6821900c2b96f9582996ec10f4f95e899e8ae26e07702148ff3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8688839e5a15188a72647a6852b7152ef71c649b254a011229a90a62fbed8fa`  
		Last Modified: Tue, 26 Aug 2025 16:51:07 GMT  
		Size: 79.2 MB (79191987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd3ba927190043e8f707e6fbd55db714f6ac35cbab88b3eeddfdc1d840bbfd`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0f04afb274482621be87eefe109335897a4ebe2d1356e3796b6ec13f7f2972`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:709a0910bc16cef04b2c634e8e1a9509f6f9d413f8774bf7047aad42b295fea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9d84eee2afb88887b41c9affc9147bd2db2e6d68070444d70b697ff6cc98f8`

```dockerfile
```

-	Layers:
	-	`sha256:35a32c7db6c318b475a81a7c92e3a96e4c331f31f14454cb7028d5768e880e71`  
		Last Modified: Tue, 26 Aug 2025 18:20:08 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:36313eff0334c42ea63ea530d129fd890b761c6a5fc6f3e4b0b791db0d0a2ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64456549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5063718db8c89c5c461727031efaa74768e5b3c1f6e767ca1cf041d4c83cedf9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae3a3450a898d7d7936a3449f5213067234680cc45f3c4dd8f008c7773f78cc`  
		Last Modified: Tue, 26 Aug 2025 17:32:17 GMT  
		Size: 61.2 MB (61235455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e2bc7a31f1eb52a19ed696c0b64c8e7df06c9ced0074bcc2c6484f6ad392a7`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304012d451fc4a526211049f43cc247c6f5565043478a91325056f52f8460652`  
		Last Modified: Tue, 26 Aug 2025 16:53:16 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:99789fd7694d7a402ae33b0d7ebbcf050020c9e7ebb1860b42099fb85a215796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa12d2a02e6aad7f79d2946e4ac6338e60254980ab67d201502ed9c2c97edf87`

```dockerfile
```

-	Layers:
	-	`sha256:a7e234a9b635e5b641a9c4bfba4a4bf34f743409faa16595478e49e0704f0367`  
		Last Modified: Tue, 26 Aug 2025 18:20:12 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:6bea3798e0b800d4b6247ce3665ba08e129ff7da73ecc13df8fa9bbdffac6822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80275423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a471b03fd084177f8b271299dc3945678572500224adaa9c8118d6e66e4d26`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4b9c79e8f0d02f79a5b5986ebbeb895a5f1752ed163e203317cdc36729b386`  
		Last Modified: Tue, 26 Aug 2025 16:53:20 GMT  
		Size: 76.1 MB (76142615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cdc7619db5c8841bd4974b23b8bd4245c5077f14582530fd9db0e8a59ca0c1`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aed738cbed2c0ea53daa581f1639bd962a3d050ae5600e2e382f710df03870`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:05157ea69a9a6d3ae3be9a75ebfa4134cf0d66132050502419874cc7e76e873c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aef9306982c345cb47205fc2a23f2d9b7c11799193e2a0671a52cc948a6f1cc`

```dockerfile
```

-	Layers:
	-	`sha256:a9a1d37c8443d12093423197a6946305dc2506e30d6e330a9a45d4f331c28072`  
		Last Modified: Tue, 26 Aug 2025 18:20:16 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:ea9aa4a49f609489b627aed9356a5873cbbdb96e02c249e6ec51ce97aa8f7e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85001515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c9237f024910b41b25a64734d559f0d5c513ba4caaba586658fbc4fdb23d7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2ed555a42edaaa80f0729b321774d3bff810ae570d3b3be84f458544f1650a`  
		Last Modified: Tue, 26 Aug 2025 16:51:40 GMT  
		Size: 81.4 MB (81384451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc952cfe554ff9395699f7f3435db2ede214f1f2ddb49051b3fcc2d7d9574e3c`  
		Last Modified: Tue, 26 Aug 2025 16:51:30 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42d19e5629e404b539dea7a92dd4e1c28fb152ac4fd387f335112d967fa42bf`  
		Last Modified: Tue, 26 Aug 2025 16:51:24 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1ca2dfd325862cf53869f98b54b6f269ff3825c7252e5b75a53ee4d34e31056d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580baac8e15bdc972db7c72085205331fa315a8f8220664084639bbaa46e484f`

```dockerfile
```

-	Layers:
	-	`sha256:4420a9c08aeaace20f6102f79d7704bd2d2d759ad92e107297a5e3b71f8c6b35`  
		Last Modified: Tue, 26 Aug 2025 18:20:20 GMT  
		Size: 19.4 KB (19431 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:82af53ff59713b0b3586af4f2977b2d5ab7df673be720e9037f0df2f5c726749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78963604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e699f34e611ec9aeac4b9938dcf600cb3d115e33cdc619e45b1006461b9ef15f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7d2a57f1ef9f97b49b6fff28a7126d97e7198d9c67b1f4d38730c945b55a7`  
		Last Modified: Tue, 26 Aug 2025 17:44:40 GMT  
		Size: 75.2 MB (75234430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bbc6a66435fbe346aedb5478520c0031df4d574bfe13b98d36123bd0cb1522`  
		Last Modified: Tue, 26 Aug 2025 16:57:41 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455ca0fa6d5a336db59bff2f1f594bb7899650b7763648479f824021cffa2a7`  
		Last Modified: Tue, 26 Aug 2025 16:57:44 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:582db1db9c028422995048d09a52f5f13e30d4a775813f9e7722c3c2105907f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3351982c781fc09f6de5ff55d9239383b65c53221e66d9276d7d3b08204962`

```dockerfile
```

-	Layers:
	-	`sha256:962692efb06cc7405e9986b44b7931d8c5120419ab4aace742096f778b04db3c`  
		Last Modified: Tue, 26 Aug 2025 18:20:23 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:7112d826a48691fd016859332f9fee9f351e69dbc356b59861aecf05372c7621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73520274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f1caf4dd71bd936b7e54525ae5ae07a1da8ae4899f5e60d3b22e024f31aff0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495f345eb737fe5e7f7d583c0f6630cf80a4d67b95ae9bd76902dde2dba9d51b`  
		Last Modified: Tue, 26 Aug 2025 17:04:01 GMT  
		Size: 69.9 MB (69873239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c307bbaffedd8c00cddb99e59f7d3697e3e731371404ac5e8955508c13d7a93`  
		Last Modified: Tue, 26 Aug 2025 17:03:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415def403d1cc7b5626e73089336be57199faba9279eb128d414f71dae0fad10`  
		Last Modified: Tue, 26 Aug 2025 17:03:52 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6b5f52d363112af7587ab99319549299d91a096b9a38dace51b58f53be34cbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74086b67192616f0b1ee67becd30f028625db9af6ee7fe3897946a283917d80`

```dockerfile
```

-	Layers:
	-	`sha256:921ec808b8a72d9cbe23454e94ef9fb544514404bf06c731e043eed5f4e2025b`  
		Last Modified: Tue, 26 Aug 2025 18:20:27 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:86655495a7ac80e7fda84f19f1eee579435fc22204562c34db13fbaf4102f436
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
$ docker pull varnish@sha256:782bd500bdb785fdb7985580fa0b73900fe962f2d6add4ab0946e2e1f69ab556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116340261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d16006e8ae81f8f4f1cef1f748768ea880de2571a18c956ab825f14ab43964`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd0391d5883cb827d680d347a739b3ac285458ef597837bda7523f0a973f2a0`  
		Last Modified: Fri, 29 Aug 2025 18:58:02 GMT  
		Size: 86.6 MB (86564929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f18a62a208f5f2eb2041475b3216fe4a1c7b8504500ecab7ea3cc68a7f482e8`  
		Last Modified: Fri, 29 Aug 2025 18:57:56 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b91bb588fd3ef1a72ee515f842eaef66d07efac4f7532be94eaaffab957db5a`  
		Last Modified: Fri, 29 Aug 2025 18:57:56 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:e9ebb92bd3223ea842c0dba0b5e7b617f0e40a44dc3e6f278fb8d41ec5c569c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7ca5fb0a6e2724c258065f33f5234ec33b438c0e2595ad17f194c0541fd540`

```dockerfile
```

-	Layers:
	-	`sha256:eb95f7f1490761e6d482aa0115f80ec0ad51f34293f9c6bc0f57dc6e7be44580`  
		Last Modified: Fri, 29 Aug 2025 21:19:35 GMT  
		Size: 19.7 KB (19659 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:68553fd4fac212872a82a9bca4f90aa0fc69638094c46c365f791db6db74d8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87147139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ea9b8a9b4396797a250bed48de5272f14681811ecd7e368deb2cc144949fc5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab1630934ea323c0d50cad725c7dc5f676c44f7a37a7c722547b3f8329a540a`  
		Last Modified: Fri, 29 Aug 2025 18:57:52 GMT  
		Size: 60.9 MB (60937606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c629879bc4ea3aea6aa633a3d7637e4e66fe14911635796f3561a26fd4907a`  
		Last Modified: Fri, 29 Aug 2025 18:57:44 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2ca73afdb667b1da50b2ea4d322fcd05513a1911e2180eb861163501ca2856`  
		Last Modified: Fri, 29 Aug 2025 18:57:44 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:a5603bef1c4cdb0221c96fb8fa2ab6b88e8d5c677ac5f8bea234ea23c2217b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ff7de3d1eba34853220a869769d6c88bea927eb496790491ad9b454d5bfcb5`

```dockerfile
```

-	Layers:
	-	`sha256:009e4efa2775778a8bb24ee0501047432be01274e856457fdd7411ddb3cbf444`  
		Last Modified: Fri, 29 Aug 2025 21:19:38 GMT  
		Size: 19.7 KB (19743 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:87e15ca38843e689554f2dac5f8df19676dc4360ec484c367710a0275ba2cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110518057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35c1a9ea2a4ea53bdd656f6df8a6a591d583ae479a541e5bf9347939e87cb04`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095ad00879fa642ecdc94b591fafeb1acb212eff67e42d43e95a0e34fcd79182`  
		Last Modified: Fri, 29 Aug 2025 18:57:55 GMT  
		Size: 80.4 MB (80379967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6844b8a704384fdb04db8dcf95cba67fd2c38388f9bfb8d5135199b792d20`  
		Last Modified: Fri, 29 Aug 2025 18:57:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b4f6076a264c3d34d430c878c986ee818ad85c4dc0443f3b8a67b58de1e2f4`  
		Last Modified: Fri, 29 Aug 2025 18:57:45 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:907b29abed401a16407383031774c0e121cb5d5afcc701f7242f24cfb230bbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66ddfba9ba0b7ff583cf8ee5d35099f251fd77e0a2bc364020d17c83a34fe99`

```dockerfile
```

-	Layers:
	-	`sha256:33d1899c4bb8d5f0a4d251575b523821bb8673bb60f18783991b9b31d97a9af9`  
		Last Modified: Fri, 29 Aug 2025 21:19:42 GMT  
		Size: 19.8 KB (19775 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:9880404747e278ecd087f5c6eab6bf8412c5b0ba50e991d6485083f61c34c1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114474612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaad62c8bff104e799093949a5bc72dcd1384b6e4388ae6f5c22a60d2830496c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045a468e3f64ef6078d1ad0e91b3c7c3410eba4b86e0f19e58de4a79c943fbe4`  
		Last Modified: Fri, 29 Aug 2025 18:58:09 GMT  
		Size: 83.2 MB (83183184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd71a380ffd5bdf2c24926cc53a053ce7702bcc2cd91ddc403cae22324d9013`  
		Last Modified: Fri, 29 Aug 2025 18:58:03 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7e5688565f7d12c50095b16053ccd03b6bbd73eccbc3ad67630e5af409894`  
		Last Modified: Fri, 29 Aug 2025 18:58:03 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:91b2780598d19fbfd5c2338ca231d9f798365da615c4b783a2c02eb230cf5340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ed2508357c088e800ceb6ab07a53c0d770560c6445f872add3ffaaa706e172`

```dockerfile
```

-	Layers:
	-	`sha256:9d50147cb40bae096e956219787393ef28d1de2bad15ebe6f44b95d5de4b4f42`  
		Last Modified: Fri, 29 Aug 2025 21:19:45 GMT  
		Size: 19.6 KB (19623 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:fb93b07d38aa9c60ef29f22da422d0bf4db0ab2a36fb584e15da11e2fc855b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111785588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cc1ecc30191b0e4f6019dd9e57152f7ceeb6cef146cd1f71f6912df8fe2a41`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeaa7de33323e9da003d76c1a5cc0bb86f35d215429e0d9f20b652378d97952`  
		Last Modified: Fri, 29 Aug 2025 19:00:08 GMT  
		Size: 78.2 MB (78189327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e630fc6d39e8589329e37f5a61e56e9ebfc7eeca0d40411c39bcc2bfccaae5e`  
		Last Modified: Fri, 29 Aug 2025 18:59:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ad6337d770f926d12752f7f661984d17f9c36353f6a8ebb231a5ad950de3b`  
		Last Modified: Fri, 29 Aug 2025 18:59:58 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:6533ac132bd0b294ecfc3638cc8b04c2ab50ca74d45046cfffa7d442aefd5f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ad9d848ff9f848e7dee20ff109298b8e870674df25d11405b571e816436923`

```dockerfile
```

-	Layers:
	-	`sha256:2de9a81e8b94b8729ba0c57f208af387d8dc241d788317f3097bf40bd0628bec`  
		Last Modified: Fri, 29 Aug 2025 21:19:48 GMT  
		Size: 19.7 KB (19707 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:316e16056f396da312924e65681e867878b12ffbd091bec4b8bfbdcab3d2e757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93293676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644c7b17565ef9c3c605d4da40e1fde193cbb69da7fe5eec550f1ccc75788f0a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1660409013e5bbfdf7e7587ce45ef14ffbe6f4f1ddf9e2334a36aa2db6abc0e`  
		Last Modified: Fri, 29 Aug 2025 18:59:41 GMT  
		Size: 63.5 MB (63458571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075bbb82d37082573ab3e19d8791666edde05284ddf8f73f45bde1f03eed1d9`  
		Last Modified: Fri, 29 Aug 2025 18:59:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683e60bd286912e7a79cfb7dc558aef4ee7e621471a31ad8194f8e80357adc97`  
		Last Modified: Fri, 29 Aug 2025 18:59:33 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:99ce5f6dcbc57b14b71f0a9f3990b5f6a78c7e76cb46fa68e49feab34553fdc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd53bd2f0c8cf8cb92f86f286a45d39252faa5929bae160e1e0e5bfdc3e0021`

```dockerfile
```

-	Layers:
	-	`sha256:b4508a75879abdd43a4e164b930d4eb6ab29efba0488ae7ed5c37f3bc5c2afb5`  
		Last Modified: Fri, 29 Aug 2025 21:19:52 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:0297e4e6f7ad8e91e4079ca4cb6376c0c6cd0816a603f9783d6d180418a5ace3
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
$ docker pull varnish@sha256:968def097e04e840a52a0cb40523f6cacd02479fe1a103aa1f4faf7020a486b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (82993733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c796b0bf4f6d6821900c2b96f9582996ec10f4f95e899e8ae26e07702148ff3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8688839e5a15188a72647a6852b7152ef71c649b254a011229a90a62fbed8fa`  
		Last Modified: Tue, 26 Aug 2025 16:51:07 GMT  
		Size: 79.2 MB (79191987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfd3ba927190043e8f707e6fbd55db714f6ac35cbab88b3eeddfdc1d840bbfd`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0f04afb274482621be87eefe109335897a4ebe2d1356e3796b6ec13f7f2972`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:709a0910bc16cef04b2c634e8e1a9509f6f9d413f8774bf7047aad42b295fea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9d84eee2afb88887b41c9affc9147bd2db2e6d68070444d70b697ff6cc98f8`

```dockerfile
```

-	Layers:
	-	`sha256:35a32c7db6c318b475a81a7c92e3a96e4c331f31f14454cb7028d5768e880e71`  
		Last Modified: Tue, 26 Aug 2025 18:20:08 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:36313eff0334c42ea63ea530d129fd890b761c6a5fc6f3e4b0b791db0d0a2ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64456549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5063718db8c89c5c461727031efaa74768e5b3c1f6e767ca1cf041d4c83cedf9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae3a3450a898d7d7936a3449f5213067234680cc45f3c4dd8f008c7773f78cc`  
		Last Modified: Tue, 26 Aug 2025 17:32:17 GMT  
		Size: 61.2 MB (61235455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e2bc7a31f1eb52a19ed696c0b64c8e7df06c9ced0074bcc2c6484f6ad392a7`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304012d451fc4a526211049f43cc247c6f5565043478a91325056f52f8460652`  
		Last Modified: Tue, 26 Aug 2025 16:53:16 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:99789fd7694d7a402ae33b0d7ebbcf050020c9e7ebb1860b42099fb85a215796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa12d2a02e6aad7f79d2946e4ac6338e60254980ab67d201502ed9c2c97edf87`

```dockerfile
```

-	Layers:
	-	`sha256:a7e234a9b635e5b641a9c4bfba4a4bf34f743409faa16595478e49e0704f0367`  
		Last Modified: Tue, 26 Aug 2025 18:20:12 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:6bea3798e0b800d4b6247ce3665ba08e129ff7da73ecc13df8fa9bbdffac6822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80275423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a471b03fd084177f8b271299dc3945678572500224adaa9c8118d6e66e4d26`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4b9c79e8f0d02f79a5b5986ebbeb895a5f1752ed163e203317cdc36729b386`  
		Last Modified: Tue, 26 Aug 2025 16:53:20 GMT  
		Size: 76.1 MB (76142615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cdc7619db5c8841bd4974b23b8bd4245c5077f14582530fd9db0e8a59ca0c1`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aed738cbed2c0ea53daa581f1639bd962a3d050ae5600e2e382f710df03870`  
		Last Modified: Tue, 26 Aug 2025 16:53:12 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:05157ea69a9a6d3ae3be9a75ebfa4134cf0d66132050502419874cc7e76e873c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aef9306982c345cb47205fc2a23f2d9b7c11799193e2a0671a52cc948a6f1cc`

```dockerfile
```

-	Layers:
	-	`sha256:a9a1d37c8443d12093423197a6946305dc2506e30d6e330a9a45d4f331c28072`  
		Last Modified: Tue, 26 Aug 2025 18:20:16 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:ea9aa4a49f609489b627aed9356a5873cbbdb96e02c249e6ec51ce97aa8f7e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85001515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c9237f024910b41b25a64734d559f0d5c513ba4caaba586658fbc4fdb23d7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2ed555a42edaaa80f0729b321774d3bff810ae570d3b3be84f458544f1650a`  
		Last Modified: Tue, 26 Aug 2025 16:51:40 GMT  
		Size: 81.4 MB (81384451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc952cfe554ff9395699f7f3435db2ede214f1f2ddb49051b3fcc2d7d9574e3c`  
		Last Modified: Tue, 26 Aug 2025 16:51:30 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42d19e5629e404b539dea7a92dd4e1c28fb152ac4fd387f335112d967fa42bf`  
		Last Modified: Tue, 26 Aug 2025 16:51:24 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1ca2dfd325862cf53869f98b54b6f269ff3825c7252e5b75a53ee4d34e31056d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580baac8e15bdc972db7c72085205331fa315a8f8220664084639bbaa46e484f`

```dockerfile
```

-	Layers:
	-	`sha256:4420a9c08aeaace20f6102f79d7704bd2d2d759ad92e107297a5e3b71f8c6b35`  
		Last Modified: Tue, 26 Aug 2025 18:20:20 GMT  
		Size: 19.4 KB (19431 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:82af53ff59713b0b3586af4f2977b2d5ab7df673be720e9037f0df2f5c726749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78963604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e699f34e611ec9aeac4b9938dcf600cb3d115e33cdc619e45b1006461b9ef15f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7d2a57f1ef9f97b49b6fff28a7126d97e7198d9c67b1f4d38730c945b55a7`  
		Last Modified: Tue, 26 Aug 2025 17:44:40 GMT  
		Size: 75.2 MB (75234430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bbc6a66435fbe346aedb5478520c0031df4d574bfe13b98d36123bd0cb1522`  
		Last Modified: Tue, 26 Aug 2025 16:57:41 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455ca0fa6d5a336db59bff2f1f594bb7899650b7763648479f824021cffa2a7`  
		Last Modified: Tue, 26 Aug 2025 16:57:44 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:582db1db9c028422995048d09a52f5f13e30d4a775813f9e7722c3c2105907f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3351982c781fc09f6de5ff55d9239383b65c53221e66d9276d7d3b08204962`

```dockerfile
```

-	Layers:
	-	`sha256:962692efb06cc7405e9986b44b7931d8c5120419ab4aace742096f778b04db3c`  
		Last Modified: Tue, 26 Aug 2025 18:20:23 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:7112d826a48691fd016859332f9fee9f351e69dbc356b59861aecf05372c7621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73520274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f1caf4dd71bd936b7e54525ae5ae07a1da8ae4899f5e60d3b22e024f31aff0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.7.3
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495f345eb737fe5e7f7d583c0f6630cf80a4d67b95ae9bd76902dde2dba9d51b`  
		Last Modified: Tue, 26 Aug 2025 17:04:01 GMT  
		Size: 69.9 MB (69873239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c307bbaffedd8c00cddb99e59f7d3697e3e731371404ac5e8955508c13d7a93`  
		Last Modified: Tue, 26 Aug 2025 17:03:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415def403d1cc7b5626e73089336be57199faba9279eb128d414f71dae0fad10`  
		Last Modified: Tue, 26 Aug 2025 17:03:52 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:6b5f52d363112af7587ab99319549299d91a096b9a38dace51b58f53be34cbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74086b67192616f0b1ee67becd30f028625db9af6ee7fe3897946a283917d80`

```dockerfile
```

-	Layers:
	-	`sha256:921ec808b8a72d9cbe23454e94ef9fb544514404bf06c731e043eed5f4e2025b`  
		Last Modified: Tue, 26 Aug 2025 18:20:27 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:86655495a7ac80e7fda84f19f1eee579435fc22204562c34db13fbaf4102f436
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
$ docker pull varnish@sha256:782bd500bdb785fdb7985580fa0b73900fe962f2d6add4ab0946e2e1f69ab556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116340261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d16006e8ae81f8f4f1cef1f748768ea880de2571a18c956ab825f14ab43964`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd0391d5883cb827d680d347a739b3ac285458ef597837bda7523f0a973f2a0`  
		Last Modified: Fri, 29 Aug 2025 18:58:02 GMT  
		Size: 86.6 MB (86564929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f18a62a208f5f2eb2041475b3216fe4a1c7b8504500ecab7ea3cc68a7f482e8`  
		Last Modified: Fri, 29 Aug 2025 18:57:56 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b91bb588fd3ef1a72ee515f842eaef66d07efac4f7532be94eaaffab957db5a`  
		Last Modified: Fri, 29 Aug 2025 18:57:56 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:e9ebb92bd3223ea842c0dba0b5e7b617f0e40a44dc3e6f278fb8d41ec5c569c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7ca5fb0a6e2724c258065f33f5234ec33b438c0e2595ad17f194c0541fd540`

```dockerfile
```

-	Layers:
	-	`sha256:eb95f7f1490761e6d482aa0115f80ec0ad51f34293f9c6bc0f57dc6e7be44580`  
		Last Modified: Fri, 29 Aug 2025 21:19:35 GMT  
		Size: 19.7 KB (19659 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:68553fd4fac212872a82a9bca4f90aa0fc69638094c46c365f791db6db74d8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87147139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ea9b8a9b4396797a250bed48de5272f14681811ecd7e368deb2cc144949fc5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab1630934ea323c0d50cad725c7dc5f676c44f7a37a7c722547b3f8329a540a`  
		Last Modified: Fri, 29 Aug 2025 18:57:52 GMT  
		Size: 60.9 MB (60937606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c629879bc4ea3aea6aa633a3d7637e4e66fe14911635796f3561a26fd4907a`  
		Last Modified: Fri, 29 Aug 2025 18:57:44 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2ca73afdb667b1da50b2ea4d322fcd05513a1911e2180eb861163501ca2856`  
		Last Modified: Fri, 29 Aug 2025 18:57:44 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:a5603bef1c4cdb0221c96fb8fa2ab6b88e8d5c677ac5f8bea234ea23c2217b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ff7de3d1eba34853220a869769d6c88bea927eb496790491ad9b454d5bfcb5`

```dockerfile
```

-	Layers:
	-	`sha256:009e4efa2775778a8bb24ee0501047432be01274e856457fdd7411ddb3cbf444`  
		Last Modified: Fri, 29 Aug 2025 21:19:38 GMT  
		Size: 19.7 KB (19743 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:87e15ca38843e689554f2dac5f8df19676dc4360ec484c367710a0275ba2cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110518057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35c1a9ea2a4ea53bdd656f6df8a6a591d583ae479a541e5bf9347939e87cb04`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095ad00879fa642ecdc94b591fafeb1acb212eff67e42d43e95a0e34fcd79182`  
		Last Modified: Fri, 29 Aug 2025 18:57:55 GMT  
		Size: 80.4 MB (80379967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6844b8a704384fdb04db8dcf95cba67fd2c38388f9bfb8d5135199b792d20`  
		Last Modified: Fri, 29 Aug 2025 18:57:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b4f6076a264c3d34d430c878c986ee818ad85c4dc0443f3b8a67b58de1e2f4`  
		Last Modified: Fri, 29 Aug 2025 18:57:45 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:907b29abed401a16407383031774c0e121cb5d5afcc701f7242f24cfb230bbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66ddfba9ba0b7ff583cf8ee5d35099f251fd77e0a2bc364020d17c83a34fe99`

```dockerfile
```

-	Layers:
	-	`sha256:33d1899c4bb8d5f0a4d251575b523821bb8673bb60f18783991b9b31d97a9af9`  
		Last Modified: Fri, 29 Aug 2025 21:19:42 GMT  
		Size: 19.8 KB (19775 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:9880404747e278ecd087f5c6eab6bf8412c5b0ba50e991d6485083f61c34c1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114474612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaad62c8bff104e799093949a5bc72dcd1384b6e4388ae6f5c22a60d2830496c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045a468e3f64ef6078d1ad0e91b3c7c3410eba4b86e0f19e58de4a79c943fbe4`  
		Last Modified: Fri, 29 Aug 2025 18:58:09 GMT  
		Size: 83.2 MB (83183184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd71a380ffd5bdf2c24926cc53a053ce7702bcc2cd91ddc403cae22324d9013`  
		Last Modified: Fri, 29 Aug 2025 18:58:03 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7e5688565f7d12c50095b16053ccd03b6bbd73eccbc3ad67630e5af409894`  
		Last Modified: Fri, 29 Aug 2025 18:58:03 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:91b2780598d19fbfd5c2338ca231d9f798365da615c4b783a2c02eb230cf5340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ed2508357c088e800ceb6ab07a53c0d770560c6445f872add3ffaaa706e172`

```dockerfile
```

-	Layers:
	-	`sha256:9d50147cb40bae096e956219787393ef28d1de2bad15ebe6f44b95d5de4b4f42`  
		Last Modified: Fri, 29 Aug 2025 21:19:45 GMT  
		Size: 19.6 KB (19623 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:fb93b07d38aa9c60ef29f22da422d0bf4db0ab2a36fb584e15da11e2fc855b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111785588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cc1ecc30191b0e4f6019dd9e57152f7ceeb6cef146cd1f71f6912df8fe2a41`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeaa7de33323e9da003d76c1a5cc0bb86f35d215429e0d9f20b652378d97952`  
		Last Modified: Fri, 29 Aug 2025 19:00:08 GMT  
		Size: 78.2 MB (78189327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e630fc6d39e8589329e37f5a61e56e9ebfc7eeca0d40411c39bcc2bfccaae5e`  
		Last Modified: Fri, 29 Aug 2025 18:59:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ad6337d770f926d12752f7f661984d17f9c36353f6a8ebb231a5ad950de3b`  
		Last Modified: Fri, 29 Aug 2025 18:59:58 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:6533ac132bd0b294ecfc3638cc8b04c2ab50ca74d45046cfffa7d442aefd5f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ad9d848ff9f848e7dee20ff109298b8e870674df25d11405b571e816436923`

```dockerfile
```

-	Layers:
	-	`sha256:2de9a81e8b94b8729ba0c57f208af387d8dc241d788317f3097bf40bd0628bec`  
		Last Modified: Fri, 29 Aug 2025 21:19:48 GMT  
		Size: 19.7 KB (19707 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:316e16056f396da312924e65681e867878b12ffbd091bec4b8bfbdcab3d2e757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93293676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644c7b17565ef9c3c605d4da40e1fde193cbb69da7fe5eec550f1ccc75788f0a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.7.3
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.7.3 DIST_SHA512=2de3f19d24e42ec092076226b629dc36d4d3c9961454502e7f9a8ff1d440cf54104198e2b5302361f093fa221f04f836bb8dda441921d1721b1d05c90c0f1661 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1660409013e5bbfdf7e7587ce45ef14ffbe6f4f1ddf9e2334a36aa2db6abc0e`  
		Last Modified: Fri, 29 Aug 2025 18:59:41 GMT  
		Size: 63.5 MB (63458571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075bbb82d37082573ab3e19d8791666edde05284ddf8f73f45bde1f03eed1d9`  
		Last Modified: Fri, 29 Aug 2025 18:59:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683e60bd286912e7a79cfb7dc558aef4ee7e621471a31ad8194f8e80357adc97`  
		Last Modified: Fri, 29 Aug 2025 18:59:33 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:99ce5f6dcbc57b14b71f0a9f3990b5f6a78c7e76cb46fa68e49feab34553fdc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd53bd2f0c8cf8cb92f86f286a45d39252faa5929bae160e1e0e5bfdc3e0021`

```dockerfile
```

-	Layers:
	-	`sha256:b4508a75879abdd43a4e164b930d4eb6ab29efba0488ae7ed5c37f3bc5c2afb5`  
		Last Modified: Fri, 29 Aug 2025 21:19:52 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:2862d218eaf5174ed6c49d05cdec7c541ac1cd187eff4525857a72e20532cf39
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
$ docker pull varnish@sha256:45296ae674b736210082997b7c92da397841d1b21196a7f10d9cf5614a61d8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116169441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94fece8572b82c77fa999a9ccf45183eb0ababb78b941c08a8006f14fc7d0f0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aafdc0f6845c6314758ea5569b830d13c704e4189855dafb5cbdc30b9169991`  
		Last Modified: Fri, 29 Aug 2025 18:58:02 GMT  
		Size: 86.4 MB (86394109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ac55296cc05f4f50014679cd428d83c67bb46c4c226898f5a7783ecc0600b`  
		Last Modified: Fri, 29 Aug 2025 18:57:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f32565fad2ea9070650b9b05ff19f924c6493c601cc3958918694e5f4e150e`  
		Last Modified: Fri, 29 Aug 2025 18:57:55 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:3806a133bb59adf5a8b56ee1c34c23fa3c07c7d5eb5b92d9102205def82ba2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079ac8dae3eced627c6b98a34fb082e3c966fc3aa1ca001ecf0f2bb00d0484bc`

```dockerfile
```

-	Layers:
	-	`sha256:e33a69edbbad8d863cae61e0a295cb7c61e461e870f5de66530c76d4b16130f0`  
		Last Modified: Fri, 29 Aug 2025 21:19:51 GMT  
		Size: 19.1 KB (19075 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:905e492b4e13eb2216f2f7be0e6f0eb98f6dab06a21bd6211ec56ded65e46a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86981619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e693710bbc6b9a8085271f2a15abae7c9b2efb4eba4e9db0beac0dfd1c46dd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1d4dd19271e3d461300ca6edbd2f656818c6c3122611f8fb62ffa8e3da5ed4`  
		Last Modified: Fri, 29 Aug 2025 19:00:55 GMT  
		Size: 60.8 MB (60772084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4746b95aa20b62727e54e73688f9e148c9b15e047d1a4cdac39dd1c8356bab70`  
		Last Modified: Fri, 29 Aug 2025 19:00:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4444a7b8087b688e02877dbd3a852ebd2748592c8466d92392d4309aa3b58d0`  
		Last Modified: Fri, 29 Aug 2025 19:00:42 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:feeaf6e2216511f5cb0931304b8cc4ad9fd78fc60277a7f21f54573ea5b5351a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c63228a3d2f58f0204922e78f1554c95d832be32519d9704cab53205159eba1`

```dockerfile
```

-	Layers:
	-	`sha256:569114f4cb82d4b50d18d99e1ca84fe00b7d9d6fad4a133168924a7ec0c826fc`  
		Last Modified: Fri, 29 Aug 2025 21:19:54 GMT  
		Size: 19.1 KB (19143 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:da7bf990f6f149f133218eaba42fda8f69d5c7d908f65deb6103e3d6d83472e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110350109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5d5e9cd9206075ebc9797665e6bb2f3f2ce2f88c2018f3ae5a0a8f1eaa6346`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e19e1a0efaedfe6217ed6bdf97d04d1b5b6cc3aa4a0f669711965a64be863a`  
		Last Modified: Fri, 29 Aug 2025 19:00:24 GMT  
		Size: 80.2 MB (80212023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8654c06c0ddb58abe0f594dca4fcdb1728cbe2e1d0caef544ba713fe7a2d529`  
		Last Modified: Fri, 29 Aug 2025 19:00:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3f62c8866ff29110155eceb7a782254918b48828d870a48e691d67a83e3f91`  
		Last Modified: Fri, 29 Aug 2025 19:00:11 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:422a5d4fc5d7016171bf07ed7e576ed64246e05d374655bb32339d8b393195db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad6a88f8ad6c6a75b72da680a295cc214d53376c4aefecc2826744a357d14bc`

```dockerfile
```

-	Layers:
	-	`sha256:592b08a80afb3bd747f044210fbe7084608be8cde41c318ffb61de7ae47d6cf2`  
		Last Modified: Fri, 29 Aug 2025 21:19:57 GMT  
		Size: 19.2 KB (19167 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:9b49c255a79105f56f9f5930bcbd148523616237ddd78656e3c61458513d62e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114331197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4116ea46ebe15c9fea54ea1919c19987809aa823bacb07b1e4166c4a1a2d6f7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b653d48e2ed0ae22132c116eeca0327ea1253db2ee63f7506f7db701030256be`  
		Last Modified: Fri, 29 Aug 2025 18:58:50 GMT  
		Size: 83.0 MB (83039775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ac55296cc05f4f50014679cd428d83c67bb46c4c226898f5a7783ecc0600b`  
		Last Modified: Fri, 29 Aug 2025 18:57:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccdd71e25e36e6758a960942ca184e20826dc86cb04b04b3dbb79ca43ab4c10`  
		Last Modified: Fri, 29 Aug 2025 18:58:34 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:03dc1fb688bec5b31b14c0fb39e85e423737a222c2fb7b515f1cc0bdd6af2af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba3f6cbb7e8ef245c726b1211b502a9a017c0c30a3fa46707aa4da405e25740`

```dockerfile
```

-	Layers:
	-	`sha256:a44a961b7acc357e6833e76c5a61a7dfc154ccb0d4fa806338360892871b9cd8`  
		Last Modified: Fri, 29 Aug 2025 21:20:01 GMT  
		Size: 19.0 KB (19048 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:501a25b09de46b5f821a4e43eace76ac3c59a1362c4f00a1f51525fadd32af7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111630089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d8372da09852672b9e8816ad943089c72905e765f71e364b566d8a21154130`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc13e4d48b41dfde630a9184655d018075902d953333b8347d5e348aa2874b87`  
		Last Modified: Fri, 29 Aug 2025 19:05:06 GMT  
		Size: 78.0 MB (78033829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169a0308b68f5f63e4c023d0c237261658b1eb70ed4e8b25f52b9b368da9b2f`  
		Last Modified: Fri, 29 Aug 2025 19:04:42 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a89a4d3f2bba8425dff2502e1a9b435355b176779a746e8e641f331ac3fdab`  
		Last Modified: Fri, 29 Aug 2025 19:04:42 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:44c717ee96fe1d79666cef219924bc97d7f5b5c3a6003a4b9641ec16ea92d4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e5eca42e31c466851d0633577843ac2652ddb028674e38bffb915937215a74`

```dockerfile
```

-	Layers:
	-	`sha256:78fca917015de0b7d224792b961841e954aaef88c18e016747b0715d79a0f604`  
		Last Modified: Fri, 29 Aug 2025 21:20:04 GMT  
		Size: 19.1 KB (19113 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:2909c1b4f47f219d0ed74649743f21b8be5a06c35eaddbe908c8ba00f8c743b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93129994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49672459310fe0bb3e4d4efaf09c70046db0cb27cded27c50d68ca3f142284e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Fri, 29 Aug 2025 18:37:31 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_VERSION=7.6.5
# Fri, 29 Aug 2025 18:37:31 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 29 Aug 2025 18:37:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 29 Aug 2025 18:37:31 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VARNISH_SIZE=100M
# Fri, 29 Aug 2025 18:37:31 GMT
ENV VSM_NOPID=1
# Fri, 29 Aug 2025 18:37:31 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
WORKDIR /etc/varnish
# Fri, 29 Aug 2025 18:37:31 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 29 Aug 2025 18:37:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 29 Aug 2025 18:37:31 GMT
USER varnish
# Fri, 29 Aug 2025 18:37:31 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 29 Aug 2025 18:37:31 GMT
CMD []
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176a7536be148e977a8fdc806980aa397eaf18445c550378857fcf89f803c2ac`  
		Last Modified: Fri, 29 Aug 2025 19:02:40 GMT  
		Size: 63.3 MB (63294891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a31f08be4a52e37428db003901e499cb1dbf9a15270aa06d7797ad13e67c39`  
		Last Modified: Fri, 29 Aug 2025 19:02:36 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd2421d3d30817464293d1d84d3eedc207d3286aa8053b81012857a25c65f7d`  
		Last Modified: Fri, 29 Aug 2025 19:02:36 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:61d2019a87faf880b4aa272a56f6d19485b2f1be336f00a96f408975507f2063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f20c86647a60b61f3bb2231c7999f7b2afe10a3645fd31e0f785fdd382a648`

```dockerfile
```

-	Layers:
	-	`sha256:c713214ddad6a75eb6c994aa47b946374068799725ab8856885bf7df602a7b28`  
		Last Modified: Fri, 29 Aug 2025 21:20:07 GMT  
		Size: 19.1 KB (19075 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:eb21e9f988be93f33ff9a0025d0a00617d49f3cc0cf59e0f2167bde7724eae6a
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
$ docker pull varnish@sha256:eb59c7c733b51c1b939cbf9ff520c263bc0c9299508d387e2c19d9df44ca052e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82842456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ba779d3e802e8d23096c4540664cc96d8536959d5b074aa304623851eb7b6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d21ba25e42c221c38da4178d142633a0f4b5df2ea8c3f3d106f42d0b10b443`  
		Last Modified: Tue, 26 Aug 2025 16:51:04 GMT  
		Size: 79.0 MB (79040710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da539f12306b86eb6f4852b5fc70b75a09cef49e31798ad611f63cc267c02be4`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4cd983d1fb0f0789a1a89e664b291a4a4661ccc517311755de1f6948133737`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:cca42d774f271c82579cabffc4db3bfc1035ac3771304e71f720aec531157efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b7b3c041668a547dc1bbb7950733445e113d810c45c9270e7a06ec1477f0bb`

```dockerfile
```

-	Layers:
	-	`sha256:352b25a10911cee1af8da5fbe36f12ae99a4566e98353faca1c19a1dba719b8a`  
		Last Modified: Tue, 26 Aug 2025 18:20:34 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a45549c23c64999161d2144378f8972638bb135b9ae2a82f7a9c677827bf5ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64309206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2054d8cf53e95e19697765491d67a689b3bf8bbd4c17141d0793f38d883f13`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df002cf37151e7b0fa6b77dce491cac03f0f43e0787475b1164effafe412756`  
		Last Modified: Tue, 26 Aug 2025 16:52:10 GMT  
		Size: 61.1 MB (61088108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8f13ade0c407bc30c2d0943af75f6686574b0f26d379104e3c205bf45afc9a`  
		Last Modified: Tue, 26 Aug 2025 16:52:04 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1122e1df195890d89e2ce223091d4fdbf016c09a99097ad0d2800e51f1c1b614`  
		Last Modified: Tue, 26 Aug 2025 16:52:08 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e2ab0e3e19ebf7c6ca62c6b44d5ebcf558dae64f334ad28c878643af087cdd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cf4ba26c47448e64139df64da0a0b9fe67159038b3408e9b09817f12aeef0e`

```dockerfile
```

-	Layers:
	-	`sha256:ce92da7aee86b3186c4df792b992aad5793b0bd68a2cf58e2c87edf2d1ca25c1`  
		Last Modified: Tue, 26 Aug 2025 18:20:39 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cc7a4c790e15bf6bf5226b0d410417ec9f531d5a753110a66b5ab276c31d529f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80124371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcffa3fc8649cd6ecd6bf2901185697844222260efa02f05e99731db0afe6372`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61af1543a395f4ec8e503d693e122083a940bf2bb76d515063e5143006014daf`  
		Last Modified: Tue, 26 Aug 2025 18:21:12 GMT  
		Size: 76.0 MB (75991566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12d13ffdec5777bc9a087e7b6a7648c20098407baf88c27c9e7fe4aac7d8762`  
		Last Modified: Tue, 26 Aug 2025 17:10:48 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829db24f940156af11f84479793cc2a0a0cfe14343815b44983b6afde47268a1`  
		Last Modified: Tue, 26 Aug 2025 17:10:51 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:0ccbeff7dbfb12f5d18c9f0cd5717acfb9ad1edf5aa9e6b00ad5b3b40c42d048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eb6f4dd4f15da4e733fba7d1e89c9f575efa966c077245df747443c718e3f9`

```dockerfile
```

-	Layers:
	-	`sha256:2a51627e99e6e144059176acd8432da0742e66b7680ad3e45c9b5b7b842abd83`  
		Last Modified: Tue, 26 Aug 2025 18:20:42 GMT  
		Size: 18.9 KB (18910 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:79de57822067c316205cf516f35730d9a48eba17a18438068b7f040a24ac3b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84867078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5504cbcd55267abd7eb20a78d9b5a7b750049aa4bc605904f43a56800e28e91b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8566fc257dd8fe62b706fceeac74d505c8d4f452f47443ab24c056b45d36a39`  
		Last Modified: Tue, 26 Aug 2025 16:51:00 GMT  
		Size: 81.3 MB (81250013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c902672d8239c81bbf78276bf948224102a95c14aa1c3425a2cd8d61ac8e72`  
		Last Modified: Tue, 26 Aug 2025 16:50:52 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b659f1d057b1bc172c204ef2be2e113d569f720ff55a3eede5412aa84a492b`  
		Last Modified: Tue, 26 Aug 2025 16:50:53 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:18c78749465acc21014ef75082ab645316c03195ac2240e39400c554dc25c080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745deeff47c188553c23284121381997db93b89c2f4f6a3ef25a5fde1cd3a4cc`

```dockerfile
```

-	Layers:
	-	`sha256:a0fa618125b27a4ad09d1553205573bf7cc3d05fe296ae1a5916418c2bef17b2`  
		Last Modified: Tue, 26 Aug 2025 18:20:46 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:edff5c8cf592568cd0c8a1791adb5a4c7038630e2396a74f30fbc286cc02d57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78817937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4e4f81bdc94adfb2b152c4986a786099e213c8872a0a447de1940eec8b36b9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41580bfa7bb549e94995896f5201eb9cea1494505ab84bd2126449b3a80d8788`  
		Last Modified: Tue, 26 Aug 2025 17:05:11 GMT  
		Size: 75.1 MB (75088762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf19c428ddd5472d5705df46e95a523161488ca0d2e70ca9bebd0089f1c233e`  
		Last Modified: Tue, 26 Aug 2025 17:05:02 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf0cd2ebebd5e2b3680f333eeeea9e24af8c1deab3442ac0419289d59b88528`  
		Last Modified: Tue, 26 Aug 2025 17:05:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a97e2c5ce5f5ae8715cfb5aa54bd600ceda8d156a4d95fe1b69ffe7160544d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd36779ff7171b497584aecf1336f80b2271cbe770dfffecab9b37499691c10d`

```dockerfile
```

-	Layers:
	-	`sha256:4e868d107d4ec0f88f2515d8c0e461129f2d4c2412b6465284b4d66c9941ba81`  
		Last Modified: Tue, 26 Aug 2025 18:20:49 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:6bc7c34f4a8c82a84964269ceb7da23eadc1bfbc06e1dd164456a4a7c5a8f064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73373120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7df50cfa2eacca4e44264105844791df8f7c91eb09af124a198445860554b81`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d347e847918994143d8709387f507640aec9549648f4ab8dd0dafaf35cda058`  
		Last Modified: Tue, 26 Aug 2025 17:17:15 GMT  
		Size: 69.7 MB (69726086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564bf67e3d60e0acd5d9612a5dc1bea2c8e30ed426161ea842a2c7203a7aa9f8`  
		Last Modified: Tue, 26 Aug 2025 17:17:08 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e8e125440740ba86e9c177b062cd9e2f77e2e8a5baecdf2b9627697318b17e`  
		Last Modified: Tue, 26 Aug 2025 17:17:08 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2040c4c901971ec2aa62d7f20a30a283a3855e4e980e1567c742de35e05f9d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb0b839668077db2d493c4e6f89335931c594587b4958d1d9f5c3171fab912c`

```dockerfile
```

-	Layers:
	-	`sha256:94a86035ec439c327f30139139dfafa0ae939c638319e9658f08da45c2eed1a3`  
		Last Modified: Tue, 26 Aug 2025 18:20:53 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:stable`

```console
$ docker pull varnish@sha256:aa957772ed72442badfc97503c7060712e882cf0a7c040d2123573882a90109b
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
$ docker pull varnish@sha256:7cbd3be8de1473ab7d729e2012007525a32dab1c32f01c66750a76c2dd6a3dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103551153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee7a302b300e0cb28da3f0880ae89e521db3f03ba8249d567a01a52c87ad28e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fb9407627d2a9673f9f2996eaefe14a925c79c1d6760a3bde4f7dac638edc8`  
		Last Modified: Tue, 26 Aug 2025 16:51:05 GMT  
		Size: 75.3 MB (75320140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c8bc1dd94e689fb630ab2b2a2aab8ea10c3a98fc336e39c91ed99ead7034ba`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 726.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:cfa7954490ec481b365f10b95e49c759856ea3ed871b62e4f3ad3389b73a81a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3706ba5ff3090a5ae767c72196968b3985e0e33ced0bd740df008593e1642394`

```dockerfile
```

-	Layers:
	-	`sha256:924ba8f8c4217d028b2f271cdbfe266029ee64ece4214470a2274aa4a6907ede`  
		Last Modified: Tue, 26 Aug 2025 18:19:31 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:67a552aaf0a0bf11116498591becce6ad57e528d4b447459e2138cc8858e77cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75973152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584645e54dd6e80ac1b2b9683f0c5b6533ce57e5a8b5bb136f9aa9b65b4bdd84`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694e45c2ad1ef6dbad25ffc201a18db57ac9b1f77c3963b7253079914477ddc`  
		Last Modified: Tue, 26 Aug 2025 16:54:20 GMT  
		Size: 52.0 MB (52033469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3e2473be879b601edfcf51083f41cc2c5a52f77f88b33aa96ca7e00754017e`  
		Last Modified: Tue, 26 Aug 2025 16:54:14 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:8a8c4e092458ba65ade061405ce3b0db4d1c90e5c00d579856a60aeebdc83470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e42311eb05fdf74621332f9c5ed20f71b0929d5f7d49de57df10a1b2f5fd012`

```dockerfile
```

-	Layers:
	-	`sha256:26460142477d0a1b71cde5a5ea3b590142211fc13d2aa4f9d11dec9898ef06d6`  
		Last Modified: Tue, 26 Aug 2025 18:19:35 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7947f456530af586dd14fc9b2ee5e323b3937a7813f17b8f5bc2eac64f7d321f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98372014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3973020c0ead804b1fc21b077ce805dbbb560aba29ab7b7b708a4c8ccbc08996`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fa0bf97d17bbeea81d2494c7f6ea7802aaa88cd8b8b476210467e1416c35e7`  
		Last Modified: Tue, 26 Aug 2025 16:59:55 GMT  
		Size: 70.3 MB (70289258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46723a79ce1a6afa1d880e4f0e59b65181a0327ff1ee22ad41e84ba426d2cd8`  
		Last Modified: Tue, 26 Aug 2025 16:59:51 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:3b30836516d8ef42543dd00040504764a4c4484d6a00d64ec8987ed0528ad47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579f165fc8ae5c798a4e2701e9479d82bbedaa55f3dd6201d6fe6c5f3728aaf8`

```dockerfile
```

-	Layers:
	-	`sha256:0519eb52a002246bc5923205d8e4b70f6978f3b2ecdfa4a23a9f736b593978f4`  
		Last Modified: Tue, 26 Aug 2025 18:19:38 GMT  
		Size: 12.8 KB (12785 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:2c5e6985d41327cbc8643b452c59764e1613f50a3b117cde8b684b50fdc50950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101012369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e63ef78a68ea4bf792399c15bdde269e88a61aa5c416925cc36c11dd66ad66`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102c072a05728f7a803239b2eb5dc78890f98f54a8014c8cbd1e6dd030c6fc9b`  
		Last Modified: Tue, 26 Aug 2025 16:51:06 GMT  
		Size: 71.8 MB (71799009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf2c5b223c5b80c6b598516e2900c4dc71f99d9796f990a1a2e3f5dc0e7da99`  
		Last Modified: Tue, 26 Aug 2025 16:50:52 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:800c990346e164b99d62c806c6e052adee15320e0d6dc5f809a8e06a41714f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbd36ff74ebe940838ed9965e0970fa1ae0bd79c0ca889995c365cf801c9137`

```dockerfile
```

-	Layers:
	-	`sha256:1ea1c351e16e7da1014311d822b69f527c6175936cf287a735e29da5ebeb9109`  
		Last Modified: Tue, 26 Aug 2025 18:19:42 GMT  
		Size: 12.7 KB (12666 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:e6b5ae618eacb7eb0133f5eb3181be22375c4b10e66899c71e17c3a24082e52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105453540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85e1e44c3fd0ad39dfe8fae37252892dd8e135a2511c415a7a2f96c6e93b09a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ea7a8002f28a34c01ba581d94952206b784a0f318fb381fc172c4b7480e157`  
		Last Modified: Tue, 26 Aug 2025 17:10:14 GMT  
		Size: 73.4 MB (73379366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5be6e400d7be941426e0d23d914b2621bd09a36a4e2ace6e8932d088497fda5`  
		Last Modified: Tue, 26 Aug 2025 17:09:59 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:aba0a640ac2b97154eecdff5b12c43f8d1a49aeb2a8329e1d9ec77a9f379ac74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c43528322730971f228ad2a545313b36fa5ab25716895e933e9d018d8048c8a`

```dockerfile
```

-	Layers:
	-	`sha256:d4859fc31065cc14ac9281aea1869b5bc5a134c4470f9259d499303d4f4af48f`  
		Last Modified: Tue, 26 Aug 2025 18:19:45 GMT  
		Size: 12.7 KB (12730 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:54424b955926c93cdb7c182553512dff290fd0eb4a0af9d68241d8ef9e0e7eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81339059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dae65dbb781c3a9d21184450a7784cf5eb3b7905f7671bb8a1e21d3efaedac`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8088d9284f19de0c8967cbf0a62ab5e1d64ba1ddf753a30f29fd51e37f7ddb7`  
		Last Modified: Tue, 26 Aug 2025 18:20:19 GMT  
		Size: 54.5 MB (54450468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663a3924ff7952fc97c3a5dc37c8fbd957d14231999ff14d0c6eebb7f9f77868`  
		Last Modified: Tue, 26 Aug 2025 17:36:49 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:caf935fe01dacf82f134899bd70342c4cc73b59ace7f8dfd85ce24bea14a9f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c74b115bc1ce0225884fc3a7e1f201e20fe235665e96a88d74f88b61683086e`

```dockerfile
```

-	Layers:
	-	`sha256:ceaf024d37a6a7c15996bff2dd71860f2f7df3d73802dbf47330c3d0bea61e0f`  
		Last Modified: Tue, 26 Aug 2025 18:19:48 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json
