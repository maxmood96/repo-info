<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `hitch`

-	[`hitch:1`](#hitch1)
-	[`hitch:1.7`](#hitch17)
-	[`hitch:1.7.2`](#hitch172)
-	[`hitch:1.7.2-1`](#hitch172-1)
-	[`hitch:1.7.3`](#hitch173)
-	[`hitch:1.7.3-1`](#hitch173-1)
-	[`hitch:latest`](#hitchlatest)

## `hitch:1`

```console
$ docker pull hitch@sha256:fa0580486f4c43096e8be455e7d7b9a0a2f864743712ebe8e1f7328386daa034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1` - linux; amd64

```console
$ docker pull hitch@sha256:419f3523e4c1aa18f38a201d0a3abbb5a5555878d5ad2fbe618a7ceeaaeffcfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33043381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00cb4ddda70622399602f4f5086191038dccf3a036ae107feeab5bd693f9367`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 06:31:32 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 06:31:32 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 06:31:32 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 06:31:32 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 06:31:32 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 06:33:13 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 06:33:13 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 06:33:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 06:33:14 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 06:33:14 GMT
EXPOSE 443
# Tue, 13 Jun 2023 06:33:14 GMT
CMD []
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d016c1951a5cca083038e61597b3ed71af70966bb902a53921ef9a29a3c5998`  
		Last Modified: Tue, 13 Jun 2023 06:35:25 GMT  
		Size: 1.6 MB (1625556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2dd14f36d5452f6591923222799b0342ee25da997ede0843b4a463bee14807`  
		Last Modified: Tue, 13 Jun 2023 06:35:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7dcf5216bbcb0d54216238183e86410613f3f15819c19cf87914affb3f6d5283
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28124024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ae9584f64bf354ce3d45d0ba8379af23a6dea0ca39e6302fd17a17555bf8d5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:58:47 GMT
ADD file:319a24b7e30fc548f9dcf48ad6cee469e8bf7e89c67901cf3851e41e75693489 in / 
# Mon, 12 Jun 2023 23:58:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 15:39:13 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 15:39:13 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 15:39:14 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 15:39:14 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 15:39:14 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 15:41:51 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 15:41:51 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 15:41:51 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 15:41:51 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 15:41:51 GMT
EXPOSE 443
# Tue, 13 Jun 2023 15:41:51 GMT
CMD []
```

-	Layers:
	-	`sha256:b7c295cb849275e211d18b720d2349cc84c0038be1a362aca4765ceb3342043c`  
		Last Modified: Tue, 13 Jun 2023 00:04:24 GMT  
		Size: 26.6 MB (26578690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef9ab99ce123115cd4cce0a3655ac6ca8a292b8dfa6872e0fea38da14fe620e`  
		Last Modified: Tue, 13 Jun 2023 15:44:07 GMT  
		Size: 1.5 MB (1544918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04f19db1ec6b03f04e6c59d89b59b160773b96679f893300459d6ac1b2ca7f2`  
		Last Modified: Tue, 13 Jun 2023 15:44:07 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:e3613f307701010326082067ce189ad3d72f9380722317d95f2b5c073951cd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31670114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09cc2ab524f50e591ba511062ba2ac517706dda45a14d55ef1be4e84c56b8f6`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:41:42 GMT
ARG SRCVER=1.7.3
# Tue, 04 Jul 2023 03:41:43 GMT
ARG PKGVER=1
# Tue, 04 Jul 2023 03:41:43 GMT
ARG DISTVER=bullseye
# Tue, 04 Jul 2023 03:41:43 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 04 Jul 2023 03:41:43 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 04 Jul 2023 03:44:23 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 04 Jul 2023 03:44:24 GMT
WORKDIR /etc/hitch
# Tue, 04 Jul 2023 03:44:24 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:44:24 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 04 Jul 2023 03:44:24 GMT
EXPOSE 443
# Tue, 04 Jul 2023 03:44:24 GMT
CMD []
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fae7fd952e1974d9c20dd7db77f76c13644d2e2d5b566021a1ad2704669426`  
		Last Modified: Tue, 04 Jul 2023 03:46:20 GMT  
		Size: 1.6 MB (1606742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317f9f83b6bff6290c708c3e88f4559ba9db96e6fa1bf027a8a7f226283f0cf6`  
		Last Modified: Tue, 04 Jul 2023 03:46:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; 386

```console
$ docker pull hitch@sha256:415bf85d24c5dd7af691abae9fec5f189c7f1bb9debb59aa757a7b4cc5c0b3a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34028711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b56ca7b1155c3104700f605b68dd2d4a1e3829a9c3bc53ec66c733fd23428ff`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:39:58 GMT
ADD file:440924fd31c090a7f5e3d36276d17574922eb3e8ececce333fa42f7a95bdd9ce in / 
# Mon, 12 Jun 2023 23:39:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:35:09 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 04:35:09 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 04:35:09 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 04:35:09 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 04:35:09 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 04:38:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 04:38:00 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 04:38:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 04:38:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 04:38:00 GMT
EXPOSE 443
# Tue, 13 Jun 2023 04:38:00 GMT
CMD []
```

-	Layers:
	-	`sha256:1646137eb700afc9e891c03fdf28d3f5bc489ef0200fdacc67beee837d48db7d`  
		Last Modified: Mon, 12 Jun 2023 23:47:07 GMT  
		Size: 32.4 MB (32397388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ea2b26de34ebf1727c697e32fab5ec6fb06d7513ee952876673a1d09a2f35`  
		Last Modified: Tue, 13 Jun 2023 04:40:32 GMT  
		Size: 1.6 MB (1630911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8ab4a5e52cf3d08d7d3812216521fcc846a0e4021691bba308ad4b00b1642b`  
		Last Modified: Tue, 13 Jun 2023 04:40:31 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; ppc64le

```console
$ docker pull hitch@sha256:9dcd19824971abc2c1ff8367fd482d07aa3973baa0a64d37d74a9bd4e27ca1d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36977823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a2db3109f14aac0b99e7e8208777bb243620b08b62abe7fcd3eab79ae0ddd0`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:18:20 GMT
ADD file:b17eabe509462fa1a2e4c5421e877e3e4149085e3da07a421a66c7b06566c457 in / 
# Mon, 12 Jun 2023 23:18:22 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:54:17 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 08:54:17 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 08:54:17 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 08:54:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 08:54:18 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 09:00:22 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 09:00:23 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 09:00:23 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:00:23 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 09:00:24 GMT
EXPOSE 443
# Tue, 13 Jun 2023 09:00:24 GMT
CMD []
```

-	Layers:
	-	`sha256:2973ac0be4a80a6cecbb73370e92810a6f67a98e12e61b3044aa63a322dab03a`  
		Last Modified: Mon, 12 Jun 2023 23:25:03 GMT  
		Size: 35.3 MB (35290790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4806ed9bc9dc262260f2605427bb7f183ed172c594caf80634953e9951025119`  
		Last Modified: Tue, 13 Jun 2023 09:05:29 GMT  
		Size: 1.7 MB (1686616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb6119e7c16c5ca9a3ab58c1fad22902d2fa4f2794aeac797db31b1ea6a979e`  
		Last Modified: Tue, 13 Jun 2023 09:05:29 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; s390x

```console
$ docker pull hitch@sha256:9cdc10c5bb65237df578ff21a756dfa5094be1d46d688090c45f75b4250e1372
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31274777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36e60aa21ef6658407f328ef85c5fcd1b37dfcfc48bc4ac1da470a8c8e0cbca`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Jun 2023 04:30:13 GMT
ADD file:558e8c34e969d458ce6bf4207d9c0fe05d2e67d3457c1d5689666749e82ef2ab in / 
# Tue, 13 Jun 2023 04:30:14 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 20:19:17 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 20:19:18 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 20:19:18 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 20:19:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 20:19:18 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 20:21:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 20:21:00 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 20:21:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 20:21:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 20:21:00 GMT
EXPOSE 443
# Tue, 13 Jun 2023 20:21:00 GMT
CMD []
```

-	Layers:
	-	`sha256:6a752e2308c741009b6f5a88a8ea6764b96ebe7f544197912d8ef9a3ec8c8763`  
		Last Modified: Tue, 13 Jun 2023 04:34:49 GMT  
		Size: 29.7 MB (29652514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afbd1ca22fbf099afdb8d17579f5c7570571aab5bdca30bed559153ed520f3f`  
		Last Modified: Tue, 13 Jun 2023 20:22:51 GMT  
		Size: 1.6 MB (1621848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0a06f08c49bb7be5acafeefbd9375a53d700b2f470f897d89acf8226462b1f`  
		Last Modified: Tue, 13 Jun 2023 20:22:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7`

```console
$ docker pull hitch@sha256:fa0580486f4c43096e8be455e7d7b9a0a2f864743712ebe8e1f7328386daa034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1.7` - linux; amd64

```console
$ docker pull hitch@sha256:419f3523e4c1aa18f38a201d0a3abbb5a5555878d5ad2fbe618a7ceeaaeffcfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33043381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00cb4ddda70622399602f4f5086191038dccf3a036ae107feeab5bd693f9367`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 06:31:32 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 06:31:32 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 06:31:32 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 06:31:32 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 06:31:32 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 06:33:13 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 06:33:13 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 06:33:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 06:33:14 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 06:33:14 GMT
EXPOSE 443
# Tue, 13 Jun 2023 06:33:14 GMT
CMD []
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d016c1951a5cca083038e61597b3ed71af70966bb902a53921ef9a29a3c5998`  
		Last Modified: Tue, 13 Jun 2023 06:35:25 GMT  
		Size: 1.6 MB (1625556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2dd14f36d5452f6591923222799b0342ee25da997ede0843b4a463bee14807`  
		Last Modified: Tue, 13 Jun 2023 06:35:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7dcf5216bbcb0d54216238183e86410613f3f15819c19cf87914affb3f6d5283
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28124024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ae9584f64bf354ce3d45d0ba8379af23a6dea0ca39e6302fd17a17555bf8d5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:58:47 GMT
ADD file:319a24b7e30fc548f9dcf48ad6cee469e8bf7e89c67901cf3851e41e75693489 in / 
# Mon, 12 Jun 2023 23:58:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 15:39:13 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 15:39:13 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 15:39:14 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 15:39:14 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 15:39:14 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 15:41:51 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 15:41:51 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 15:41:51 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 15:41:51 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 15:41:51 GMT
EXPOSE 443
# Tue, 13 Jun 2023 15:41:51 GMT
CMD []
```

-	Layers:
	-	`sha256:b7c295cb849275e211d18b720d2349cc84c0038be1a362aca4765ceb3342043c`  
		Last Modified: Tue, 13 Jun 2023 00:04:24 GMT  
		Size: 26.6 MB (26578690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef9ab99ce123115cd4cce0a3655ac6ca8a292b8dfa6872e0fea38da14fe620e`  
		Last Modified: Tue, 13 Jun 2023 15:44:07 GMT  
		Size: 1.5 MB (1544918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04f19db1ec6b03f04e6c59d89b59b160773b96679f893300459d6ac1b2ca7f2`  
		Last Modified: Tue, 13 Jun 2023 15:44:07 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:e3613f307701010326082067ce189ad3d72f9380722317d95f2b5c073951cd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31670114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09cc2ab524f50e591ba511062ba2ac517706dda45a14d55ef1be4e84c56b8f6`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:41:42 GMT
ARG SRCVER=1.7.3
# Tue, 04 Jul 2023 03:41:43 GMT
ARG PKGVER=1
# Tue, 04 Jul 2023 03:41:43 GMT
ARG DISTVER=bullseye
# Tue, 04 Jul 2023 03:41:43 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 04 Jul 2023 03:41:43 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 04 Jul 2023 03:44:23 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 04 Jul 2023 03:44:24 GMT
WORKDIR /etc/hitch
# Tue, 04 Jul 2023 03:44:24 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:44:24 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 04 Jul 2023 03:44:24 GMT
EXPOSE 443
# Tue, 04 Jul 2023 03:44:24 GMT
CMD []
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fae7fd952e1974d9c20dd7db77f76c13644d2e2d5b566021a1ad2704669426`  
		Last Modified: Tue, 04 Jul 2023 03:46:20 GMT  
		Size: 1.6 MB (1606742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317f9f83b6bff6290c708c3e88f4559ba9db96e6fa1bf027a8a7f226283f0cf6`  
		Last Modified: Tue, 04 Jul 2023 03:46:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; 386

```console
$ docker pull hitch@sha256:415bf85d24c5dd7af691abae9fec5f189c7f1bb9debb59aa757a7b4cc5c0b3a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34028711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b56ca7b1155c3104700f605b68dd2d4a1e3829a9c3bc53ec66c733fd23428ff`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:39:58 GMT
ADD file:440924fd31c090a7f5e3d36276d17574922eb3e8ececce333fa42f7a95bdd9ce in / 
# Mon, 12 Jun 2023 23:39:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:35:09 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 04:35:09 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 04:35:09 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 04:35:09 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 04:35:09 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 04:38:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 04:38:00 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 04:38:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 04:38:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 04:38:00 GMT
EXPOSE 443
# Tue, 13 Jun 2023 04:38:00 GMT
CMD []
```

-	Layers:
	-	`sha256:1646137eb700afc9e891c03fdf28d3f5bc489ef0200fdacc67beee837d48db7d`  
		Last Modified: Mon, 12 Jun 2023 23:47:07 GMT  
		Size: 32.4 MB (32397388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ea2b26de34ebf1727c697e32fab5ec6fb06d7513ee952876673a1d09a2f35`  
		Last Modified: Tue, 13 Jun 2023 04:40:32 GMT  
		Size: 1.6 MB (1630911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8ab4a5e52cf3d08d7d3812216521fcc846a0e4021691bba308ad4b00b1642b`  
		Last Modified: Tue, 13 Jun 2023 04:40:31 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; ppc64le

```console
$ docker pull hitch@sha256:9dcd19824971abc2c1ff8367fd482d07aa3973baa0a64d37d74a9bd4e27ca1d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36977823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a2db3109f14aac0b99e7e8208777bb243620b08b62abe7fcd3eab79ae0ddd0`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:18:20 GMT
ADD file:b17eabe509462fa1a2e4c5421e877e3e4149085e3da07a421a66c7b06566c457 in / 
# Mon, 12 Jun 2023 23:18:22 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:54:17 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 08:54:17 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 08:54:17 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 08:54:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 08:54:18 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 09:00:22 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 09:00:23 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 09:00:23 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:00:23 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 09:00:24 GMT
EXPOSE 443
# Tue, 13 Jun 2023 09:00:24 GMT
CMD []
```

-	Layers:
	-	`sha256:2973ac0be4a80a6cecbb73370e92810a6f67a98e12e61b3044aa63a322dab03a`  
		Last Modified: Mon, 12 Jun 2023 23:25:03 GMT  
		Size: 35.3 MB (35290790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4806ed9bc9dc262260f2605427bb7f183ed172c594caf80634953e9951025119`  
		Last Modified: Tue, 13 Jun 2023 09:05:29 GMT  
		Size: 1.7 MB (1686616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb6119e7c16c5ca9a3ab58c1fad22902d2fa4f2794aeac797db31b1ea6a979e`  
		Last Modified: Tue, 13 Jun 2023 09:05:29 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; s390x

```console
$ docker pull hitch@sha256:9cdc10c5bb65237df578ff21a756dfa5094be1d46d688090c45f75b4250e1372
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31274777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36e60aa21ef6658407f328ef85c5fcd1b37dfcfc48bc4ac1da470a8c8e0cbca`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Jun 2023 04:30:13 GMT
ADD file:558e8c34e969d458ce6bf4207d9c0fe05d2e67d3457c1d5689666749e82ef2ab in / 
# Tue, 13 Jun 2023 04:30:14 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 20:19:17 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 20:19:18 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 20:19:18 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 20:19:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 20:19:18 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 20:21:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 20:21:00 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 20:21:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 20:21:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 20:21:00 GMT
EXPOSE 443
# Tue, 13 Jun 2023 20:21:00 GMT
CMD []
```

-	Layers:
	-	`sha256:6a752e2308c741009b6f5a88a8ea6764b96ebe7f544197912d8ef9a3ec8c8763`  
		Last Modified: Tue, 13 Jun 2023 04:34:49 GMT  
		Size: 29.7 MB (29652514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afbd1ca22fbf099afdb8d17579f5c7570571aab5bdca30bed559153ed520f3f`  
		Last Modified: Tue, 13 Jun 2023 20:22:51 GMT  
		Size: 1.6 MB (1621848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0a06f08c49bb7be5acafeefbd9375a53d700b2f470f897d89acf8226462b1f`  
		Last Modified: Tue, 13 Jun 2023 20:22:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7.2`

```console
$ docker pull hitch@sha256:c63f667b17d34ef23c43479c11d297380c71338dbd5027cd87040308fa0b60ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1.7.2` - linux; amd64

```console
$ docker pull hitch@sha256:b1a3d6d14cfec91219ab9a5259b6cc4b21ba0c616d6c5a0b3d174aec3b6b2640
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33042758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d022f758b9a8770a2d281f815a5eefa8ca8d42ecbe5c251be7dd4255285566`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 06:33:25 GMT
ARG SRCVER=1.7.2
# Tue, 13 Jun 2023 06:33:25 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 06:33:25 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 06:33:25 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 06:33:25 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 13 Jun 2023 06:35:02 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 06:35:02 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 06:35:02 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 06:35:02 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 06:35:02 GMT
EXPOSE 443
# Tue, 13 Jun 2023 06:35:02 GMT
CMD []
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48698c7a3b6b1f2cbb6a3b22b05a68ce7832656bb3d35f7e1e497fa32e862d4`  
		Last Modified: Tue, 13 Jun 2023 06:35:37 GMT  
		Size: 1.6 MB (1624932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b22190c7fbf39830c6742cb698b7fa5bda72025a4f742e2454c5900174f5c9`  
		Last Modified: Tue, 13 Jun 2023 06:35:37 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; arm variant v7

```console
$ docker pull hitch@sha256:4036636ee89eca1a91c9226cdd2594cec1d1bf43e05032631eb09faf57514c33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28122930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674e7851421f353e17cf56d219921b097db0968afe703c9625ffdc72905bd9cd`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:58:47 GMT
ADD file:319a24b7e30fc548f9dcf48ad6cee469e8bf7e89c67901cf3851e41e75693489 in / 
# Mon, 12 Jun 2023 23:58:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 15:42:06 GMT
ARG SRCVER=1.7.2
# Tue, 13 Jun 2023 15:42:06 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 15:42:06 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 15:42:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 15:42:07 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 13 Jun 2023 15:43:49 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 15:43:49 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 15:43:50 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 15:43:50 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 15:43:50 GMT
EXPOSE 443
# Tue, 13 Jun 2023 15:43:50 GMT
CMD []
```

-	Layers:
	-	`sha256:b7c295cb849275e211d18b720d2349cc84c0038be1a362aca4765ceb3342043c`  
		Last Modified: Tue, 13 Jun 2023 00:04:24 GMT  
		Size: 26.6 MB (26578690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406da4525623a409f0f0c479278d9551d3952e54a19da699e0ce65f00f0a20f8`  
		Last Modified: Tue, 13 Jun 2023 15:44:21 GMT  
		Size: 1.5 MB (1543825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b90c45077cb54af55030f9674cd32f0809f47ad777b05f367f66203231f3a3`  
		Last Modified: Tue, 13 Jun 2023 15:44:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:91164400cf15c41b60eee836f4e5419baf6f7e70f8b5a0280d57078e3ad1fec6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31669353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0d6edabab7220328fe991d8a145fbcb2af71d1cb10ccebebf3a66000e3e12a`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:44:35 GMT
ARG SRCVER=1.7.2
# Tue, 04 Jul 2023 03:44:35 GMT
ARG PKGVER=1
# Tue, 04 Jul 2023 03:44:35 GMT
ARG DISTVER=bullseye
# Tue, 04 Jul 2023 03:44:35 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 04 Jul 2023 03:44:35 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 04 Jul 2023 03:46:06 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 04 Jul 2023 03:46:06 GMT
WORKDIR /etc/hitch
# Tue, 04 Jul 2023 03:46:06 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:46:06 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 04 Jul 2023 03:46:06 GMT
EXPOSE 443
# Tue, 04 Jul 2023 03:46:06 GMT
CMD []
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a961bfe8a611b854f65b57e993668c85e90b17b908261e6ba404d80d49bc3d9e`  
		Last Modified: Tue, 04 Jul 2023 03:46:33 GMT  
		Size: 1.6 MB (1605981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a809719f19d4abfa60bc2eb73199d36f3e544f41e8ee17100c93ff6a6274d5b6`  
		Last Modified: Tue, 04 Jul 2023 03:46:33 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; 386

```console
$ docker pull hitch@sha256:8f73a285e08a5f7c3a2ffd15a486f4b4c710a8c5bbcadc05cd7adf93bf3297a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34027384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde40d51e22521a1a96bde5cca0154b4b0b25dfaab7429398f2210f350e98ec9`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:39:58 GMT
ADD file:440924fd31c090a7f5e3d36276d17574922eb3e8ececce333fa42f7a95bdd9ce in / 
# Mon, 12 Jun 2023 23:39:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:38:17 GMT
ARG SRCVER=1.7.2
# Tue, 13 Jun 2023 04:38:17 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 04:38:17 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 04:38:17 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 04:38:17 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 13 Jun 2023 04:40:15 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 04:40:16 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 04:40:16 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 04:40:16 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 04:40:16 GMT
EXPOSE 443
# Tue, 13 Jun 2023 04:40:16 GMT
CMD []
```

-	Layers:
	-	`sha256:1646137eb700afc9e891c03fdf28d3f5bc489ef0200fdacc67beee837d48db7d`  
		Last Modified: Mon, 12 Jun 2023 23:47:07 GMT  
		Size: 32.4 MB (32397388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fbe9bc94f1f8864e8cd193df3d6b97dcdf04f9ad36552a372cff0a8d294d34`  
		Last Modified: Tue, 13 Jun 2023 04:40:45 GMT  
		Size: 1.6 MB (1629582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4684dd49142febee1addbb959b56a0585bbbc1c6bccad74d53d7c537fd142393`  
		Last Modified: Tue, 13 Jun 2023 04:40:44 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; ppc64le

```console
$ docker pull hitch@sha256:adf28c6513aaa8eed2286ead2ec0821baadceb46969de7c1598bcd18cb881243
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36976371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786ed5f3fe1fcdd8f175d9254b34a4625f5635c441aed4ca8376e39c5bdd1334`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:18:20 GMT
ADD file:b17eabe509462fa1a2e4c5421e877e3e4149085e3da07a421a66c7b06566c457 in / 
# Mon, 12 Jun 2023 23:18:22 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 09:00:42 GMT
ARG SRCVER=1.7.2
# Tue, 13 Jun 2023 09:00:42 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 09:00:42 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 09:00:43 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 09:00:43 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 13 Jun 2023 09:05:06 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 09:05:06 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 09:05:07 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:05:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 09:05:07 GMT
EXPOSE 443
# Tue, 13 Jun 2023 09:05:07 GMT
CMD []
```

-	Layers:
	-	`sha256:2973ac0be4a80a6cecbb73370e92810a6f67a98e12e61b3044aa63a322dab03a`  
		Last Modified: Mon, 12 Jun 2023 23:25:03 GMT  
		Size: 35.3 MB (35290790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c196935f5fbd8d51e2e82b7d02ee290a46ac2e6a730144fdf5d98ae709913f`  
		Last Modified: Tue, 13 Jun 2023 09:05:44 GMT  
		Size: 1.7 MB (1685166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b663a94c5b3729878f887d7b8a5d617ad694f54ba35b54030b38d590b5af744c`  
		Last Modified: Tue, 13 Jun 2023 09:05:43 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; s390x

```console
$ docker pull hitch@sha256:7143746e3e152153d82dfdf9c5ba28aca7ed889f37aa2e1d634ecdf4891792ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31274222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8310da6565c35262b51cbd5c7026b6eff2eaba0fdbea92a73535949f97d7bbcc`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Jun 2023 04:30:13 GMT
ADD file:558e8c34e969d458ce6bf4207d9c0fe05d2e67d3457c1d5689666749e82ef2ab in / 
# Tue, 13 Jun 2023 04:30:14 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 20:21:07 GMT
ARG SRCVER=1.7.2
# Tue, 13 Jun 2023 20:21:07 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 20:21:07 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 20:21:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 20:21:07 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 13 Jun 2023 20:22:27 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 20:22:28 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 20:22:28 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 20:22:28 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 20:22:28 GMT
EXPOSE 443
# Tue, 13 Jun 2023 20:22:28 GMT
CMD []
```

-	Layers:
	-	`sha256:6a752e2308c741009b6f5a88a8ea6764b96ebe7f544197912d8ef9a3ec8c8763`  
		Last Modified: Tue, 13 Jun 2023 04:34:49 GMT  
		Size: 29.7 MB (29652514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1140a71f529f3851a1304db19614f28fe43c568346c9784876923c527313ab1`  
		Last Modified: Tue, 13 Jun 2023 20:23:01 GMT  
		Size: 1.6 MB (1621291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36effd60d2d03284f2d91a683ff8be3901edcb774d1c1a81c4e72c751a8e4872`  
		Last Modified: Tue, 13 Jun 2023 20:23:01 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7.2-1`

```console
$ docker pull hitch@sha256:c63f667b17d34ef23c43479c11d297380c71338dbd5027cd87040308fa0b60ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1.7.2-1` - linux; amd64

```console
$ docker pull hitch@sha256:b1a3d6d14cfec91219ab9a5259b6cc4b21ba0c616d6c5a0b3d174aec3b6b2640
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33042758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d022f758b9a8770a2d281f815a5eefa8ca8d42ecbe5c251be7dd4255285566`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 06:33:25 GMT
ARG SRCVER=1.7.2
# Tue, 13 Jun 2023 06:33:25 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 06:33:25 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 06:33:25 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 06:33:25 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 13 Jun 2023 06:35:02 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 06:35:02 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 06:35:02 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 06:35:02 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 06:35:02 GMT
EXPOSE 443
# Tue, 13 Jun 2023 06:35:02 GMT
CMD []
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48698c7a3b6b1f2cbb6a3b22b05a68ce7832656bb3d35f7e1e497fa32e862d4`  
		Last Modified: Tue, 13 Jun 2023 06:35:37 GMT  
		Size: 1.6 MB (1624932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b22190c7fbf39830c6742cb698b7fa5bda72025a4f742e2454c5900174f5c9`  
		Last Modified: Tue, 13 Jun 2023 06:35:37 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:4036636ee89eca1a91c9226cdd2594cec1d1bf43e05032631eb09faf57514c33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28122930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674e7851421f353e17cf56d219921b097db0968afe703c9625ffdc72905bd9cd`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:58:47 GMT
ADD file:319a24b7e30fc548f9dcf48ad6cee469e8bf7e89c67901cf3851e41e75693489 in / 
# Mon, 12 Jun 2023 23:58:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 15:42:06 GMT
ARG SRCVER=1.7.2
# Tue, 13 Jun 2023 15:42:06 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 15:42:06 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 15:42:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 15:42:07 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 13 Jun 2023 15:43:49 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 15:43:49 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 15:43:50 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 15:43:50 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 15:43:50 GMT
EXPOSE 443
# Tue, 13 Jun 2023 15:43:50 GMT
CMD []
```

-	Layers:
	-	`sha256:b7c295cb849275e211d18b720d2349cc84c0038be1a362aca4765ceb3342043c`  
		Last Modified: Tue, 13 Jun 2023 00:04:24 GMT  
		Size: 26.6 MB (26578690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406da4525623a409f0f0c479278d9551d3952e54a19da699e0ce65f00f0a20f8`  
		Last Modified: Tue, 13 Jun 2023 15:44:21 GMT  
		Size: 1.5 MB (1543825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b90c45077cb54af55030f9674cd32f0809f47ad777b05f367f66203231f3a3`  
		Last Modified: Tue, 13 Jun 2023 15:44:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:91164400cf15c41b60eee836f4e5419baf6f7e70f8b5a0280d57078e3ad1fec6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31669353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0d6edabab7220328fe991d8a145fbcb2af71d1cb10ccebebf3a66000e3e12a`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:44:35 GMT
ARG SRCVER=1.7.2
# Tue, 04 Jul 2023 03:44:35 GMT
ARG PKGVER=1
# Tue, 04 Jul 2023 03:44:35 GMT
ARG DISTVER=bullseye
# Tue, 04 Jul 2023 03:44:35 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 04 Jul 2023 03:44:35 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 04 Jul 2023 03:46:06 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 04 Jul 2023 03:46:06 GMT
WORKDIR /etc/hitch
# Tue, 04 Jul 2023 03:46:06 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:46:06 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 04 Jul 2023 03:46:06 GMT
EXPOSE 443
# Tue, 04 Jul 2023 03:46:06 GMT
CMD []
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a961bfe8a611b854f65b57e993668c85e90b17b908261e6ba404d80d49bc3d9e`  
		Last Modified: Tue, 04 Jul 2023 03:46:33 GMT  
		Size: 1.6 MB (1605981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a809719f19d4abfa60bc2eb73199d36f3e544f41e8ee17100c93ff6a6274d5b6`  
		Last Modified: Tue, 04 Jul 2023 03:46:33 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; 386

```console
$ docker pull hitch@sha256:8f73a285e08a5f7c3a2ffd15a486f4b4c710a8c5bbcadc05cd7adf93bf3297a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34027384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde40d51e22521a1a96bde5cca0154b4b0b25dfaab7429398f2210f350e98ec9`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:39:58 GMT
ADD file:440924fd31c090a7f5e3d36276d17574922eb3e8ececce333fa42f7a95bdd9ce in / 
# Mon, 12 Jun 2023 23:39:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:38:17 GMT
ARG SRCVER=1.7.2
# Tue, 13 Jun 2023 04:38:17 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 04:38:17 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 04:38:17 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 04:38:17 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 13 Jun 2023 04:40:15 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 04:40:16 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 04:40:16 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 04:40:16 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 04:40:16 GMT
EXPOSE 443
# Tue, 13 Jun 2023 04:40:16 GMT
CMD []
```

-	Layers:
	-	`sha256:1646137eb700afc9e891c03fdf28d3f5bc489ef0200fdacc67beee837d48db7d`  
		Last Modified: Mon, 12 Jun 2023 23:47:07 GMT  
		Size: 32.4 MB (32397388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fbe9bc94f1f8864e8cd193df3d6b97dcdf04f9ad36552a372cff0a8d294d34`  
		Last Modified: Tue, 13 Jun 2023 04:40:45 GMT  
		Size: 1.6 MB (1629582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4684dd49142febee1addbb959b56a0585bbbc1c6bccad74d53d7c537fd142393`  
		Last Modified: Tue, 13 Jun 2023 04:40:44 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; ppc64le

```console
$ docker pull hitch@sha256:adf28c6513aaa8eed2286ead2ec0821baadceb46969de7c1598bcd18cb881243
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36976371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786ed5f3fe1fcdd8f175d9254b34a4625f5635c441aed4ca8376e39c5bdd1334`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:18:20 GMT
ADD file:b17eabe509462fa1a2e4c5421e877e3e4149085e3da07a421a66c7b06566c457 in / 
# Mon, 12 Jun 2023 23:18:22 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 09:00:42 GMT
ARG SRCVER=1.7.2
# Tue, 13 Jun 2023 09:00:42 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 09:00:42 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 09:00:43 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 09:00:43 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 13 Jun 2023 09:05:06 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 09:05:06 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 09:05:07 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:05:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 09:05:07 GMT
EXPOSE 443
# Tue, 13 Jun 2023 09:05:07 GMT
CMD []
```

-	Layers:
	-	`sha256:2973ac0be4a80a6cecbb73370e92810a6f67a98e12e61b3044aa63a322dab03a`  
		Last Modified: Mon, 12 Jun 2023 23:25:03 GMT  
		Size: 35.3 MB (35290790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c196935f5fbd8d51e2e82b7d02ee290a46ac2e6a730144fdf5d98ae709913f`  
		Last Modified: Tue, 13 Jun 2023 09:05:44 GMT  
		Size: 1.7 MB (1685166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b663a94c5b3729878f887d7b8a5d617ad694f54ba35b54030b38d590b5af744c`  
		Last Modified: Tue, 13 Jun 2023 09:05:43 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; s390x

```console
$ docker pull hitch@sha256:7143746e3e152153d82dfdf9c5ba28aca7ed889f37aa2e1d634ecdf4891792ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31274222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8310da6565c35262b51cbd5c7026b6eff2eaba0fdbea92a73535949f97d7bbcc`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Jun 2023 04:30:13 GMT
ADD file:558e8c34e969d458ce6bf4207d9c0fe05d2e67d3457c1d5689666749e82ef2ab in / 
# Tue, 13 Jun 2023 04:30:14 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 20:21:07 GMT
ARG SRCVER=1.7.2
# Tue, 13 Jun 2023 20:21:07 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 20:21:07 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 20:21:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 20:21:07 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 13 Jun 2023 20:22:27 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 20:22:28 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 20:22:28 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 20:22:28 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 20:22:28 GMT
EXPOSE 443
# Tue, 13 Jun 2023 20:22:28 GMT
CMD []
```

-	Layers:
	-	`sha256:6a752e2308c741009b6f5a88a8ea6764b96ebe7f544197912d8ef9a3ec8c8763`  
		Last Modified: Tue, 13 Jun 2023 04:34:49 GMT  
		Size: 29.7 MB (29652514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1140a71f529f3851a1304db19614f28fe43c568346c9784876923c527313ab1`  
		Last Modified: Tue, 13 Jun 2023 20:23:01 GMT  
		Size: 1.6 MB (1621291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36effd60d2d03284f2d91a683ff8be3901edcb774d1c1a81c4e72c751a8e4872`  
		Last Modified: Tue, 13 Jun 2023 20:23:01 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7.3`

```console
$ docker pull hitch@sha256:fa0580486f4c43096e8be455e7d7b9a0a2f864743712ebe8e1f7328386daa034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1.7.3` - linux; amd64

```console
$ docker pull hitch@sha256:419f3523e4c1aa18f38a201d0a3abbb5a5555878d5ad2fbe618a7ceeaaeffcfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33043381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00cb4ddda70622399602f4f5086191038dccf3a036ae107feeab5bd693f9367`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 06:31:32 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 06:31:32 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 06:31:32 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 06:31:32 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 06:31:32 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 06:33:13 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 06:33:13 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 06:33:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 06:33:14 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 06:33:14 GMT
EXPOSE 443
# Tue, 13 Jun 2023 06:33:14 GMT
CMD []
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d016c1951a5cca083038e61597b3ed71af70966bb902a53921ef9a29a3c5998`  
		Last Modified: Tue, 13 Jun 2023 06:35:25 GMT  
		Size: 1.6 MB (1625556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2dd14f36d5452f6591923222799b0342ee25da997ede0843b4a463bee14807`  
		Last Modified: Tue, 13 Jun 2023 06:35:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7dcf5216bbcb0d54216238183e86410613f3f15819c19cf87914affb3f6d5283
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28124024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ae9584f64bf354ce3d45d0ba8379af23a6dea0ca39e6302fd17a17555bf8d5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:58:47 GMT
ADD file:319a24b7e30fc548f9dcf48ad6cee469e8bf7e89c67901cf3851e41e75693489 in / 
# Mon, 12 Jun 2023 23:58:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 15:39:13 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 15:39:13 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 15:39:14 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 15:39:14 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 15:39:14 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 15:41:51 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 15:41:51 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 15:41:51 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 15:41:51 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 15:41:51 GMT
EXPOSE 443
# Tue, 13 Jun 2023 15:41:51 GMT
CMD []
```

-	Layers:
	-	`sha256:b7c295cb849275e211d18b720d2349cc84c0038be1a362aca4765ceb3342043c`  
		Last Modified: Tue, 13 Jun 2023 00:04:24 GMT  
		Size: 26.6 MB (26578690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef9ab99ce123115cd4cce0a3655ac6ca8a292b8dfa6872e0fea38da14fe620e`  
		Last Modified: Tue, 13 Jun 2023 15:44:07 GMT  
		Size: 1.5 MB (1544918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04f19db1ec6b03f04e6c59d89b59b160773b96679f893300459d6ac1b2ca7f2`  
		Last Modified: Tue, 13 Jun 2023 15:44:07 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:e3613f307701010326082067ce189ad3d72f9380722317d95f2b5c073951cd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31670114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09cc2ab524f50e591ba511062ba2ac517706dda45a14d55ef1be4e84c56b8f6`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:41:42 GMT
ARG SRCVER=1.7.3
# Tue, 04 Jul 2023 03:41:43 GMT
ARG PKGVER=1
# Tue, 04 Jul 2023 03:41:43 GMT
ARG DISTVER=bullseye
# Tue, 04 Jul 2023 03:41:43 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 04 Jul 2023 03:41:43 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 04 Jul 2023 03:44:23 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 04 Jul 2023 03:44:24 GMT
WORKDIR /etc/hitch
# Tue, 04 Jul 2023 03:44:24 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:44:24 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 04 Jul 2023 03:44:24 GMT
EXPOSE 443
# Tue, 04 Jul 2023 03:44:24 GMT
CMD []
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fae7fd952e1974d9c20dd7db77f76c13644d2e2d5b566021a1ad2704669426`  
		Last Modified: Tue, 04 Jul 2023 03:46:20 GMT  
		Size: 1.6 MB (1606742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317f9f83b6bff6290c708c3e88f4559ba9db96e6fa1bf027a8a7f226283f0cf6`  
		Last Modified: Tue, 04 Jul 2023 03:46:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; 386

```console
$ docker pull hitch@sha256:415bf85d24c5dd7af691abae9fec5f189c7f1bb9debb59aa757a7b4cc5c0b3a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34028711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b56ca7b1155c3104700f605b68dd2d4a1e3829a9c3bc53ec66c733fd23428ff`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:39:58 GMT
ADD file:440924fd31c090a7f5e3d36276d17574922eb3e8ececce333fa42f7a95bdd9ce in / 
# Mon, 12 Jun 2023 23:39:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:35:09 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 04:35:09 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 04:35:09 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 04:35:09 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 04:35:09 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 04:38:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 04:38:00 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 04:38:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 04:38:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 04:38:00 GMT
EXPOSE 443
# Tue, 13 Jun 2023 04:38:00 GMT
CMD []
```

-	Layers:
	-	`sha256:1646137eb700afc9e891c03fdf28d3f5bc489ef0200fdacc67beee837d48db7d`  
		Last Modified: Mon, 12 Jun 2023 23:47:07 GMT  
		Size: 32.4 MB (32397388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ea2b26de34ebf1727c697e32fab5ec6fb06d7513ee952876673a1d09a2f35`  
		Last Modified: Tue, 13 Jun 2023 04:40:32 GMT  
		Size: 1.6 MB (1630911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8ab4a5e52cf3d08d7d3812216521fcc846a0e4021691bba308ad4b00b1642b`  
		Last Modified: Tue, 13 Jun 2023 04:40:31 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; ppc64le

```console
$ docker pull hitch@sha256:9dcd19824971abc2c1ff8367fd482d07aa3973baa0a64d37d74a9bd4e27ca1d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36977823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a2db3109f14aac0b99e7e8208777bb243620b08b62abe7fcd3eab79ae0ddd0`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:18:20 GMT
ADD file:b17eabe509462fa1a2e4c5421e877e3e4149085e3da07a421a66c7b06566c457 in / 
# Mon, 12 Jun 2023 23:18:22 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:54:17 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 08:54:17 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 08:54:17 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 08:54:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 08:54:18 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 09:00:22 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 09:00:23 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 09:00:23 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:00:23 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 09:00:24 GMT
EXPOSE 443
# Tue, 13 Jun 2023 09:00:24 GMT
CMD []
```

-	Layers:
	-	`sha256:2973ac0be4a80a6cecbb73370e92810a6f67a98e12e61b3044aa63a322dab03a`  
		Last Modified: Mon, 12 Jun 2023 23:25:03 GMT  
		Size: 35.3 MB (35290790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4806ed9bc9dc262260f2605427bb7f183ed172c594caf80634953e9951025119`  
		Last Modified: Tue, 13 Jun 2023 09:05:29 GMT  
		Size: 1.7 MB (1686616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb6119e7c16c5ca9a3ab58c1fad22902d2fa4f2794aeac797db31b1ea6a979e`  
		Last Modified: Tue, 13 Jun 2023 09:05:29 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; s390x

```console
$ docker pull hitch@sha256:9cdc10c5bb65237df578ff21a756dfa5094be1d46d688090c45f75b4250e1372
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31274777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36e60aa21ef6658407f328ef85c5fcd1b37dfcfc48bc4ac1da470a8c8e0cbca`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Jun 2023 04:30:13 GMT
ADD file:558e8c34e969d458ce6bf4207d9c0fe05d2e67d3457c1d5689666749e82ef2ab in / 
# Tue, 13 Jun 2023 04:30:14 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 20:19:17 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 20:19:18 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 20:19:18 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 20:19:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 20:19:18 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 20:21:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 20:21:00 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 20:21:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 20:21:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 20:21:00 GMT
EXPOSE 443
# Tue, 13 Jun 2023 20:21:00 GMT
CMD []
```

-	Layers:
	-	`sha256:6a752e2308c741009b6f5a88a8ea6764b96ebe7f544197912d8ef9a3ec8c8763`  
		Last Modified: Tue, 13 Jun 2023 04:34:49 GMT  
		Size: 29.7 MB (29652514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afbd1ca22fbf099afdb8d17579f5c7570571aab5bdca30bed559153ed520f3f`  
		Last Modified: Tue, 13 Jun 2023 20:22:51 GMT  
		Size: 1.6 MB (1621848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0a06f08c49bb7be5acafeefbd9375a53d700b2f470f897d89acf8226462b1f`  
		Last Modified: Tue, 13 Jun 2023 20:22:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7.3-1`

```console
$ docker pull hitch@sha256:fa0580486f4c43096e8be455e7d7b9a0a2f864743712ebe8e1f7328386daa034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:1.7.3-1` - linux; amd64

```console
$ docker pull hitch@sha256:419f3523e4c1aa18f38a201d0a3abbb5a5555878d5ad2fbe618a7ceeaaeffcfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33043381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00cb4ddda70622399602f4f5086191038dccf3a036ae107feeab5bd693f9367`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 06:31:32 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 06:31:32 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 06:31:32 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 06:31:32 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 06:31:32 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 06:33:13 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 06:33:13 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 06:33:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 06:33:14 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 06:33:14 GMT
EXPOSE 443
# Tue, 13 Jun 2023 06:33:14 GMT
CMD []
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d016c1951a5cca083038e61597b3ed71af70966bb902a53921ef9a29a3c5998`  
		Last Modified: Tue, 13 Jun 2023 06:35:25 GMT  
		Size: 1.6 MB (1625556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2dd14f36d5452f6591923222799b0342ee25da997ede0843b4a463bee14807`  
		Last Modified: Tue, 13 Jun 2023 06:35:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7dcf5216bbcb0d54216238183e86410613f3f15819c19cf87914affb3f6d5283
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28124024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ae9584f64bf354ce3d45d0ba8379af23a6dea0ca39e6302fd17a17555bf8d5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:58:47 GMT
ADD file:319a24b7e30fc548f9dcf48ad6cee469e8bf7e89c67901cf3851e41e75693489 in / 
# Mon, 12 Jun 2023 23:58:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 15:39:13 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 15:39:13 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 15:39:14 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 15:39:14 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 15:39:14 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 15:41:51 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 15:41:51 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 15:41:51 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 15:41:51 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 15:41:51 GMT
EXPOSE 443
# Tue, 13 Jun 2023 15:41:51 GMT
CMD []
```

-	Layers:
	-	`sha256:b7c295cb849275e211d18b720d2349cc84c0038be1a362aca4765ceb3342043c`  
		Last Modified: Tue, 13 Jun 2023 00:04:24 GMT  
		Size: 26.6 MB (26578690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef9ab99ce123115cd4cce0a3655ac6ca8a292b8dfa6872e0fea38da14fe620e`  
		Last Modified: Tue, 13 Jun 2023 15:44:07 GMT  
		Size: 1.5 MB (1544918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04f19db1ec6b03f04e6c59d89b59b160773b96679f893300459d6ac1b2ca7f2`  
		Last Modified: Tue, 13 Jun 2023 15:44:07 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:e3613f307701010326082067ce189ad3d72f9380722317d95f2b5c073951cd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31670114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09cc2ab524f50e591ba511062ba2ac517706dda45a14d55ef1be4e84c56b8f6`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:41:42 GMT
ARG SRCVER=1.7.3
# Tue, 04 Jul 2023 03:41:43 GMT
ARG PKGVER=1
# Tue, 04 Jul 2023 03:41:43 GMT
ARG DISTVER=bullseye
# Tue, 04 Jul 2023 03:41:43 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 04 Jul 2023 03:41:43 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 04 Jul 2023 03:44:23 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 04 Jul 2023 03:44:24 GMT
WORKDIR /etc/hitch
# Tue, 04 Jul 2023 03:44:24 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:44:24 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 04 Jul 2023 03:44:24 GMT
EXPOSE 443
# Tue, 04 Jul 2023 03:44:24 GMT
CMD []
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fae7fd952e1974d9c20dd7db77f76c13644d2e2d5b566021a1ad2704669426`  
		Last Modified: Tue, 04 Jul 2023 03:46:20 GMT  
		Size: 1.6 MB (1606742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317f9f83b6bff6290c708c3e88f4559ba9db96e6fa1bf027a8a7f226283f0cf6`  
		Last Modified: Tue, 04 Jul 2023 03:46:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; 386

```console
$ docker pull hitch@sha256:415bf85d24c5dd7af691abae9fec5f189c7f1bb9debb59aa757a7b4cc5c0b3a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34028711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b56ca7b1155c3104700f605b68dd2d4a1e3829a9c3bc53ec66c733fd23428ff`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:39:58 GMT
ADD file:440924fd31c090a7f5e3d36276d17574922eb3e8ececce333fa42f7a95bdd9ce in / 
# Mon, 12 Jun 2023 23:39:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:35:09 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 04:35:09 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 04:35:09 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 04:35:09 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 04:35:09 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 04:38:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 04:38:00 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 04:38:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 04:38:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 04:38:00 GMT
EXPOSE 443
# Tue, 13 Jun 2023 04:38:00 GMT
CMD []
```

-	Layers:
	-	`sha256:1646137eb700afc9e891c03fdf28d3f5bc489ef0200fdacc67beee837d48db7d`  
		Last Modified: Mon, 12 Jun 2023 23:47:07 GMT  
		Size: 32.4 MB (32397388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ea2b26de34ebf1727c697e32fab5ec6fb06d7513ee952876673a1d09a2f35`  
		Last Modified: Tue, 13 Jun 2023 04:40:32 GMT  
		Size: 1.6 MB (1630911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8ab4a5e52cf3d08d7d3812216521fcc846a0e4021691bba308ad4b00b1642b`  
		Last Modified: Tue, 13 Jun 2023 04:40:31 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; ppc64le

```console
$ docker pull hitch@sha256:9dcd19824971abc2c1ff8367fd482d07aa3973baa0a64d37d74a9bd4e27ca1d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36977823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a2db3109f14aac0b99e7e8208777bb243620b08b62abe7fcd3eab79ae0ddd0`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:18:20 GMT
ADD file:b17eabe509462fa1a2e4c5421e877e3e4149085e3da07a421a66c7b06566c457 in / 
# Mon, 12 Jun 2023 23:18:22 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:54:17 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 08:54:17 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 08:54:17 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 08:54:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 08:54:18 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 09:00:22 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 09:00:23 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 09:00:23 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:00:23 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 09:00:24 GMT
EXPOSE 443
# Tue, 13 Jun 2023 09:00:24 GMT
CMD []
```

-	Layers:
	-	`sha256:2973ac0be4a80a6cecbb73370e92810a6f67a98e12e61b3044aa63a322dab03a`  
		Last Modified: Mon, 12 Jun 2023 23:25:03 GMT  
		Size: 35.3 MB (35290790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4806ed9bc9dc262260f2605427bb7f183ed172c594caf80634953e9951025119`  
		Last Modified: Tue, 13 Jun 2023 09:05:29 GMT  
		Size: 1.7 MB (1686616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb6119e7c16c5ca9a3ab58c1fad22902d2fa4f2794aeac797db31b1ea6a979e`  
		Last Modified: Tue, 13 Jun 2023 09:05:29 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; s390x

```console
$ docker pull hitch@sha256:9cdc10c5bb65237df578ff21a756dfa5094be1d46d688090c45f75b4250e1372
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31274777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36e60aa21ef6658407f328ef85c5fcd1b37dfcfc48bc4ac1da470a8c8e0cbca`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Jun 2023 04:30:13 GMT
ADD file:558e8c34e969d458ce6bf4207d9c0fe05d2e67d3457c1d5689666749e82ef2ab in / 
# Tue, 13 Jun 2023 04:30:14 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 20:19:17 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 20:19:18 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 20:19:18 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 20:19:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 20:19:18 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 20:21:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 20:21:00 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 20:21:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 20:21:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 20:21:00 GMT
EXPOSE 443
# Tue, 13 Jun 2023 20:21:00 GMT
CMD []
```

-	Layers:
	-	`sha256:6a752e2308c741009b6f5a88a8ea6764b96ebe7f544197912d8ef9a3ec8c8763`  
		Last Modified: Tue, 13 Jun 2023 04:34:49 GMT  
		Size: 29.7 MB (29652514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afbd1ca22fbf099afdb8d17579f5c7570571aab5bdca30bed559153ed520f3f`  
		Last Modified: Tue, 13 Jun 2023 20:22:51 GMT  
		Size: 1.6 MB (1621848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0a06f08c49bb7be5acafeefbd9375a53d700b2f470f897d89acf8226462b1f`  
		Last Modified: Tue, 13 Jun 2023 20:22:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:latest`

```console
$ docker pull hitch@sha256:fa0580486f4c43096e8be455e7d7b9a0a2f864743712ebe8e1f7328386daa034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:latest` - linux; amd64

```console
$ docker pull hitch@sha256:419f3523e4c1aa18f38a201d0a3abbb5a5555878d5ad2fbe618a7ceeaaeffcfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33043381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00cb4ddda70622399602f4f5086191038dccf3a036ae107feeab5bd693f9367`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 06:31:32 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 06:31:32 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 06:31:32 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 06:31:32 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 06:31:32 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 06:33:13 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 06:33:13 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 06:33:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 06:33:14 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 06:33:14 GMT
EXPOSE 443
# Tue, 13 Jun 2023 06:33:14 GMT
CMD []
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d016c1951a5cca083038e61597b3ed71af70966bb902a53921ef9a29a3c5998`  
		Last Modified: Tue, 13 Jun 2023 06:35:25 GMT  
		Size: 1.6 MB (1625556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2dd14f36d5452f6591923222799b0342ee25da997ede0843b4a463bee14807`  
		Last Modified: Tue, 13 Jun 2023 06:35:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7dcf5216bbcb0d54216238183e86410613f3f15819c19cf87914affb3f6d5283
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28124024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ae9584f64bf354ce3d45d0ba8379af23a6dea0ca39e6302fd17a17555bf8d5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:58:47 GMT
ADD file:319a24b7e30fc548f9dcf48ad6cee469e8bf7e89c67901cf3851e41e75693489 in / 
# Mon, 12 Jun 2023 23:58:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 15:39:13 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 15:39:13 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 15:39:14 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 15:39:14 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 15:39:14 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 15:41:51 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 15:41:51 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 15:41:51 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 15:41:51 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 15:41:51 GMT
EXPOSE 443
# Tue, 13 Jun 2023 15:41:51 GMT
CMD []
```

-	Layers:
	-	`sha256:b7c295cb849275e211d18b720d2349cc84c0038be1a362aca4765ceb3342043c`  
		Last Modified: Tue, 13 Jun 2023 00:04:24 GMT  
		Size: 26.6 MB (26578690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef9ab99ce123115cd4cce0a3655ac6ca8a292b8dfa6872e0fea38da14fe620e`  
		Last Modified: Tue, 13 Jun 2023 15:44:07 GMT  
		Size: 1.5 MB (1544918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04f19db1ec6b03f04e6c59d89b59b160773b96679f893300459d6ac1b2ca7f2`  
		Last Modified: Tue, 13 Jun 2023 15:44:07 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:e3613f307701010326082067ce189ad3d72f9380722317d95f2b5c073951cd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31670114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09cc2ab524f50e591ba511062ba2ac517706dda45a14d55ef1be4e84c56b8f6`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:41:42 GMT
ARG SRCVER=1.7.3
# Tue, 04 Jul 2023 03:41:43 GMT
ARG PKGVER=1
# Tue, 04 Jul 2023 03:41:43 GMT
ARG DISTVER=bullseye
# Tue, 04 Jul 2023 03:41:43 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 04 Jul 2023 03:41:43 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 04 Jul 2023 03:44:23 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 04 Jul 2023 03:44:24 GMT
WORKDIR /etc/hitch
# Tue, 04 Jul 2023 03:44:24 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:44:24 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 04 Jul 2023 03:44:24 GMT
EXPOSE 443
# Tue, 04 Jul 2023 03:44:24 GMT
CMD []
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fae7fd952e1974d9c20dd7db77f76c13644d2e2d5b566021a1ad2704669426`  
		Last Modified: Tue, 04 Jul 2023 03:46:20 GMT  
		Size: 1.6 MB (1606742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317f9f83b6bff6290c708c3e88f4559ba9db96e6fa1bf027a8a7f226283f0cf6`  
		Last Modified: Tue, 04 Jul 2023 03:46:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; 386

```console
$ docker pull hitch@sha256:415bf85d24c5dd7af691abae9fec5f189c7f1bb9debb59aa757a7b4cc5c0b3a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34028711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b56ca7b1155c3104700f605b68dd2d4a1e3829a9c3bc53ec66c733fd23428ff`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:39:58 GMT
ADD file:440924fd31c090a7f5e3d36276d17574922eb3e8ececce333fa42f7a95bdd9ce in / 
# Mon, 12 Jun 2023 23:39:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:35:09 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 04:35:09 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 04:35:09 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 04:35:09 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 04:35:09 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 04:38:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 04:38:00 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 04:38:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 04:38:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 04:38:00 GMT
EXPOSE 443
# Tue, 13 Jun 2023 04:38:00 GMT
CMD []
```

-	Layers:
	-	`sha256:1646137eb700afc9e891c03fdf28d3f5bc489ef0200fdacc67beee837d48db7d`  
		Last Modified: Mon, 12 Jun 2023 23:47:07 GMT  
		Size: 32.4 MB (32397388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111ea2b26de34ebf1727c697e32fab5ec6fb06d7513ee952876673a1d09a2f35`  
		Last Modified: Tue, 13 Jun 2023 04:40:32 GMT  
		Size: 1.6 MB (1630911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8ab4a5e52cf3d08d7d3812216521fcc846a0e4021691bba308ad4b00b1642b`  
		Last Modified: Tue, 13 Jun 2023 04:40:31 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; ppc64le

```console
$ docker pull hitch@sha256:9dcd19824971abc2c1ff8367fd482d07aa3973baa0a64d37d74a9bd4e27ca1d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36977823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a2db3109f14aac0b99e7e8208777bb243620b08b62abe7fcd3eab79ae0ddd0`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Mon, 12 Jun 2023 23:18:20 GMT
ADD file:b17eabe509462fa1a2e4c5421e877e3e4149085e3da07a421a66c7b06566c457 in / 
# Mon, 12 Jun 2023 23:18:22 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:54:17 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 08:54:17 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 08:54:17 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 08:54:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 08:54:18 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 09:00:22 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 09:00:23 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 09:00:23 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:00:23 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 09:00:24 GMT
EXPOSE 443
# Tue, 13 Jun 2023 09:00:24 GMT
CMD []
```

-	Layers:
	-	`sha256:2973ac0be4a80a6cecbb73370e92810a6f67a98e12e61b3044aa63a322dab03a`  
		Last Modified: Mon, 12 Jun 2023 23:25:03 GMT  
		Size: 35.3 MB (35290790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4806ed9bc9dc262260f2605427bb7f183ed172c594caf80634953e9951025119`  
		Last Modified: Tue, 13 Jun 2023 09:05:29 GMT  
		Size: 1.7 MB (1686616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb6119e7c16c5ca9a3ab58c1fad22902d2fa4f2794aeac797db31b1ea6a979e`  
		Last Modified: Tue, 13 Jun 2023 09:05:29 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; s390x

```console
$ docker pull hitch@sha256:9cdc10c5bb65237df578ff21a756dfa5094be1d46d688090c45f75b4250e1372
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31274777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36e60aa21ef6658407f328ef85c5fcd1b37dfcfc48bc4ac1da470a8c8e0cbca`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Jun 2023 04:30:13 GMT
ADD file:558e8c34e969d458ce6bf4207d9c0fe05d2e67d3457c1d5689666749e82ef2ab in / 
# Tue, 13 Jun 2023 04:30:14 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 20:19:17 GMT
ARG SRCVER=1.7.3
# Tue, 13 Jun 2023 20:19:18 GMT
ARG PKGVER=1
# Tue, 13 Jun 2023 20:19:18 GMT
ARG DISTVER=bullseye
# Tue, 13 Jun 2023 20:19:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Jun 2023 20:19:18 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 13 Jun 2023 20:21:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Jun 2023 20:21:00 GMT
WORKDIR /etc/hitch
# Tue, 13 Jun 2023 20:21:00 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Jun 2023 20:21:00 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Jun 2023 20:21:00 GMT
EXPOSE 443
# Tue, 13 Jun 2023 20:21:00 GMT
CMD []
```

-	Layers:
	-	`sha256:6a752e2308c741009b6f5a88a8ea6764b96ebe7f544197912d8ef9a3ec8c8763`  
		Last Modified: Tue, 13 Jun 2023 04:34:49 GMT  
		Size: 29.7 MB (29652514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afbd1ca22fbf099afdb8d17579f5c7570571aab5bdca30bed559153ed520f3f`  
		Last Modified: Tue, 13 Jun 2023 20:22:51 GMT  
		Size: 1.6 MB (1621848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0a06f08c49bb7be5acafeefbd9375a53d700b2f470f897d89acf8226462b1f`  
		Last Modified: Tue, 13 Jun 2023 20:22:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
