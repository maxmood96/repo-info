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
$ docker pull varnish@sha256:2feff07af34515467b14e78c1f57ba34ea8d14d2ea92b91292423f91959532a7
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
$ docker pull varnish@sha256:be38eacdd90a91c5a2b83b2a514393a1ad145c131d01c978fcb506c8acc6ae19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103549427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d4b38bc14671cce6ee2b38d639ddc782fda68c588e05f77e474ba2f93ef1ea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc34925c959542e1e775e8577e6422eb6bc393fdff50be15cb1ddbbb9a844d93`  
		Last Modified: Mon, 08 Sep 2025 22:08:52 GMT  
		Size: 75.3 MB (75320326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df1cef4f661e5a17ca4bfd74416369abb8265ebac3e8179db0d4872d07ae90d`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:11b9ca6be19340007a7ce7e34f3e60f286a2840267debe45b89fc363223568eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8e43ecc9cd4d5f8175fba6bcf7f3c6028535c28c1862578251f5245121700c`

```dockerfile
```

-	Layers:
	-	`sha256:4c77bdf7c8e959323db56f78f2fa65d1f23c64233329860198f2f4a0b7d8237e`  
		Last Modified: Tue, 09 Sep 2025 00:19:26 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:83d0eb092587fb5442cfdbd0359adf6882ca26c5fa9e5957c2aa9997f7bf8fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75967394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca5d3d8e50e1364c4b1de38f7a093ed938e5b162b5c7c87a5651993f42ca6c7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
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
	-	`sha256:e747f8ef7f1d9a41c99bfb53889f7b8de3504300740a326627fc7522904708cc`  
		Last Modified: Mon, 08 Sep 2025 21:14:21 GMT  
		Size: 23.9 MB (23933904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a96e3e9f59bc14457ad942b973f0d57ab12afaff6dc14cb34cb73d85b3ffd4`  
		Last Modified: Mon, 08 Sep 2025 22:49:28 GMT  
		Size: 52.0 MB (52032733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2319aebd117135eff4658d33b156b6b2a9d49f00ad83a96a75352f08061c664`  
		Last Modified: Mon, 08 Sep 2025 22:39:51 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:761cb4d694b8df422a48c010a217c18afca4cb7b51be9d4573e99562c98d080e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dd6497965803a8eda5b5e176c760ebf0c549a405b5127e071dd297beff09b2`

```dockerfile
```

-	Layers:
	-	`sha256:533d2079eacc98d46a2c79d10c8af512dcc0ffb6699d73c883e1b7b2bd750c9a`  
		Last Modified: Tue, 09 Sep 2025 00:19:29 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f655ffc11d5f56663ecf62d77a29dee3bf6ff8b7976cb0930f0d2ce3ab00dc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98404475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f265a7695386d7aaef5f45ced676dc9eff2437ba9b68bdff89234a60a21f78c8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f3604c9d6c5bd2bd42dfa6de3534592419579a2f1aedf06648c0bbf6a136d`  
		Last Modified: Mon, 08 Sep 2025 22:30:59 GMT  
		Size: 70.3 MB (70301621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c938b01c1fb1304d80a769a0b51cbf645149cade2acd897ecbd53d9b38bb4`  
		Last Modified: Mon, 08 Sep 2025 22:31:01 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:d5dd1f6ee1bc7ea8f5ce60af3bfc1d0c5a9f0a784c00000a9f15b0b4a1c04253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad85a772a21422209b63854c1be2ae1834eb939021eb90a7cb352748f9921c3`

```dockerfile
```

-	Layers:
	-	`sha256:02c53f8649fe16d5c7af504e905da91cbdded3b39efe336dfd31c30eea4ce75a`  
		Last Modified: Tue, 09 Sep 2025 00:19:32 GMT  
		Size: 12.8 KB (12785 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:ad2e165c8b1a90ee344f670b0be2623abf9284e487beea34a9133dbe80e31ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101009277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204fe8fa8253f66756ef05be40e3af7205fb1225057a585991d6f16c1a2e4aaa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
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
	-	`sha256:dc2a09b0db8b98044474925cacc9c009aa76e5883edf644cc36c3f6a2e3917ac`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 29.2 MB (29209634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b78d82146cc6d4082a0d5804c71c506ba351a615197ef8c4e728a4edaf1d0bc`  
		Last Modified: Mon, 08 Sep 2025 22:05:55 GMT  
		Size: 71.8 MB (71798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffa68900cf9a604a0f767d161c84a80879aec6ef88255e9a7131d881ed287eb`  
		Last Modified: Mon, 08 Sep 2025 21:42:45 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:056602f331287da74b46d80369349b7bf1974e24e2bd8c331b76bf59647c2333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd9c1b839b0ad41ac1ea5ecea1c95ea536c024237f209d93e167c7a00779e8e`

```dockerfile
```

-	Layers:
	-	`sha256:f9cb9b18765636d42027eff05bbb548e743b509b2ad28f55f503998ec39d09d0`  
		Last Modified: Tue, 09 Sep 2025 00:19:35 GMT  
		Size: 12.7 KB (12666 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:cda3f84a524ce26496944326d0fa01b70d036a03b5ebd533158d74dc771b5ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105448760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0ebeaf1ed77e48a4d1cb9ebfbec5334b02381b14c832f80f7ae2620a39e90c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
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
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc374f61690bfbde05777b216808ef4ca55da9b385772d1e11c2582cce8eea1`  
		Last Modified: Tue, 09 Sep 2025 03:19:41 GMT  
		Size: 73.4 MB (73379243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fb0210a0c4003e5d22dcdff1d2f4adacc7333b8cc018962cd478e2c4cb4f25`  
		Last Modified: Tue, 09 Sep 2025 02:16:19 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:95b564b7811b2f0940e19273c3edbbcba8d048ad314ab12e20cf69838b5b29e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8848e40fc40a9cbda6e721d532704562057c11768aeb759a7461dc43e80eabd7`

```dockerfile
```

-	Layers:
	-	`sha256:413e97a38d767932bdc61c06dfeca8574b71e5e3e907123b2318bf18298d3ae1`  
		Last Modified: Tue, 09 Sep 2025 03:19:28 GMT  
		Size: 12.7 KB (12731 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:d7297d7a856b26abe2c6cf4dcb68ae223583daf2c3550d3425c41409a1a9d5ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81334954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec54986ee0a82e7a66d2124326e72a1d3f6d107ee409784e0775eb3d87c6d4f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781a8b71ec9183860b5d496ba64d7fcb94baf033b0a47bdf697456121aa97ab8`  
		Last Modified: Tue, 09 Sep 2025 01:20:52 GMT  
		Size: 54.4 MB (54449903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6c5868347cf32752b393fd028c91b374fb426c00125c580c514d6ea595de10`  
		Last Modified: Tue, 09 Sep 2025 00:36:29 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:adf6530b925c2fd277152f73ec3be30ac6d739811028a260c80e3e544d2b559c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54a6010917691e007652e9e563302a407b67631e6e06c5887cb3b1310581cc7`

```dockerfile
```

-	Layers:
	-	`sha256:af860943ec06665363dc0c57d26faf0d3f10690a7dc1610c95f2ba15529d8d6b`  
		Last Modified: Tue, 09 Sep 2025 03:19:31 GMT  
		Size: 12.7 KB (12691 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.16`

```console
$ docker pull varnish@sha256:2feff07af34515467b14e78c1f57ba34ea8d14d2ea92b91292423f91959532a7
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
$ docker pull varnish@sha256:be38eacdd90a91c5a2b83b2a514393a1ad145c131d01c978fcb506c8acc6ae19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103549427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d4b38bc14671cce6ee2b38d639ddc782fda68c588e05f77e474ba2f93ef1ea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc34925c959542e1e775e8577e6422eb6bc393fdff50be15cb1ddbbb9a844d93`  
		Last Modified: Mon, 08 Sep 2025 22:08:52 GMT  
		Size: 75.3 MB (75320326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df1cef4f661e5a17ca4bfd74416369abb8265ebac3e8179db0d4872d07ae90d`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:11b9ca6be19340007a7ce7e34f3e60f286a2840267debe45b89fc363223568eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8e43ecc9cd4d5f8175fba6bcf7f3c6028535c28c1862578251f5245121700c`

```dockerfile
```

-	Layers:
	-	`sha256:4c77bdf7c8e959323db56f78f2fa65d1f23c64233329860198f2f4a0b7d8237e`  
		Last Modified: Tue, 09 Sep 2025 00:19:26 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; arm variant v7

```console
$ docker pull varnish@sha256:83d0eb092587fb5442cfdbd0359adf6882ca26c5fa9e5957c2aa9997f7bf8fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75967394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca5d3d8e50e1364c4b1de38f7a093ed938e5b162b5c7c87a5651993f42ca6c7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
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
	-	`sha256:e747f8ef7f1d9a41c99bfb53889f7b8de3504300740a326627fc7522904708cc`  
		Last Modified: Mon, 08 Sep 2025 21:14:21 GMT  
		Size: 23.9 MB (23933904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a96e3e9f59bc14457ad942b973f0d57ab12afaff6dc14cb34cb73d85b3ffd4`  
		Last Modified: Mon, 08 Sep 2025 22:49:28 GMT  
		Size: 52.0 MB (52032733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2319aebd117135eff4658d33b156b6b2a9d49f00ad83a96a75352f08061c664`  
		Last Modified: Mon, 08 Sep 2025 22:39:51 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:761cb4d694b8df422a48c010a217c18afca4cb7b51be9d4573e99562c98d080e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dd6497965803a8eda5b5e176c760ebf0c549a405b5127e071dd297beff09b2`

```dockerfile
```

-	Layers:
	-	`sha256:533d2079eacc98d46a2c79d10c8af512dcc0ffb6699d73c883e1b7b2bd750c9a`  
		Last Modified: Tue, 09 Sep 2025 00:19:29 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f655ffc11d5f56663ecf62d77a29dee3bf6ff8b7976cb0930f0d2ce3ab00dc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98404475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f265a7695386d7aaef5f45ced676dc9eff2437ba9b68bdff89234a60a21f78c8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f3604c9d6c5bd2bd42dfa6de3534592419579a2f1aedf06648c0bbf6a136d`  
		Last Modified: Mon, 08 Sep 2025 22:30:59 GMT  
		Size: 70.3 MB (70301621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c938b01c1fb1304d80a769a0b51cbf645149cade2acd897ecbd53d9b38bb4`  
		Last Modified: Mon, 08 Sep 2025 22:31:01 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:d5dd1f6ee1bc7ea8f5ce60af3bfc1d0c5a9f0a784c00000a9f15b0b4a1c04253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad85a772a21422209b63854c1be2ae1834eb939021eb90a7cb352748f9921c3`

```dockerfile
```

-	Layers:
	-	`sha256:02c53f8649fe16d5c7af504e905da91cbdded3b39efe336dfd31c30eea4ce75a`  
		Last Modified: Tue, 09 Sep 2025 00:19:32 GMT  
		Size: 12.8 KB (12785 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; 386

```console
$ docker pull varnish@sha256:ad2e165c8b1a90ee344f670b0be2623abf9284e487beea34a9133dbe80e31ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101009277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204fe8fa8253f66756ef05be40e3af7205fb1225057a585991d6f16c1a2e4aaa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
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
	-	`sha256:dc2a09b0db8b98044474925cacc9c009aa76e5883edf644cc36c3f6a2e3917ac`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 29.2 MB (29209634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b78d82146cc6d4082a0d5804c71c506ba351a615197ef8c4e728a4edaf1d0bc`  
		Last Modified: Mon, 08 Sep 2025 22:05:55 GMT  
		Size: 71.8 MB (71798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffa68900cf9a604a0f767d161c84a80879aec6ef88255e9a7131d881ed287eb`  
		Last Modified: Mon, 08 Sep 2025 21:42:45 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:056602f331287da74b46d80369349b7bf1974e24e2bd8c331b76bf59647c2333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd9c1b839b0ad41ac1ea5ecea1c95ea536c024237f209d93e167c7a00779e8e`

```dockerfile
```

-	Layers:
	-	`sha256:f9cb9b18765636d42027eff05bbb548e743b509b2ad28f55f503998ec39d09d0`  
		Last Modified: Tue, 09 Sep 2025 00:19:35 GMT  
		Size: 12.7 KB (12666 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; ppc64le

```console
$ docker pull varnish@sha256:cda3f84a524ce26496944326d0fa01b70d036a03b5ebd533158d74dc771b5ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105448760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0ebeaf1ed77e48a4d1cb9ebfbec5334b02381b14c832f80f7ae2620a39e90c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
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
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc374f61690bfbde05777b216808ef4ca55da9b385772d1e11c2582cce8eea1`  
		Last Modified: Tue, 09 Sep 2025 03:19:41 GMT  
		Size: 73.4 MB (73379243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fb0210a0c4003e5d22dcdff1d2f4adacc7333b8cc018962cd478e2c4cb4f25`  
		Last Modified: Tue, 09 Sep 2025 02:16:19 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:95b564b7811b2f0940e19273c3edbbcba8d048ad314ab12e20cf69838b5b29e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8848e40fc40a9cbda6e721d532704562057c11768aeb759a7461dc43e80eabd7`

```dockerfile
```

-	Layers:
	-	`sha256:413e97a38d767932bdc61c06dfeca8574b71e5e3e907123b2318bf18298d3ae1`  
		Last Modified: Tue, 09 Sep 2025 03:19:28 GMT  
		Size: 12.7 KB (12731 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.16` - linux; s390x

```console
$ docker pull varnish@sha256:d7297d7a856b26abe2c6cf4dcb68ae223583daf2c3550d3425c41409a1a9d5ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81334954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec54986ee0a82e7a66d2124326e72a1d3f6d107ee409784e0775eb3d87c6d4f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781a8b71ec9183860b5d496ba64d7fcb94baf033b0a47bdf697456121aa97ab8`  
		Last Modified: Tue, 09 Sep 2025 01:20:52 GMT  
		Size: 54.4 MB (54449903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6c5868347cf32752b393fd028c91b374fb426c00125c580c514d6ea595de10`  
		Last Modified: Tue, 09 Sep 2025 00:36:29 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.16` - unknown; unknown

```console
$ docker pull varnish@sha256:adf6530b925c2fd277152f73ec3be30ac6d739811028a260c80e3e544d2b559c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54a6010917691e007652e9e563302a407b67631e6e06c5887cb3b1310581cc7`

```dockerfile
```

-	Layers:
	-	`sha256:af860943ec06665363dc0c57d26faf0d3f10690a7dc1610c95f2ba15529d8d6b`  
		Last Modified: Tue, 09 Sep 2025 03:19:31 GMT  
		Size: 12.7 KB (12691 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:7`

```console
$ docker pull varnish@sha256:004c5a83a7b96e0fb5d919e5bd6ed6e1753b55193424098053f82930d6a5a41f
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
$ docker pull varnish@sha256:6ea1906f66af6621b5be872303c27e841be3dbfeb25fad920106bcd1584972a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116340831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01e7e6b16318fcf88489ab37bf10ef98f6ab82f29cc546a4e247c7eac136c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18944dae82a25a4881028dd55772eed24b1c8be1950466b6eca61af312c365b5`  
		Last Modified: Tue, 09 Sep 2025 00:19:45 GMT  
		Size: 86.6 MB (86565292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979091d7194e04769585896205808e30477930f91bad468ad1ee0d8bd2f4dc17`  
		Last Modified: Mon, 08 Sep 2025 22:17:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235840fec02341cf6a06d9789cc95025caf43e0fb0546f4d04f761f0a49468a3`  
		Last Modified: Mon, 08 Sep 2025 22:17:46 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:eb4857110035e2485163b912e78d6c7b6571b70179390045e5c98559d6016c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f977ceb09ae86ba9316aefad8d1859df715e250f91df628547048e4e1c07e32a`

```dockerfile
```

-	Layers:
	-	`sha256:4686e767536418e4a698907c2556dd03e0bec42e4c88727a281219cd60411966`  
		Last Modified: Tue, 09 Sep 2025 00:19:42 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d33d114522a19162030ba52c0d519272214d675caebf98a5ad08eb5ab940849a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87147881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae4857cee8b53c7c015034fa7fb713a19d124820b19bb35e190f7e6b96267c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59e639359797c17456c01ec48e4af37d9baf75ee3c0948abe907c4af26067d5`  
		Last Modified: Tue, 09 Sep 2025 00:20:08 GMT  
		Size: 60.9 MB (60937990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180e014771bbced72cbad616ceb8444f6d848941c5d222cf2ca05114acee6bf9`  
		Last Modified: Mon, 08 Sep 2025 22:39:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a8715837fc6167839fb47529731f895e6dc16d9c9611e536684e8b569e33e`  
		Last Modified: Mon, 08 Sep 2025 22:38:58 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:f992b2f49e938ba0f4b0b17151999161f71790a5112c46e2c9cec8015021cf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97486c43c69413bd0cfb916d32fea08f17f534e580c717f1111f51e100a1735f`

```dockerfile
```

-	Layers:
	-	`sha256:8e91e51e2f4a23ccb610579876c56ad109ff00a4659ab6f510d1f08abdf22740`  
		Last Modified: Tue, 09 Sep 2025 00:19:46 GMT  
		Size: 19.7 KB (19748 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:34cd0a30bda20160ff7ae516e04a1c3adef99857d02fdfcaf3ce813c1428842d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110519111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039ab2351cd19844ffc5080315de35144824e0864dfbe6e515900d5f1a66507e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b95db52a59f557a64013c0413ad4c7fdfda02dc7d71dc4ada8359ad435f60aa`  
		Last Modified: Tue, 09 Sep 2025 00:20:13 GMT  
		Size: 80.4 MB (80380435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f1221a4365e75b2f093d2849e49dcd43efab4c3fc25561ade12264e79369bf`  
		Last Modified: Mon, 08 Sep 2025 22:24:18 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac397b371684df07816dd8ccffd8a1d93cd6f2c5551537f329f0b0ab7a40c98`  
		Last Modified: Mon, 08 Sep 2025 22:24:17 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:3fcb990fe9d285b0d6e1511655fd18dd6ada705278900042a7e02128a3d4eb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c980a283bec0356ac4ed751735e36c07ec10c1770c95c332fea24d9fc7ccc81e`

```dockerfile
```

-	Layers:
	-	`sha256:2eef8bd9e2934552fb4337fca4fba8742b2153e1cd79bb4aa0114d701f1ba32d`  
		Last Modified: Tue, 09 Sep 2025 00:19:49 GMT  
		Size: 19.8 KB (19776 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; 386

```console
$ docker pull varnish@sha256:02c9234acad0eb04a624acb34e1a426dbea290ee3784b86c78b474c36781aa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114475602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe1e1d673a9da90136affd095c1aed23ac4ad6dafe10cd762077e5b353f526e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0954a711fdaa9e018a9a6874f258e53d4d982956e83088cd21bdf4838a7c5d81`  
		Last Modified: Tue, 09 Sep 2025 03:11:14 GMT  
		Size: 83.2 MB (83183774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412dfbccb4add8bf8ea9f87514c792eb1cd1ead4780eaa7674e205104cb5d88e`  
		Last Modified: Mon, 08 Sep 2025 22:11:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554eb893a0fae71e2e1992c018c0746b293311942cded5755793b9688ddac647`  
		Last Modified: Mon, 08 Sep 2025 22:11:46 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:79202697d68cbb52332eb571c5f3c6b5807332c4f725188a41005ad0ee7ea8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9f8665dfd530dd16dd6372f423c0935d0a2f57da7ea6e15f046d3126312e61`

```dockerfile
```

-	Layers:
	-	`sha256:1dd9b3af765c1a491122bf4c7a2cfc1509071e35560a190211e441360dbe3124`  
		Last Modified: Tue, 09 Sep 2025 00:19:52 GMT  
		Size: 19.6 KB (19623 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; ppc64le

```console
$ docker pull varnish@sha256:45e721b9ba7357ff98acfdb99721198264110d417fb3e646444cdb0874e0a397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111785987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2d152b59ebf7a541d959405f35f5e76efe5935e5eb69944be6b7975f3d64d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975feffc410074d031a1889b1523855076bb3908dfda525fe57beeb0acaf7a96`  
		Last Modified: Tue, 09 Sep 2025 03:40:24 GMT  
		Size: 78.2 MB (78189591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6c8eafcde7062c2c5d363432172aa9b5849730f606006ac478bfd950f7885a`  
		Last Modified: Tue, 09 Sep 2025 02:07:35 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4361b66c8c004035e5030a72f431c6246e601ff9f86e2db2d21f90427739a9da`  
		Last Modified: Tue, 09 Sep 2025 02:07:39 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:95750c616c60d2cc10939b255833cd544029b2dbe2da4bba06a6c306eb82b4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02143556e0d1a70cab52c94769238b65c2aa3664652ecbc0427221cdd8f2b8f`

```dockerfile
```

-	Layers:
	-	`sha256:8aef501842bf7fdfd1cf343f4ed959a5dcf2e237f59496b8376f4c8f554f8e29`  
		Last Modified: Tue, 09 Sep 2025 03:19:38 GMT  
		Size: 19.7 KB (19710 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7` - linux; s390x

```console
$ docker pull varnish@sha256:0d76e1525b65b81f28d384281945e4e6d194f7e59bcec2d99739f2dcb627ed6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93293729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cdd50dd7876713d35642aadc4213d530d9c9dd674ab4302227b7c3e7da9eef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31d437241e3bf162ee0841d622c5453ec33b6aa287db252eecef0f1682e1f16`  
		Last Modified: Tue, 09 Sep 2025 03:42:49 GMT  
		Size: 63.5 MB (63458780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ff8b958359c3bc4e16b623284934a8085c7c1c6082817984b533868f9baeee`  
		Last Modified: Tue, 09 Sep 2025 00:58:29 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078ddf87fbf84d8e6d0c3ea29e44e5fd87bc0ecd2fb75ade6322f86ed54e793b`  
		Last Modified: Tue, 09 Sep 2025 00:58:43 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7` - unknown; unknown

```console
$ docker pull varnish@sha256:b41d3da7d84c7778320ded3e186c2ec0c339cffadf5a25ef4ddd387ccbb462b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea04f26282e2ac6c0e836a79bcd449e3754325fbb7431006b3a95bcfde56345`

```dockerfile
```

-	Layers:
	-	`sha256:36ad6c9ceb1fa050b4c785991f70ce29290c961664a691190a82fdc458e5b2fe`  
		Last Modified: Tue, 09 Sep 2025 03:19:41 GMT  
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
$ docker pull varnish@sha256:85580f7b7a622bdb652357242337cd5268be7779356dc04658179d60649b5ebf
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
$ docker pull varnish@sha256:ecc6a26bf15dd703f103a5f51a47e35bc8bdc32152fce86901f0645ebee22758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116170212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bc9ee89ef2eb3f3b72a5035e389aefff37c1fd2d0f26a50c6e663e19d27a7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4586aa2f1c1b6a17a80401224aa72142bd768259b9d0cb08f75bb0e3f6445e`  
		Last Modified: Tue, 09 Sep 2025 00:20:21 GMT  
		Size: 86.4 MB (86394674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98145976a2c73a1ba56b595c657d806188787ae612359fb875362c3e85619d5`  
		Last Modified: Mon, 08 Sep 2025 22:08:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f20fad4ae01fcbd8b56d8e8336fea6b823874389df807e72d2f1029f247e1aa`  
		Last Modified: Mon, 08 Sep 2025 22:08:54 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:d12ed67298e9f3e45c64c672108663a64831ab17e6479ec6af4a4d4cbc5f4f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cb2f383d57d2ffd2eec890733d4474bca757058447546bb2c4cc71419c6bd6`

```dockerfile
```

-	Layers:
	-	`sha256:3ada4edf24301994dc6407707c47aff49de0e01eb65f474e3fa633d5707957c4`  
		Last Modified: Tue, 09 Sep 2025 00:19:55 GMT  
		Size: 19.1 KB (19075 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm variant v7

```console
$ docker pull varnish@sha256:618f6d9cb494fd6937da8de7ad4534e1c9f1d1c45136b951b94e9e4e48b74b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86982465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97302bae394872a4baf7e08c49d59946ea2d72fea4032e9ebd47a7a82161845d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85290fe2f41f38e39ed4ff986fe9781c3552f4deee12aa9639f6acce85c4871d`  
		Last Modified: Tue, 09 Sep 2025 00:20:21 GMT  
		Size: 60.8 MB (60772573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3d0d0d1aab01d38b0aa4a55e366cf394a400100eb197721a3f5c963675b521`  
		Last Modified: Mon, 08 Sep 2025 22:16:33 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd995ccdba4e5572862f1fd445d9fd76721bc0fe723bccacfd2464096df41592`  
		Last Modified: Mon, 08 Sep 2025 22:16:37 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:bf55030d1b5a0959c9b53f308174a69d7f188df2a8954cbcd192548d9464b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a110f3cecf86c21858dc4f899ac790a0d61f1fe988ebe2d8383986efe0f358e2`

```dockerfile
```

-	Layers:
	-	`sha256:98521ba37abbe20c52b1798d59e1df90cc600abf8a5701f51e1d35dcac94a526`  
		Last Modified: Tue, 09 Sep 2025 00:19:58 GMT  
		Size: 19.1 KB (19147 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7948284e2a487e1ae96dfff26bfe4a090ee4c3a8a35e7b8ffd05fc867bdd2819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110351079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86917349ee9ae444e2e913003413cb0344a744a370338b57fc3acff3aa669727`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782650d0bbbe8d92500f05fe23b87bce22da057ddc40d45e626b048911899c29`  
		Last Modified: Tue, 09 Sep 2025 00:20:27 GMT  
		Size: 80.2 MB (80212403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55836a339a291165ac646724e4933ac49427c59f3a797a7544297640540757f`  
		Last Modified: Mon, 08 Sep 2025 22:04:09 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3069acc19e6bfa9ce61086a8f1fffe8dfaceda8ff920ab2bbb4e8a876aacf5`  
		Last Modified: Mon, 08 Sep 2025 22:04:13 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:9ea446c95df7bcce6792d4669ec4e2393201258ea95f1da4a880072a170190dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568dbcc2a4dcddb4affd77e884f1a08e97693debba31a23bc2cc6fb758284b83`

```dockerfile
```

-	Layers:
	-	`sha256:d921c7235d6a3d1f3d789964a0056eee0e57d0b1c8991d65326105c207f43271`  
		Last Modified: Tue, 09 Sep 2025 00:20:01 GMT  
		Size: 19.2 KB (19167 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; 386

```console
$ docker pull varnish@sha256:33eadfafccb65febcc1439cc50697c9d842485db69468a27fd2c4d005ec93b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114332278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d551e50aafac831d1ef8a2eed198885b20b52f6d575ccee3d6ab798956c04880`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329e70a910dca132a58fd19c1a02b5bdd14b5e8a890d9593867a5be55719e9e7`  
		Last Modified: Tue, 09 Sep 2025 00:20:24 GMT  
		Size: 83.0 MB (83040447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e29eeee5ef81c64fdce60973a16f65a9ecf178bdc4e0383a501f72f6e3caa`  
		Last Modified: Mon, 08 Sep 2025 22:08:35 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7374d7d503bfb089f2349b6ab4f697fad9c0e95af91a627c2585f6a30bc5ce20`  
		Last Modified: Mon, 08 Sep 2025 22:08:35 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:cedfcb4ec8a8a88ce63cc771a90eee02b6582f1e230f843df2bb9239fd841343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a69fee7fd4c939c04a90e96a37a2ef49b62ebe691f7e800ac3689a82d9f87f`

```dockerfile
```

-	Layers:
	-	`sha256:2c7e183f9508e1a6351338808f9c408dc01aab08f146db141c117543c8212b42`  
		Last Modified: Tue, 09 Sep 2025 00:20:05 GMT  
		Size: 19.0 KB (19048 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; ppc64le

```console
$ docker pull varnish@sha256:7151e93bb1caf96c2984726f1b03fb4bb4fcddef223eab54cfd375754d92fd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111630730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a334d7aa8d7ed517b1811bfc01b8ec3595717a5498af19c5e6c3b352d87b30c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ddf22107defed9fd4ff0aa86749828b64f1b9385b8224e36dfd85dd24bcf1b`  
		Last Modified: Tue, 09 Sep 2025 03:20:16 GMT  
		Size: 78.0 MB (78034330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d92aacd629706c3a9934ab592c2c2806f5b808459a82537230cf5f27a7d7e0e`  
		Last Modified: Tue, 09 Sep 2025 02:05:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c81a8ce04f06b5cc7eea69fcef084cd62e705dc26bb99a408eb14df1ba422aa`  
		Last Modified: Tue, 09 Sep 2025 02:05:11 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:8a426e3a48660055208e3f2c2548d40f417f67f35fbe4b3b6bf92a392c721b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6baaeb7a0756e1b97989e091504c377486cc10f0cfcd840bb1a736cc280e2a`

```dockerfile
```

-	Layers:
	-	`sha256:ec44d20cfdbee142b2bf941302c00019b334bd8d787e811100c080f058e64d01`  
		Last Modified: Tue, 09 Sep 2025 03:19:47 GMT  
		Size: 19.1 KB (19113 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6` - linux; s390x

```console
$ docker pull varnish@sha256:ec1d315af03f40535061112d0198e8d513f5f629e9b83d84dbd371d190894000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93130361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcff9cdde552eb57d813d405bda8ffca70326d6b2afaf34bf6d1403ecc32e7c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39fb1e4c0b615ba5af0790bacda79c49927c0e7af8f0722976241026c9741cf`  
		Last Modified: Tue, 09 Sep 2025 03:20:13 GMT  
		Size: 63.3 MB (63295411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849d402ae06890fde1aa94ad7910410fe302fef8bf49e251c8de8d39726331bb`  
		Last Modified: Tue, 09 Sep 2025 00:41:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae236667616f5c6a4e3e0b239268e9f95afa0d669b937c23b4fca0aa994e3c8`  
		Last Modified: Tue, 09 Sep 2025 00:41:04 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6` - unknown; unknown

```console
$ docker pull varnish@sha256:5a4db547525dcc23b86ade398358a5b52a095a9a85ca3815745f28510682e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b268ef3d63040ca88dae15ec4288c3f1b138890399a58d61a8618b485e25c5a`

```dockerfile
```

-	Layers:
	-	`sha256:494aeb88a49b2f94e3a3865d3394760387d925a90b78239b18cf46380a5db6c5`  
		Last Modified: Tue, 09 Sep 2025 03:19:50 GMT  
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
$ docker pull varnish@sha256:85580f7b7a622bdb652357242337cd5268be7779356dc04658179d60649b5ebf
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
$ docker pull varnish@sha256:ecc6a26bf15dd703f103a5f51a47e35bc8bdc32152fce86901f0645ebee22758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116170212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bc9ee89ef2eb3f3b72a5035e389aefff37c1fd2d0f26a50c6e663e19d27a7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4586aa2f1c1b6a17a80401224aa72142bd768259b9d0cb08f75bb0e3f6445e`  
		Last Modified: Tue, 09 Sep 2025 00:20:21 GMT  
		Size: 86.4 MB (86394674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98145976a2c73a1ba56b595c657d806188787ae612359fb875362c3e85619d5`  
		Last Modified: Mon, 08 Sep 2025 22:08:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f20fad4ae01fcbd8b56d8e8336fea6b823874389df807e72d2f1029f247e1aa`  
		Last Modified: Mon, 08 Sep 2025 22:08:54 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5` - unknown; unknown

```console
$ docker pull varnish@sha256:d12ed67298e9f3e45c64c672108663a64831ab17e6479ec6af4a4d4cbc5f4f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cb2f383d57d2ffd2eec890733d4474bca757058447546bb2c4cc71419c6bd6`

```dockerfile
```

-	Layers:
	-	`sha256:3ada4edf24301994dc6407707c47aff49de0e01eb65f474e3fa633d5707957c4`  
		Last Modified: Tue, 09 Sep 2025 00:19:55 GMT  
		Size: 19.1 KB (19075 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5` - linux; arm variant v7

```console
$ docker pull varnish@sha256:618f6d9cb494fd6937da8de7ad4534e1c9f1d1c45136b951b94e9e4e48b74b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86982465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97302bae394872a4baf7e08c49d59946ea2d72fea4032e9ebd47a7a82161845d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85290fe2f41f38e39ed4ff986fe9781c3552f4deee12aa9639f6acce85c4871d`  
		Last Modified: Tue, 09 Sep 2025 00:20:21 GMT  
		Size: 60.8 MB (60772573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3d0d0d1aab01d38b0aa4a55e366cf394a400100eb197721a3f5c963675b521`  
		Last Modified: Mon, 08 Sep 2025 22:16:33 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd995ccdba4e5572862f1fd445d9fd76721bc0fe723bccacfd2464096df41592`  
		Last Modified: Mon, 08 Sep 2025 22:16:37 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5` - unknown; unknown

```console
$ docker pull varnish@sha256:bf55030d1b5a0959c9b53f308174a69d7f188df2a8954cbcd192548d9464b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a110f3cecf86c21858dc4f899ac790a0d61f1fe988ebe2d8383986efe0f358e2`

```dockerfile
```

-	Layers:
	-	`sha256:98521ba37abbe20c52b1798d59e1df90cc600abf8a5701f51e1d35dcac94a526`  
		Last Modified: Tue, 09 Sep 2025 00:19:58 GMT  
		Size: 19.1 KB (19147 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7948284e2a487e1ae96dfff26bfe4a090ee4c3a8a35e7b8ffd05fc867bdd2819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110351079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86917349ee9ae444e2e913003413cb0344a744a370338b57fc3acff3aa669727`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782650d0bbbe8d92500f05fe23b87bce22da057ddc40d45e626b048911899c29`  
		Last Modified: Tue, 09 Sep 2025 00:20:27 GMT  
		Size: 80.2 MB (80212403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55836a339a291165ac646724e4933ac49427c59f3a797a7544297640540757f`  
		Last Modified: Mon, 08 Sep 2025 22:04:09 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3069acc19e6bfa9ce61086a8f1fffe8dfaceda8ff920ab2bbb4e8a876aacf5`  
		Last Modified: Mon, 08 Sep 2025 22:04:13 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5` - unknown; unknown

```console
$ docker pull varnish@sha256:9ea446c95df7bcce6792d4669ec4e2393201258ea95f1da4a880072a170190dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568dbcc2a4dcddb4affd77e884f1a08e97693debba31a23bc2cc6fb758284b83`

```dockerfile
```

-	Layers:
	-	`sha256:d921c7235d6a3d1f3d789964a0056eee0e57d0b1c8991d65326105c207f43271`  
		Last Modified: Tue, 09 Sep 2025 00:20:01 GMT  
		Size: 19.2 KB (19167 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5` - linux; 386

```console
$ docker pull varnish@sha256:33eadfafccb65febcc1439cc50697c9d842485db69468a27fd2c4d005ec93b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114332278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d551e50aafac831d1ef8a2eed198885b20b52f6d575ccee3d6ab798956c04880`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329e70a910dca132a58fd19c1a02b5bdd14b5e8a890d9593867a5be55719e9e7`  
		Last Modified: Tue, 09 Sep 2025 00:20:24 GMT  
		Size: 83.0 MB (83040447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e29eeee5ef81c64fdce60973a16f65a9ecf178bdc4e0383a501f72f6e3caa`  
		Last Modified: Mon, 08 Sep 2025 22:08:35 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7374d7d503bfb089f2349b6ab4f697fad9c0e95af91a627c2585f6a30bc5ce20`  
		Last Modified: Mon, 08 Sep 2025 22:08:35 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5` - unknown; unknown

```console
$ docker pull varnish@sha256:cedfcb4ec8a8a88ce63cc771a90eee02b6582f1e230f843df2bb9239fd841343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a69fee7fd4c939c04a90e96a37a2ef49b62ebe691f7e800ac3689a82d9f87f`

```dockerfile
```

-	Layers:
	-	`sha256:2c7e183f9508e1a6351338808f9c408dc01aab08f146db141c117543c8212b42`  
		Last Modified: Tue, 09 Sep 2025 00:20:05 GMT  
		Size: 19.0 KB (19048 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5` - linux; ppc64le

```console
$ docker pull varnish@sha256:7151e93bb1caf96c2984726f1b03fb4bb4fcddef223eab54cfd375754d92fd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111630730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a334d7aa8d7ed517b1811bfc01b8ec3595717a5498af19c5e6c3b352d87b30c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ddf22107defed9fd4ff0aa86749828b64f1b9385b8224e36dfd85dd24bcf1b`  
		Last Modified: Tue, 09 Sep 2025 03:20:16 GMT  
		Size: 78.0 MB (78034330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d92aacd629706c3a9934ab592c2c2806f5b808459a82537230cf5f27a7d7e0e`  
		Last Modified: Tue, 09 Sep 2025 02:05:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c81a8ce04f06b5cc7eea69fcef084cd62e705dc26bb99a408eb14df1ba422aa`  
		Last Modified: Tue, 09 Sep 2025 02:05:11 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5` - unknown; unknown

```console
$ docker pull varnish@sha256:8a426e3a48660055208e3f2c2548d40f417f67f35fbe4b3b6bf92a392c721b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6baaeb7a0756e1b97989e091504c377486cc10f0cfcd840bb1a736cc280e2a`

```dockerfile
```

-	Layers:
	-	`sha256:ec44d20cfdbee142b2bf941302c00019b334bd8d787e811100c080f058e64d01`  
		Last Modified: Tue, 09 Sep 2025 03:19:47 GMT  
		Size: 19.1 KB (19113 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.6.5` - linux; s390x

```console
$ docker pull varnish@sha256:ec1d315af03f40535061112d0198e8d513f5f629e9b83d84dbd371d190894000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93130361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcff9cdde552eb57d813d405bda8ffca70326d6b2afaf34bf6d1403ecc32e7c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39fb1e4c0b615ba5af0790bacda79c49927c0e7af8f0722976241026c9741cf`  
		Last Modified: Tue, 09 Sep 2025 03:20:13 GMT  
		Size: 63.3 MB (63295411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849d402ae06890fde1aa94ad7910410fe302fef8bf49e251c8de8d39726331bb`  
		Last Modified: Tue, 09 Sep 2025 00:41:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae236667616f5c6a4e3e0b239268e9f95afa0d669b937c23b4fca0aa994e3c8`  
		Last Modified: Tue, 09 Sep 2025 00:41:04 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.6.5` - unknown; unknown

```console
$ docker pull varnish@sha256:5a4db547525dcc23b86ade398358a5b52a095a9a85ca3815745f28510682e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b268ef3d63040ca88dae15ec4288c3f1b138890399a58d61a8618b485e25c5a`

```dockerfile
```

-	Layers:
	-	`sha256:494aeb88a49b2f94e3a3865d3394760387d925a90b78239b18cf46380a5db6c5`  
		Last Modified: Tue, 09 Sep 2025 03:19:50 GMT  
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
$ docker pull varnish@sha256:004c5a83a7b96e0fb5d919e5bd6ed6e1753b55193424098053f82930d6a5a41f
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
$ docker pull varnish@sha256:6ea1906f66af6621b5be872303c27e841be3dbfeb25fad920106bcd1584972a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116340831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01e7e6b16318fcf88489ab37bf10ef98f6ab82f29cc546a4e247c7eac136c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18944dae82a25a4881028dd55772eed24b1c8be1950466b6eca61af312c365b5`  
		Last Modified: Tue, 09 Sep 2025 00:19:45 GMT  
		Size: 86.6 MB (86565292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979091d7194e04769585896205808e30477930f91bad468ad1ee0d8bd2f4dc17`  
		Last Modified: Mon, 08 Sep 2025 22:17:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235840fec02341cf6a06d9789cc95025caf43e0fb0546f4d04f761f0a49468a3`  
		Last Modified: Mon, 08 Sep 2025 22:17:46 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:eb4857110035e2485163b912e78d6c7b6571b70179390045e5c98559d6016c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f977ceb09ae86ba9316aefad8d1859df715e250f91df628547048e4e1c07e32a`

```dockerfile
```

-	Layers:
	-	`sha256:4686e767536418e4a698907c2556dd03e0bec42e4c88727a281219cd60411966`  
		Last Modified: Tue, 09 Sep 2025 00:19:42 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d33d114522a19162030ba52c0d519272214d675caebf98a5ad08eb5ab940849a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87147881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae4857cee8b53c7c015034fa7fb713a19d124820b19bb35e190f7e6b96267c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59e639359797c17456c01ec48e4af37d9baf75ee3c0948abe907c4af26067d5`  
		Last Modified: Tue, 09 Sep 2025 00:20:08 GMT  
		Size: 60.9 MB (60937990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180e014771bbced72cbad616ceb8444f6d848941c5d222cf2ca05114acee6bf9`  
		Last Modified: Mon, 08 Sep 2025 22:39:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a8715837fc6167839fb47529731f895e6dc16d9c9611e536684e8b569e33e`  
		Last Modified: Mon, 08 Sep 2025 22:38:58 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:f992b2f49e938ba0f4b0b17151999161f71790a5112c46e2c9cec8015021cf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97486c43c69413bd0cfb916d32fea08f17f534e580c717f1111f51e100a1735f`

```dockerfile
```

-	Layers:
	-	`sha256:8e91e51e2f4a23ccb610579876c56ad109ff00a4659ab6f510d1f08abdf22740`  
		Last Modified: Tue, 09 Sep 2025 00:19:46 GMT  
		Size: 19.7 KB (19748 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:34cd0a30bda20160ff7ae516e04a1c3adef99857d02fdfcaf3ce813c1428842d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110519111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039ab2351cd19844ffc5080315de35144824e0864dfbe6e515900d5f1a66507e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b95db52a59f557a64013c0413ad4c7fdfda02dc7d71dc4ada8359ad435f60aa`  
		Last Modified: Tue, 09 Sep 2025 00:20:13 GMT  
		Size: 80.4 MB (80380435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f1221a4365e75b2f093d2849e49dcd43efab4c3fc25561ade12264e79369bf`  
		Last Modified: Mon, 08 Sep 2025 22:24:18 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac397b371684df07816dd8ccffd8a1d93cd6f2c5551537f329f0b0ab7a40c98`  
		Last Modified: Mon, 08 Sep 2025 22:24:17 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:3fcb990fe9d285b0d6e1511655fd18dd6ada705278900042a7e02128a3d4eb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c980a283bec0356ac4ed751735e36c07ec10c1770c95c332fea24d9fc7ccc81e`

```dockerfile
```

-	Layers:
	-	`sha256:2eef8bd9e2934552fb4337fca4fba8742b2153e1cd79bb4aa0114d701f1ba32d`  
		Last Modified: Tue, 09 Sep 2025 00:19:49 GMT  
		Size: 19.8 KB (19776 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; 386

```console
$ docker pull varnish@sha256:02c9234acad0eb04a624acb34e1a426dbea290ee3784b86c78b474c36781aa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114475602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe1e1d673a9da90136affd095c1aed23ac4ad6dafe10cd762077e5b353f526e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0954a711fdaa9e018a9a6874f258e53d4d982956e83088cd21bdf4838a7c5d81`  
		Last Modified: Tue, 09 Sep 2025 03:11:14 GMT  
		Size: 83.2 MB (83183774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412dfbccb4add8bf8ea9f87514c792eb1cd1ead4780eaa7674e205104cb5d88e`  
		Last Modified: Mon, 08 Sep 2025 22:11:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554eb893a0fae71e2e1992c018c0746b293311942cded5755793b9688ddac647`  
		Last Modified: Mon, 08 Sep 2025 22:11:46 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:79202697d68cbb52332eb571c5f3c6b5807332c4f725188a41005ad0ee7ea8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9f8665dfd530dd16dd6372f423c0935d0a2f57da7ea6e15f046d3126312e61`

```dockerfile
```

-	Layers:
	-	`sha256:1dd9b3af765c1a491122bf4c7a2cfc1509071e35560a190211e441360dbe3124`  
		Last Modified: Tue, 09 Sep 2025 00:19:52 GMT  
		Size: 19.6 KB (19623 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; ppc64le

```console
$ docker pull varnish@sha256:45e721b9ba7357ff98acfdb99721198264110d417fb3e646444cdb0874e0a397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111785987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2d152b59ebf7a541d959405f35f5e76efe5935e5eb69944be6b7975f3d64d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975feffc410074d031a1889b1523855076bb3908dfda525fe57beeb0acaf7a96`  
		Last Modified: Tue, 09 Sep 2025 03:40:24 GMT  
		Size: 78.2 MB (78189591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6c8eafcde7062c2c5d363432172aa9b5849730f606006ac478bfd950f7885a`  
		Last Modified: Tue, 09 Sep 2025 02:07:35 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4361b66c8c004035e5030a72f431c6246e601ff9f86e2db2d21f90427739a9da`  
		Last Modified: Tue, 09 Sep 2025 02:07:39 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:95750c616c60d2cc10939b255833cd544029b2dbe2da4bba06a6c306eb82b4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02143556e0d1a70cab52c94769238b65c2aa3664652ecbc0427221cdd8f2b8f`

```dockerfile
```

-	Layers:
	-	`sha256:8aef501842bf7fdfd1cf343f4ed959a5dcf2e237f59496b8376f4c8f554f8e29`  
		Last Modified: Tue, 09 Sep 2025 03:19:38 GMT  
		Size: 19.7 KB (19710 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7` - linux; s390x

```console
$ docker pull varnish@sha256:0d76e1525b65b81f28d384281945e4e6d194f7e59bcec2d99739f2dcb627ed6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93293729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cdd50dd7876713d35642aadc4213d530d9c9dd674ab4302227b7c3e7da9eef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31d437241e3bf162ee0841d622c5453ec33b6aa287db252eecef0f1682e1f16`  
		Last Modified: Tue, 09 Sep 2025 03:42:49 GMT  
		Size: 63.5 MB (63458780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ff8b958359c3bc4e16b623284934a8085c7c1c6082817984b533868f9baeee`  
		Last Modified: Tue, 09 Sep 2025 00:58:29 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078ddf87fbf84d8e6d0c3ea29e44e5fd87bc0ecd2fb75ade6322f86ed54e793b`  
		Last Modified: Tue, 09 Sep 2025 00:58:43 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7` - unknown; unknown

```console
$ docker pull varnish@sha256:b41d3da7d84c7778320ded3e186c2ec0c339cffadf5a25ef4ddd387ccbb462b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea04f26282e2ac6c0e836a79bcd449e3754325fbb7431006b3a95bcfde56345`

```dockerfile
```

-	Layers:
	-	`sha256:36ad6c9ceb1fa050b4c785991f70ce29290c961664a691190a82fdc458e5b2fe`  
		Last Modified: Tue, 09 Sep 2025 03:19:41 GMT  
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
$ docker pull varnish@sha256:004c5a83a7b96e0fb5d919e5bd6ed6e1753b55193424098053f82930d6a5a41f
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
$ docker pull varnish@sha256:6ea1906f66af6621b5be872303c27e841be3dbfeb25fad920106bcd1584972a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116340831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01e7e6b16318fcf88489ab37bf10ef98f6ab82f29cc546a4e247c7eac136c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18944dae82a25a4881028dd55772eed24b1c8be1950466b6eca61af312c365b5`  
		Last Modified: Tue, 09 Sep 2025 00:19:45 GMT  
		Size: 86.6 MB (86565292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979091d7194e04769585896205808e30477930f91bad468ad1ee0d8bd2f4dc17`  
		Last Modified: Mon, 08 Sep 2025 22:17:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235840fec02341cf6a06d9789cc95025caf43e0fb0546f4d04f761f0a49468a3`  
		Last Modified: Mon, 08 Sep 2025 22:17:46 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:eb4857110035e2485163b912e78d6c7b6571b70179390045e5c98559d6016c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f977ceb09ae86ba9316aefad8d1859df715e250f91df628547048e4e1c07e32a`

```dockerfile
```

-	Layers:
	-	`sha256:4686e767536418e4a698907c2556dd03e0bec42e4c88727a281219cd60411966`  
		Last Modified: Tue, 09 Sep 2025 00:19:42 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d33d114522a19162030ba52c0d519272214d675caebf98a5ad08eb5ab940849a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87147881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae4857cee8b53c7c015034fa7fb713a19d124820b19bb35e190f7e6b96267c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59e639359797c17456c01ec48e4af37d9baf75ee3c0948abe907c4af26067d5`  
		Last Modified: Tue, 09 Sep 2025 00:20:08 GMT  
		Size: 60.9 MB (60937990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180e014771bbced72cbad616ceb8444f6d848941c5d222cf2ca05114acee6bf9`  
		Last Modified: Mon, 08 Sep 2025 22:39:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a8715837fc6167839fb47529731f895e6dc16d9c9611e536684e8b569e33e`  
		Last Modified: Mon, 08 Sep 2025 22:38:58 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:f992b2f49e938ba0f4b0b17151999161f71790a5112c46e2c9cec8015021cf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97486c43c69413bd0cfb916d32fea08f17f534e580c717f1111f51e100a1735f`

```dockerfile
```

-	Layers:
	-	`sha256:8e91e51e2f4a23ccb610579876c56ad109ff00a4659ab6f510d1f08abdf22740`  
		Last Modified: Tue, 09 Sep 2025 00:19:46 GMT  
		Size: 19.7 KB (19748 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:34cd0a30bda20160ff7ae516e04a1c3adef99857d02fdfcaf3ce813c1428842d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110519111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039ab2351cd19844ffc5080315de35144824e0864dfbe6e515900d5f1a66507e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b95db52a59f557a64013c0413ad4c7fdfda02dc7d71dc4ada8359ad435f60aa`  
		Last Modified: Tue, 09 Sep 2025 00:20:13 GMT  
		Size: 80.4 MB (80380435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f1221a4365e75b2f093d2849e49dcd43efab4c3fc25561ade12264e79369bf`  
		Last Modified: Mon, 08 Sep 2025 22:24:18 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac397b371684df07816dd8ccffd8a1d93cd6f2c5551537f329f0b0ab7a40c98`  
		Last Modified: Mon, 08 Sep 2025 22:24:17 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:3fcb990fe9d285b0d6e1511655fd18dd6ada705278900042a7e02128a3d4eb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c980a283bec0356ac4ed751735e36c07ec10c1770c95c332fea24d9fc7ccc81e`

```dockerfile
```

-	Layers:
	-	`sha256:2eef8bd9e2934552fb4337fca4fba8742b2153e1cd79bb4aa0114d701f1ba32d`  
		Last Modified: Tue, 09 Sep 2025 00:19:49 GMT  
		Size: 19.8 KB (19776 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; 386

```console
$ docker pull varnish@sha256:02c9234acad0eb04a624acb34e1a426dbea290ee3784b86c78b474c36781aa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114475602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe1e1d673a9da90136affd095c1aed23ac4ad6dafe10cd762077e5b353f526e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0954a711fdaa9e018a9a6874f258e53d4d982956e83088cd21bdf4838a7c5d81`  
		Last Modified: Tue, 09 Sep 2025 03:11:14 GMT  
		Size: 83.2 MB (83183774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412dfbccb4add8bf8ea9f87514c792eb1cd1ead4780eaa7674e205104cb5d88e`  
		Last Modified: Mon, 08 Sep 2025 22:11:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554eb893a0fae71e2e1992c018c0746b293311942cded5755793b9688ddac647`  
		Last Modified: Mon, 08 Sep 2025 22:11:46 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:79202697d68cbb52332eb571c5f3c6b5807332c4f725188a41005ad0ee7ea8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9f8665dfd530dd16dd6372f423c0935d0a2f57da7ea6e15f046d3126312e61`

```dockerfile
```

-	Layers:
	-	`sha256:1dd9b3af765c1a491122bf4c7a2cfc1509071e35560a190211e441360dbe3124`  
		Last Modified: Tue, 09 Sep 2025 00:19:52 GMT  
		Size: 19.6 KB (19623 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; ppc64le

```console
$ docker pull varnish@sha256:45e721b9ba7357ff98acfdb99721198264110d417fb3e646444cdb0874e0a397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111785987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2d152b59ebf7a541d959405f35f5e76efe5935e5eb69944be6b7975f3d64d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975feffc410074d031a1889b1523855076bb3908dfda525fe57beeb0acaf7a96`  
		Last Modified: Tue, 09 Sep 2025 03:40:24 GMT  
		Size: 78.2 MB (78189591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6c8eafcde7062c2c5d363432172aa9b5849730f606006ac478bfd950f7885a`  
		Last Modified: Tue, 09 Sep 2025 02:07:35 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4361b66c8c004035e5030a72f431c6246e601ff9f86e2db2d21f90427739a9da`  
		Last Modified: Tue, 09 Sep 2025 02:07:39 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:95750c616c60d2cc10939b255833cd544029b2dbe2da4bba06a6c306eb82b4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02143556e0d1a70cab52c94769238b65c2aa3664652ecbc0427221cdd8f2b8f`

```dockerfile
```

-	Layers:
	-	`sha256:8aef501842bf7fdfd1cf343f4ed959a5dcf2e237f59496b8376f4c8f554f8e29`  
		Last Modified: Tue, 09 Sep 2025 03:19:38 GMT  
		Size: 19.7 KB (19710 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7.7.3` - linux; s390x

```console
$ docker pull varnish@sha256:0d76e1525b65b81f28d384281945e4e6d194f7e59bcec2d99739f2dcb627ed6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93293729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cdd50dd7876713d35642aadc4213d530d9c9dd674ab4302227b7c3e7da9eef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31d437241e3bf162ee0841d622c5453ec33b6aa287db252eecef0f1682e1f16`  
		Last Modified: Tue, 09 Sep 2025 03:42:49 GMT  
		Size: 63.5 MB (63458780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ff8b958359c3bc4e16b623284934a8085c7c1c6082817984b533868f9baeee`  
		Last Modified: Tue, 09 Sep 2025 00:58:29 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078ddf87fbf84d8e6d0c3ea29e44e5fd87bc0ecd2fb75ade6322f86ed54e793b`  
		Last Modified: Tue, 09 Sep 2025 00:58:43 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7.7.3` - unknown; unknown

```console
$ docker pull varnish@sha256:b41d3da7d84c7778320ded3e186c2ec0c339cffadf5a25ef4ddd387ccbb462b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea04f26282e2ac6c0e836a79bcd449e3754325fbb7431006b3a95bcfde56345`

```dockerfile
```

-	Layers:
	-	`sha256:36ad6c9ceb1fa050b4c785991f70ce29290c961664a691190a82fdc458e5b2fe`  
		Last Modified: Tue, 09 Sep 2025 03:19:41 GMT  
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
$ docker pull varnish@sha256:004c5a83a7b96e0fb5d919e5bd6ed6e1753b55193424098053f82930d6a5a41f
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
$ docker pull varnish@sha256:6ea1906f66af6621b5be872303c27e841be3dbfeb25fad920106bcd1584972a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116340831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01e7e6b16318fcf88489ab37bf10ef98f6ab82f29cc546a4e247c7eac136c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18944dae82a25a4881028dd55772eed24b1c8be1950466b6eca61af312c365b5`  
		Last Modified: Tue, 09 Sep 2025 00:19:45 GMT  
		Size: 86.6 MB (86565292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979091d7194e04769585896205808e30477930f91bad468ad1ee0d8bd2f4dc17`  
		Last Modified: Mon, 08 Sep 2025 22:17:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235840fec02341cf6a06d9789cc95025caf43e0fb0546f4d04f761f0a49468a3`  
		Last Modified: Mon, 08 Sep 2025 22:17:46 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:eb4857110035e2485163b912e78d6c7b6571b70179390045e5c98559d6016c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f977ceb09ae86ba9316aefad8d1859df715e250f91df628547048e4e1c07e32a`

```dockerfile
```

-	Layers:
	-	`sha256:4686e767536418e4a698907c2556dd03e0bec42e4c88727a281219cd60411966`  
		Last Modified: Tue, 09 Sep 2025 00:19:42 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d33d114522a19162030ba52c0d519272214d675caebf98a5ad08eb5ab940849a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87147881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae4857cee8b53c7c015034fa7fb713a19d124820b19bb35e190f7e6b96267c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59e639359797c17456c01ec48e4af37d9baf75ee3c0948abe907c4af26067d5`  
		Last Modified: Tue, 09 Sep 2025 00:20:08 GMT  
		Size: 60.9 MB (60937990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180e014771bbced72cbad616ceb8444f6d848941c5d222cf2ca05114acee6bf9`  
		Last Modified: Mon, 08 Sep 2025 22:39:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a8715837fc6167839fb47529731f895e6dc16d9c9611e536684e8b569e33e`  
		Last Modified: Mon, 08 Sep 2025 22:38:58 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:f992b2f49e938ba0f4b0b17151999161f71790a5112c46e2c9cec8015021cf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97486c43c69413bd0cfb916d32fea08f17f534e580c717f1111f51e100a1735f`

```dockerfile
```

-	Layers:
	-	`sha256:8e91e51e2f4a23ccb610579876c56ad109ff00a4659ab6f510d1f08abdf22740`  
		Last Modified: Tue, 09 Sep 2025 00:19:46 GMT  
		Size: 19.7 KB (19748 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:34cd0a30bda20160ff7ae516e04a1c3adef99857d02fdfcaf3ce813c1428842d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110519111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039ab2351cd19844ffc5080315de35144824e0864dfbe6e515900d5f1a66507e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b95db52a59f557a64013c0413ad4c7fdfda02dc7d71dc4ada8359ad435f60aa`  
		Last Modified: Tue, 09 Sep 2025 00:20:13 GMT  
		Size: 80.4 MB (80380435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f1221a4365e75b2f093d2849e49dcd43efab4c3fc25561ade12264e79369bf`  
		Last Modified: Mon, 08 Sep 2025 22:24:18 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac397b371684df07816dd8ccffd8a1d93cd6f2c5551537f329f0b0ab7a40c98`  
		Last Modified: Mon, 08 Sep 2025 22:24:17 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:3fcb990fe9d285b0d6e1511655fd18dd6ada705278900042a7e02128a3d4eb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c980a283bec0356ac4ed751735e36c07ec10c1770c95c332fea24d9fc7ccc81e`

```dockerfile
```

-	Layers:
	-	`sha256:2eef8bd9e2934552fb4337fca4fba8742b2153e1cd79bb4aa0114d701f1ba32d`  
		Last Modified: Tue, 09 Sep 2025 00:19:49 GMT  
		Size: 19.8 KB (19776 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:02c9234acad0eb04a624acb34e1a426dbea290ee3784b86c78b474c36781aa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114475602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe1e1d673a9da90136affd095c1aed23ac4ad6dafe10cd762077e5b353f526e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0954a711fdaa9e018a9a6874f258e53d4d982956e83088cd21bdf4838a7c5d81`  
		Last Modified: Tue, 09 Sep 2025 03:11:14 GMT  
		Size: 83.2 MB (83183774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412dfbccb4add8bf8ea9f87514c792eb1cd1ead4780eaa7674e205104cb5d88e`  
		Last Modified: Mon, 08 Sep 2025 22:11:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554eb893a0fae71e2e1992c018c0746b293311942cded5755793b9688ddac647`  
		Last Modified: Mon, 08 Sep 2025 22:11:46 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:79202697d68cbb52332eb571c5f3c6b5807332c4f725188a41005ad0ee7ea8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9f8665dfd530dd16dd6372f423c0935d0a2f57da7ea6e15f046d3126312e61`

```dockerfile
```

-	Layers:
	-	`sha256:1dd9b3af765c1a491122bf4c7a2cfc1509071e35560a190211e441360dbe3124`  
		Last Modified: Tue, 09 Sep 2025 00:19:52 GMT  
		Size: 19.6 KB (19623 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:45e721b9ba7357ff98acfdb99721198264110d417fb3e646444cdb0874e0a397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111785987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2d152b59ebf7a541d959405f35f5e76efe5935e5eb69944be6b7975f3d64d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975feffc410074d031a1889b1523855076bb3908dfda525fe57beeb0acaf7a96`  
		Last Modified: Tue, 09 Sep 2025 03:40:24 GMT  
		Size: 78.2 MB (78189591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6c8eafcde7062c2c5d363432172aa9b5849730f606006ac478bfd950f7885a`  
		Last Modified: Tue, 09 Sep 2025 02:07:35 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4361b66c8c004035e5030a72f431c6246e601ff9f86e2db2d21f90427739a9da`  
		Last Modified: Tue, 09 Sep 2025 02:07:39 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:95750c616c60d2cc10939b255833cd544029b2dbe2da4bba06a6c306eb82b4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02143556e0d1a70cab52c94769238b65c2aa3664652ecbc0427221cdd8f2b8f`

```dockerfile
```

-	Layers:
	-	`sha256:8aef501842bf7fdfd1cf343f4ed959a5dcf2e237f59496b8376f4c8f554f8e29`  
		Last Modified: Tue, 09 Sep 2025 03:19:38 GMT  
		Size: 19.7 KB (19710 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:0d76e1525b65b81f28d384281945e4e6d194f7e59bcec2d99739f2dcb627ed6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93293729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cdd50dd7876713d35642aadc4213d530d9c9dd674ab4302227b7c3e7da9eef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31d437241e3bf162ee0841d622c5453ec33b6aa287db252eecef0f1682e1f16`  
		Last Modified: Tue, 09 Sep 2025 03:42:49 GMT  
		Size: 63.5 MB (63458780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ff8b958359c3bc4e16b623284934a8085c7c1c6082817984b533868f9baeee`  
		Last Modified: Tue, 09 Sep 2025 00:58:29 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078ddf87fbf84d8e6d0c3ea29e44e5fd87bc0ecd2fb75ade6322f86ed54e793b`  
		Last Modified: Tue, 09 Sep 2025 00:58:43 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:b41d3da7d84c7778320ded3e186c2ec0c339cffadf5a25ef4ddd387ccbb462b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea04f26282e2ac6c0e836a79bcd449e3754325fbb7431006b3a95bcfde56345`

```dockerfile
```

-	Layers:
	-	`sha256:36ad6c9ceb1fa050b4c785991f70ce29290c961664a691190a82fdc458e5b2fe`  
		Last Modified: Tue, 09 Sep 2025 03:19:41 GMT  
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
$ docker pull varnish@sha256:004c5a83a7b96e0fb5d919e5bd6ed6e1753b55193424098053f82930d6a5a41f
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
$ docker pull varnish@sha256:6ea1906f66af6621b5be872303c27e841be3dbfeb25fad920106bcd1584972a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116340831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01e7e6b16318fcf88489ab37bf10ef98f6ab82f29cc546a4e247c7eac136c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18944dae82a25a4881028dd55772eed24b1c8be1950466b6eca61af312c365b5`  
		Last Modified: Tue, 09 Sep 2025 00:19:45 GMT  
		Size: 86.6 MB (86565292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979091d7194e04769585896205808e30477930f91bad468ad1ee0d8bd2f4dc17`  
		Last Modified: Mon, 08 Sep 2025 22:17:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235840fec02341cf6a06d9789cc95025caf43e0fb0546f4d04f761f0a49468a3`  
		Last Modified: Mon, 08 Sep 2025 22:17:46 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:eb4857110035e2485163b912e78d6c7b6571b70179390045e5c98559d6016c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f977ceb09ae86ba9316aefad8d1859df715e250f91df628547048e4e1c07e32a`

```dockerfile
```

-	Layers:
	-	`sha256:4686e767536418e4a698907c2556dd03e0bec42e4c88727a281219cd60411966`  
		Last Modified: Tue, 09 Sep 2025 00:19:42 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d33d114522a19162030ba52c0d519272214d675caebf98a5ad08eb5ab940849a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87147881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae4857cee8b53c7c015034fa7fb713a19d124820b19bb35e190f7e6b96267c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59e639359797c17456c01ec48e4af37d9baf75ee3c0948abe907c4af26067d5`  
		Last Modified: Tue, 09 Sep 2025 00:20:08 GMT  
		Size: 60.9 MB (60937990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180e014771bbced72cbad616ceb8444f6d848941c5d222cf2ca05114acee6bf9`  
		Last Modified: Mon, 08 Sep 2025 22:39:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a8715837fc6167839fb47529731f895e6dc16d9c9611e536684e8b569e33e`  
		Last Modified: Mon, 08 Sep 2025 22:38:58 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:f992b2f49e938ba0f4b0b17151999161f71790a5112c46e2c9cec8015021cf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97486c43c69413bd0cfb916d32fea08f17f534e580c717f1111f51e100a1735f`

```dockerfile
```

-	Layers:
	-	`sha256:8e91e51e2f4a23ccb610579876c56ad109ff00a4659ab6f510d1f08abdf22740`  
		Last Modified: Tue, 09 Sep 2025 00:19:46 GMT  
		Size: 19.7 KB (19748 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:34cd0a30bda20160ff7ae516e04a1c3adef99857d02fdfcaf3ce813c1428842d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110519111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039ab2351cd19844ffc5080315de35144824e0864dfbe6e515900d5f1a66507e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b95db52a59f557a64013c0413ad4c7fdfda02dc7d71dc4ada8359ad435f60aa`  
		Last Modified: Tue, 09 Sep 2025 00:20:13 GMT  
		Size: 80.4 MB (80380435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f1221a4365e75b2f093d2849e49dcd43efab4c3fc25561ade12264e79369bf`  
		Last Modified: Mon, 08 Sep 2025 22:24:18 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac397b371684df07816dd8ccffd8a1d93cd6f2c5551537f329f0b0ab7a40c98`  
		Last Modified: Mon, 08 Sep 2025 22:24:17 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:3fcb990fe9d285b0d6e1511655fd18dd6ada705278900042a7e02128a3d4eb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c980a283bec0356ac4ed751735e36c07ec10c1770c95c332fea24d9fc7ccc81e`

```dockerfile
```

-	Layers:
	-	`sha256:2eef8bd9e2934552fb4337fca4fba8742b2153e1cd79bb4aa0114d701f1ba32d`  
		Last Modified: Tue, 09 Sep 2025 00:19:49 GMT  
		Size: 19.8 KB (19776 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:02c9234acad0eb04a624acb34e1a426dbea290ee3784b86c78b474c36781aa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114475602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe1e1d673a9da90136affd095c1aed23ac4ad6dafe10cd762077e5b353f526e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0954a711fdaa9e018a9a6874f258e53d4d982956e83088cd21bdf4838a7c5d81`  
		Last Modified: Tue, 09 Sep 2025 03:11:14 GMT  
		Size: 83.2 MB (83183774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412dfbccb4add8bf8ea9f87514c792eb1cd1ead4780eaa7674e205104cb5d88e`  
		Last Modified: Mon, 08 Sep 2025 22:11:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554eb893a0fae71e2e1992c018c0746b293311942cded5755793b9688ddac647`  
		Last Modified: Mon, 08 Sep 2025 22:11:46 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:79202697d68cbb52332eb571c5f3c6b5807332c4f725188a41005ad0ee7ea8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9f8665dfd530dd16dd6372f423c0935d0a2f57da7ea6e15f046d3126312e61`

```dockerfile
```

-	Layers:
	-	`sha256:1dd9b3af765c1a491122bf4c7a2cfc1509071e35560a190211e441360dbe3124`  
		Last Modified: Tue, 09 Sep 2025 00:19:52 GMT  
		Size: 19.6 KB (19623 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:45e721b9ba7357ff98acfdb99721198264110d417fb3e646444cdb0874e0a397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111785987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2d152b59ebf7a541d959405f35f5e76efe5935e5eb69944be6b7975f3d64d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975feffc410074d031a1889b1523855076bb3908dfda525fe57beeb0acaf7a96`  
		Last Modified: Tue, 09 Sep 2025 03:40:24 GMT  
		Size: 78.2 MB (78189591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6c8eafcde7062c2c5d363432172aa9b5849730f606006ac478bfd950f7885a`  
		Last Modified: Tue, 09 Sep 2025 02:07:35 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4361b66c8c004035e5030a72f431c6246e601ff9f86e2db2d21f90427739a9da`  
		Last Modified: Tue, 09 Sep 2025 02:07:39 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:95750c616c60d2cc10939b255833cd544029b2dbe2da4bba06a6c306eb82b4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02143556e0d1a70cab52c94769238b65c2aa3664652ecbc0427221cdd8f2b8f`

```dockerfile
```

-	Layers:
	-	`sha256:8aef501842bf7fdfd1cf343f4ed959a5dcf2e237f59496b8376f4c8f554f8e29`  
		Last Modified: Tue, 09 Sep 2025 03:19:38 GMT  
		Size: 19.7 KB (19710 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:0d76e1525b65b81f28d384281945e4e6d194f7e59bcec2d99739f2dcb627ed6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93293729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cdd50dd7876713d35642aadc4213d530d9c9dd674ab4302227b7c3e7da9eef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31d437241e3bf162ee0841d622c5453ec33b6aa287db252eecef0f1682e1f16`  
		Last Modified: Tue, 09 Sep 2025 03:42:49 GMT  
		Size: 63.5 MB (63458780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ff8b958359c3bc4e16b623284934a8085c7c1c6082817984b533868f9baeee`  
		Last Modified: Tue, 09 Sep 2025 00:58:29 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078ddf87fbf84d8e6d0c3ea29e44e5fd87bc0ecd2fb75ade6322f86ed54e793b`  
		Last Modified: Tue, 09 Sep 2025 00:58:43 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:b41d3da7d84c7778320ded3e186c2ec0c339cffadf5a25ef4ddd387ccbb462b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea04f26282e2ac6c0e836a79bcd449e3754325fbb7431006b3a95bcfde56345`

```dockerfile
```

-	Layers:
	-	`sha256:36ad6c9ceb1fa050b4c785991f70ce29290c961664a691190a82fdc458e5b2fe`  
		Last Modified: Tue, 09 Sep 2025 03:19:41 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:85580f7b7a622bdb652357242337cd5268be7779356dc04658179d60649b5ebf
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
$ docker pull varnish@sha256:ecc6a26bf15dd703f103a5f51a47e35bc8bdc32152fce86901f0645ebee22758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116170212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7bc9ee89ef2eb3f3b72a5035e389aefff37c1fd2d0f26a50c6e663e19d27a7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4586aa2f1c1b6a17a80401224aa72142bd768259b9d0cb08f75bb0e3f6445e`  
		Last Modified: Tue, 09 Sep 2025 00:20:21 GMT  
		Size: 86.4 MB (86394674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98145976a2c73a1ba56b595c657d806188787ae612359fb875362c3e85619d5`  
		Last Modified: Mon, 08 Sep 2025 22:08:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f20fad4ae01fcbd8b56d8e8336fea6b823874389df807e72d2f1029f247e1aa`  
		Last Modified: Mon, 08 Sep 2025 22:08:54 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:d12ed67298e9f3e45c64c672108663a64831ab17e6479ec6af4a4d4cbc5f4f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cb2f383d57d2ffd2eec890733d4474bca757058447546bb2c4cc71419c6bd6`

```dockerfile
```

-	Layers:
	-	`sha256:3ada4edf24301994dc6407707c47aff49de0e01eb65f474e3fa633d5707957c4`  
		Last Modified: Tue, 09 Sep 2025 00:19:55 GMT  
		Size: 19.1 KB (19075 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:618f6d9cb494fd6937da8de7ad4534e1c9f1d1c45136b951b94e9e4e48b74b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86982465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97302bae394872a4baf7e08c49d59946ea2d72fea4032e9ebd47a7a82161845d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85290fe2f41f38e39ed4ff986fe9781c3552f4deee12aa9639f6acce85c4871d`  
		Last Modified: Tue, 09 Sep 2025 00:20:21 GMT  
		Size: 60.8 MB (60772573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3d0d0d1aab01d38b0aa4a55e366cf394a400100eb197721a3f5c963675b521`  
		Last Modified: Mon, 08 Sep 2025 22:16:33 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd995ccdba4e5572862f1fd445d9fd76721bc0fe723bccacfd2464096df41592`  
		Last Modified: Mon, 08 Sep 2025 22:16:37 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:bf55030d1b5a0959c9b53f308174a69d7f188df2a8954cbcd192548d9464b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a110f3cecf86c21858dc4f899ac790a0d61f1fe988ebe2d8383986efe0f358e2`

```dockerfile
```

-	Layers:
	-	`sha256:98521ba37abbe20c52b1798d59e1df90cc600abf8a5701f51e1d35dcac94a526`  
		Last Modified: Tue, 09 Sep 2025 00:19:58 GMT  
		Size: 19.1 KB (19147 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7948284e2a487e1ae96dfff26bfe4a090ee4c3a8a35e7b8ffd05fc867bdd2819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110351079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86917349ee9ae444e2e913003413cb0344a744a370338b57fc3acff3aa669727`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782650d0bbbe8d92500f05fe23b87bce22da057ddc40d45e626b048911899c29`  
		Last Modified: Tue, 09 Sep 2025 00:20:27 GMT  
		Size: 80.2 MB (80212403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55836a339a291165ac646724e4933ac49427c59f3a797a7544297640540757f`  
		Last Modified: Mon, 08 Sep 2025 22:04:09 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3069acc19e6bfa9ce61086a8f1fffe8dfaceda8ff920ab2bbb4e8a876aacf5`  
		Last Modified: Mon, 08 Sep 2025 22:04:13 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:9ea446c95df7bcce6792d4669ec4e2393201258ea95f1da4a880072a170190dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568dbcc2a4dcddb4affd77e884f1a08e97693debba31a23bc2cc6fb758284b83`

```dockerfile
```

-	Layers:
	-	`sha256:d921c7235d6a3d1f3d789964a0056eee0e57d0b1c8991d65326105c207f43271`  
		Last Modified: Tue, 09 Sep 2025 00:20:01 GMT  
		Size: 19.2 KB (19167 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:33eadfafccb65febcc1439cc50697c9d842485db69468a27fd2c4d005ec93b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114332278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d551e50aafac831d1ef8a2eed198885b20b52f6d575ccee3d6ab798956c04880`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329e70a910dca132a58fd19c1a02b5bdd14b5e8a890d9593867a5be55719e9e7`  
		Last Modified: Tue, 09 Sep 2025 00:20:24 GMT  
		Size: 83.0 MB (83040447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e29eeee5ef81c64fdce60973a16f65a9ecf178bdc4e0383a501f72f6e3caa`  
		Last Modified: Mon, 08 Sep 2025 22:08:35 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7374d7d503bfb089f2349b6ab4f697fad9c0e95af91a627c2585f6a30bc5ce20`  
		Last Modified: Mon, 08 Sep 2025 22:08:35 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:cedfcb4ec8a8a88ce63cc771a90eee02b6582f1e230f843df2bb9239fd841343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a69fee7fd4c939c04a90e96a37a2ef49b62ebe691f7e800ac3689a82d9f87f`

```dockerfile
```

-	Layers:
	-	`sha256:2c7e183f9508e1a6351338808f9c408dc01aab08f146db141c117543c8212b42`  
		Last Modified: Tue, 09 Sep 2025 00:20:05 GMT  
		Size: 19.0 KB (19048 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:7151e93bb1caf96c2984726f1b03fb4bb4fcddef223eab54cfd375754d92fd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111630730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a334d7aa8d7ed517b1811bfc01b8ec3595717a5498af19c5e6c3b352d87b30c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ddf22107defed9fd4ff0aa86749828b64f1b9385b8224e36dfd85dd24bcf1b`  
		Last Modified: Tue, 09 Sep 2025 03:20:16 GMT  
		Size: 78.0 MB (78034330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d92aacd629706c3a9934ab592c2c2806f5b808459a82537230cf5f27a7d7e0e`  
		Last Modified: Tue, 09 Sep 2025 02:05:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c81a8ce04f06b5cc7eea69fcef084cd62e705dc26bb99a408eb14df1ba422aa`  
		Last Modified: Tue, 09 Sep 2025 02:05:11 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:8a426e3a48660055208e3f2c2548d40f417f67f35fbe4b3b6bf92a392c721b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6baaeb7a0756e1b97989e091504c377486cc10f0cfcd840bb1a736cc280e2a`

```dockerfile
```

-	Layers:
	-	`sha256:ec44d20cfdbee142b2bf941302c00019b334bd8d787e811100c080f058e64d01`  
		Last Modified: Tue, 09 Sep 2025 03:19:47 GMT  
		Size: 19.1 KB (19113 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:ec1d315af03f40535061112d0198e8d513f5f629e9b83d84dbd371d190894000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93130361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcff9cdde552eb57d813d405bda8ffca70326d6b2afaf34bf6d1403ecc32e7c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 29 Aug 2025 18:37:31 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39fb1e4c0b615ba5af0790bacda79c49927c0e7af8f0722976241026c9741cf`  
		Last Modified: Tue, 09 Sep 2025 03:20:13 GMT  
		Size: 63.3 MB (63295411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849d402ae06890fde1aa94ad7910410fe302fef8bf49e251c8de8d39726331bb`  
		Last Modified: Tue, 09 Sep 2025 00:41:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae236667616f5c6a4e3e0b239268e9f95afa0d669b937c23b4fca0aa994e3c8`  
		Last Modified: Tue, 09 Sep 2025 00:41:04 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:5a4db547525dcc23b86ade398358a5b52a095a9a85ca3815745f28510682e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b268ef3d63040ca88dae15ec4288c3f1b138890399a58d61a8618b485e25c5a`

```dockerfile
```

-	Layers:
	-	`sha256:494aeb88a49b2f94e3a3865d3394760387d925a90b78239b18cf46380a5db6c5`  
		Last Modified: Tue, 09 Sep 2025 03:19:50 GMT  
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
$ docker pull varnish@sha256:2feff07af34515467b14e78c1f57ba34ea8d14d2ea92b91292423f91959532a7
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
$ docker pull varnish@sha256:be38eacdd90a91c5a2b83b2a514393a1ad145c131d01c978fcb506c8acc6ae19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103549427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d4b38bc14671cce6ee2b38d639ddc782fda68c588e05f77e474ba2f93ef1ea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc34925c959542e1e775e8577e6422eb6bc393fdff50be15cb1ddbbb9a844d93`  
		Last Modified: Mon, 08 Sep 2025 22:08:52 GMT  
		Size: 75.3 MB (75320326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df1cef4f661e5a17ca4bfd74416369abb8265ebac3e8179db0d4872d07ae90d`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:11b9ca6be19340007a7ce7e34f3e60f286a2840267debe45b89fc363223568eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8e43ecc9cd4d5f8175fba6bcf7f3c6028535c28c1862578251f5245121700c`

```dockerfile
```

-	Layers:
	-	`sha256:4c77bdf7c8e959323db56f78f2fa65d1f23c64233329860198f2f4a0b7d8237e`  
		Last Modified: Tue, 09 Sep 2025 00:19:26 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:83d0eb092587fb5442cfdbd0359adf6882ca26c5fa9e5957c2aa9997f7bf8fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75967394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca5d3d8e50e1364c4b1de38f7a093ed938e5b162b5c7c87a5651993f42ca6c7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
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
	-	`sha256:e747f8ef7f1d9a41c99bfb53889f7b8de3504300740a326627fc7522904708cc`  
		Last Modified: Mon, 08 Sep 2025 21:14:21 GMT  
		Size: 23.9 MB (23933904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a96e3e9f59bc14457ad942b973f0d57ab12afaff6dc14cb34cb73d85b3ffd4`  
		Last Modified: Mon, 08 Sep 2025 22:49:28 GMT  
		Size: 52.0 MB (52032733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2319aebd117135eff4658d33b156b6b2a9d49f00ad83a96a75352f08061c664`  
		Last Modified: Mon, 08 Sep 2025 22:39:51 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:761cb4d694b8df422a48c010a217c18afca4cb7b51be9d4573e99562c98d080e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dd6497965803a8eda5b5e176c760ebf0c549a405b5127e071dd297beff09b2`

```dockerfile
```

-	Layers:
	-	`sha256:533d2079eacc98d46a2c79d10c8af512dcc0ffb6699d73c883e1b7b2bd750c9a`  
		Last Modified: Tue, 09 Sep 2025 00:19:29 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f655ffc11d5f56663ecf62d77a29dee3bf6ff8b7976cb0930f0d2ce3ab00dc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98404475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f265a7695386d7aaef5f45ced676dc9eff2437ba9b68bdff89234a60a21f78c8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f3604c9d6c5bd2bd42dfa6de3534592419579a2f1aedf06648c0bbf6a136d`  
		Last Modified: Mon, 08 Sep 2025 22:30:59 GMT  
		Size: 70.3 MB (70301621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c938b01c1fb1304d80a769a0b51cbf645149cade2acd897ecbd53d9b38bb4`  
		Last Modified: Mon, 08 Sep 2025 22:31:01 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:d5dd1f6ee1bc7ea8f5ce60af3bfc1d0c5a9f0a784c00000a9f15b0b4a1c04253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad85a772a21422209b63854c1be2ae1834eb939021eb90a7cb352748f9921c3`

```dockerfile
```

-	Layers:
	-	`sha256:02c53f8649fe16d5c7af504e905da91cbdded3b39efe336dfd31c30eea4ce75a`  
		Last Modified: Tue, 09 Sep 2025 00:19:32 GMT  
		Size: 12.8 KB (12785 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:ad2e165c8b1a90ee344f670b0be2623abf9284e487beea34a9133dbe80e31ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101009277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204fe8fa8253f66756ef05be40e3af7205fb1225057a585991d6f16c1a2e4aaa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
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
	-	`sha256:dc2a09b0db8b98044474925cacc9c009aa76e5883edf644cc36c3f6a2e3917ac`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 29.2 MB (29209634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b78d82146cc6d4082a0d5804c71c506ba351a615197ef8c4e728a4edaf1d0bc`  
		Last Modified: Mon, 08 Sep 2025 22:05:55 GMT  
		Size: 71.8 MB (71798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffa68900cf9a604a0f767d161c84a80879aec6ef88255e9a7131d881ed287eb`  
		Last Modified: Mon, 08 Sep 2025 21:42:45 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:056602f331287da74b46d80369349b7bf1974e24e2bd8c331b76bf59647c2333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd9c1b839b0ad41ac1ea5ecea1c95ea536c024237f209d93e167c7a00779e8e`

```dockerfile
```

-	Layers:
	-	`sha256:f9cb9b18765636d42027eff05bbb548e743b509b2ad28f55f503998ec39d09d0`  
		Last Modified: Tue, 09 Sep 2025 00:19:35 GMT  
		Size: 12.7 KB (12666 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:cda3f84a524ce26496944326d0fa01b70d036a03b5ebd533158d74dc771b5ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105448760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0ebeaf1ed77e48a4d1cb9ebfbec5334b02381b14c832f80f7ae2620a39e90c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
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
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc374f61690bfbde05777b216808ef4ca55da9b385772d1e11c2582cce8eea1`  
		Last Modified: Tue, 09 Sep 2025 03:19:41 GMT  
		Size: 73.4 MB (73379243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fb0210a0c4003e5d22dcdff1d2f4adacc7333b8cc018962cd478e2c4cb4f25`  
		Last Modified: Tue, 09 Sep 2025 02:16:19 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:95b564b7811b2f0940e19273c3edbbcba8d048ad314ab12e20cf69838b5b29e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8848e40fc40a9cbda6e721d532704562057c11768aeb759a7461dc43e80eabd7`

```dockerfile
```

-	Layers:
	-	`sha256:413e97a38d767932bdc61c06dfeca8574b71e5e3e907123b2318bf18298d3ae1`  
		Last Modified: Tue, 09 Sep 2025 03:19:28 GMT  
		Size: 12.7 KB (12731 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:d7297d7a856b26abe2c6cf4dcb68ae223583daf2c3550d3425c41409a1a9d5ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81334954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec54986ee0a82e7a66d2124326e72a1d3f6d107ee409784e0775eb3d87c6d4f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781a8b71ec9183860b5d496ba64d7fcb94baf033b0a47bdf697456121aa97ab8`  
		Last Modified: Tue, 09 Sep 2025 01:20:52 GMT  
		Size: 54.4 MB (54449903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6c5868347cf32752b393fd028c91b374fb426c00125c580c514d6ea595de10`  
		Last Modified: Tue, 09 Sep 2025 00:36:29 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:adf6530b925c2fd277152f73ec3be30ac6d739811028a260c80e3e544d2b559c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54a6010917691e007652e9e563302a407b67631e6e06c5887cb3b1310581cc7`

```dockerfile
```

-	Layers:
	-	`sha256:af860943ec06665363dc0c57d26faf0d3f10690a7dc1610c95f2ba15529d8d6b`  
		Last Modified: Tue, 09 Sep 2025 03:19:31 GMT  
		Size: 12.7 KB (12691 bytes)  
		MIME: application/vnd.in-toto+json
