<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `hitch`

-	[`hitch:1`](#hitch1)
-	[`hitch:1.8`](#hitch18)
-	[`hitch:1.8.0`](#hitch180)
-	[`hitch:1.8.0-1`](#hitch180-1)
-	[`hitch:latest`](#hitchlatest)

## `hitch:1`

```console
$ docker pull hitch@sha256:3d6c9c81c3c0000514f0329e09a2ccd78d02830958f649b0df409521b76c7234
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hitch:1` - linux; amd64

```console
$ docker pull hitch@sha256:d8cdbbb65fd280e0a179e479b53f8a9bc09fb5f47fcb54486ca25d34d4433727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32250164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b111ec9be9d13c03e7481e1ac42fb7f831836f6a74dac81a39cf4d0c7d499f4e`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:38:30 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:38:30 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:38:30 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:38:30 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:38:30 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:38:30 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:38:31 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:38:31 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:38:31 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:38:31 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:38:31 GMT
CMD []
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4948d1c638f9e53a7907ed5cc86e6ea390c97f7ca87f0eff02c5ca74400364f1`  
		Last Modified: Mon, 08 Dec 2025 22:38:42 GMT  
		Size: 4.0 MB (4021302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1607c536ced231ececdaf8bea9cc360b67ed066ebe3320112b312db1c0f0051e`  
		Last Modified: Mon, 08 Dec 2025 22:38:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:50a6d2d5e692f5b853ffd4b81d82a8ab308ef83a4ed5f14989b48c144451c55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2544927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf7a07ab0231a85c30b953c694b73d5eaaa3493536ecbe70158357569c7869e`

```dockerfile
```

-	Layers:
	-	`sha256:21b205514099547dbcc1fbdfcb76a4a929c3812cb0fa92df4695970c41d3401b`  
		Last Modified: Tue, 09 Dec 2025 01:46:55 GMT  
		Size: 2.5 MB (2531345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff9d5cde017c428fa4c55dceae78d8464babb564c2ad342500c17d8e6b2be46`  
		Last Modified: Tue, 09 Dec 2025 01:46:55 GMT  
		Size: 13.6 KB (13582 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7fa72fc14e86cdae66d0f5308109a0fc91e72219af1da87900c3c7f265404df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27319297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0fba3ab800c9f6851d460d228002f3492d8a2dbaee3d0af2f67d1169417f3b`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:36:36 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:36:36 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:36:36 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:36:36 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:36:36 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:36:36 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:36:36 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:36:36 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:36 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:36:36 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:36:36 GMT
CMD []
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e12d05562656f2ada4a6c1a89e279d71ae7d4607341c4fd6ed3872a3a165f2`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 3.4 MB (3384831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe81099c0ae18944a3828de6408d45e95ca967b18f95d4edcebb9265d04ccb0`  
		Last Modified: Mon, 08 Dec 2025 22:36:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:033a5f91c9acbce1b5c80de845f633049dad17b96003148783e8e1fe7b0d4f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2547245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f70caa6fb9a5550c239a8d1e3d9d352b6fc3bce599d9c7f27011e7195ce46`

```dockerfile
```

-	Layers:
	-	`sha256:600e7dca7e4a224abdd71f7b55bfd2d32bb002bfb0711d352061914e9d1615ff`  
		Last Modified: Tue, 09 Dec 2025 01:46:59 GMT  
		Size: 2.5 MB (2533577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe0d13cbf4054021a7b33839da223983ac75c99a8ec422c14fa48022c4f3a3b`  
		Last Modified: Tue, 09 Dec 2025 01:47:00 GMT  
		Size: 13.7 KB (13668 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:1dc00ac4dc445a0dca2dcbbf2c1e448340542cabe97861e238264ba4429846be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31974362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e53ad05e8a2a3533254dfabd07450dd9d5d9b413df3d05c7251de4d069d0111`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:33:25 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:33:25 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:33:25 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:33:25 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:33:25 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:33:25 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:33:25 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:33:25 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:25 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:33:25 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:33:25 GMT
CMD []
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7669bcb0960a42101f23697817bdb33540df27a24a66e9747affd47c401057`  
		Last Modified: Mon, 08 Dec 2025 22:33:38 GMT  
		Size: 3.9 MB (3871688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4f6720f4c1ae0c1d00a2529f2a9b5961420036342041a664ceb2aa792c7d7f`  
		Last Modified: Mon, 08 Dec 2025 22:33:38 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:ea28eb37a0f2ed39da63abb42419b2e45ceac2f87d77ac6dcfc79bbade9e92e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e8534a0fbf39350ff049ce1770f6eab3cf5159887c6a866ced97dd6944c5bb`

```dockerfile
```

-	Layers:
	-	`sha256:39efa46ca8d3aabc01e59cffdde2081707946d7f27da767cc1b4a32e5ae80eb3`  
		Last Modified: Tue, 09 Dec 2025 01:47:04 GMT  
		Size: 2.5 MB (2531615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad19fc3d9734e347986795b4059b0eb73c138ba6a8e2775958d213a09373a97e`  
		Last Modified: Tue, 09 Dec 2025 01:47:05 GMT  
		Size: 13.7 KB (13698 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; 386

```console
$ docker pull hitch@sha256:ac5056d4ffcb6d5676e63ee43fb455e7bec8335336f9d46fcf21eb55e6cd7b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33226136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7f5e7fe75cfc8cde9e9dff12afa783993fc90191536207b3f6879d2dfe9892`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:36:11 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:36:11 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:36:11 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:36:11 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:36:11 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:36:11 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:36:11 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:36:11 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:11 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:36:11 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a077194ed7ec145f4f6772fbfbd563b41be1d1ea7524e0041a266f4cc1a711`  
		Last Modified: Mon, 08 Dec 2025 22:36:24 GMT  
		Size: 4.0 MB (4015962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5732e83715eb2e1b8bfa444dcc10e458d52a7341f955f7769649a2d480d134`  
		Last Modified: Mon, 08 Dec 2025 22:36:23 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:49277a97a2518d3a564cc3febf0fbd174072605a3eddd98dba1631ccf64aff09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6009a480cb12adb3b8f47931596924d42fcbe66ff669fcf1d7b4e2067c2f0393`

```dockerfile
```

-	Layers:
	-	`sha256:2d10de457e78b892961f31ea28bc8d20f57515f7397c7bb8b9b1e4b0ef7b9a81`  
		Last Modified: Tue, 09 Dec 2025 01:47:08 GMT  
		Size: 2.5 MB (2528521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7070cee358ef4a7a2b0b88274c5d1dd8fe63aa2072b154decfe397e5ba2cfaab`  
		Last Modified: Tue, 09 Dec 2025 01:47:09 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:1.8`

```console
$ docker pull hitch@sha256:3d6c9c81c3c0000514f0329e09a2ccd78d02830958f649b0df409521b76c7234
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hitch:1.8` - linux; amd64

```console
$ docker pull hitch@sha256:d8cdbbb65fd280e0a179e479b53f8a9bc09fb5f47fcb54486ca25d34d4433727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32250164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b111ec9be9d13c03e7481e1ac42fb7f831836f6a74dac81a39cf4d0c7d499f4e`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:38:30 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:38:30 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:38:30 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:38:30 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:38:30 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:38:30 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:38:31 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:38:31 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:38:31 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:38:31 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:38:31 GMT
CMD []
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4948d1c638f9e53a7907ed5cc86e6ea390c97f7ca87f0eff02c5ca74400364f1`  
		Last Modified: Mon, 08 Dec 2025 22:38:42 GMT  
		Size: 4.0 MB (4021302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1607c536ced231ececdaf8bea9cc360b67ed066ebe3320112b312db1c0f0051e`  
		Last Modified: Mon, 08 Dec 2025 22:38:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:50a6d2d5e692f5b853ffd4b81d82a8ab308ef83a4ed5f14989b48c144451c55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2544927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf7a07ab0231a85c30b953c694b73d5eaaa3493536ecbe70158357569c7869e`

```dockerfile
```

-	Layers:
	-	`sha256:21b205514099547dbcc1fbdfcb76a4a929c3812cb0fa92df4695970c41d3401b`  
		Last Modified: Tue, 09 Dec 2025 01:46:55 GMT  
		Size: 2.5 MB (2531345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff9d5cde017c428fa4c55dceae78d8464babb564c2ad342500c17d8e6b2be46`  
		Last Modified: Tue, 09 Dec 2025 01:46:55 GMT  
		Size: 13.6 KB (13582 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7fa72fc14e86cdae66d0f5308109a0fc91e72219af1da87900c3c7f265404df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27319297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0fba3ab800c9f6851d460d228002f3492d8a2dbaee3d0af2f67d1169417f3b`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:36:36 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:36:36 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:36:36 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:36:36 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:36:36 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:36:36 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:36:36 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:36:36 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:36 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:36:36 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:36:36 GMT
CMD []
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e12d05562656f2ada4a6c1a89e279d71ae7d4607341c4fd6ed3872a3a165f2`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 3.4 MB (3384831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe81099c0ae18944a3828de6408d45e95ca967b18f95d4edcebb9265d04ccb0`  
		Last Modified: Mon, 08 Dec 2025 22:36:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:033a5f91c9acbce1b5c80de845f633049dad17b96003148783e8e1fe7b0d4f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2547245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f70caa6fb9a5550c239a8d1e3d9d352b6fc3bce599d9c7f27011e7195ce46`

```dockerfile
```

-	Layers:
	-	`sha256:600e7dca7e4a224abdd71f7b55bfd2d32bb002bfb0711d352061914e9d1615ff`  
		Last Modified: Tue, 09 Dec 2025 01:46:59 GMT  
		Size: 2.5 MB (2533577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe0d13cbf4054021a7b33839da223983ac75c99a8ec422c14fa48022c4f3a3b`  
		Last Modified: Tue, 09 Dec 2025 01:47:00 GMT  
		Size: 13.7 KB (13668 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:1dc00ac4dc445a0dca2dcbbf2c1e448340542cabe97861e238264ba4429846be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31974362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e53ad05e8a2a3533254dfabd07450dd9d5d9b413df3d05c7251de4d069d0111`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:33:25 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:33:25 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:33:25 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:33:25 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:33:25 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:33:25 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:33:25 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:33:25 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:25 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:33:25 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:33:25 GMT
CMD []
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7669bcb0960a42101f23697817bdb33540df27a24a66e9747affd47c401057`  
		Last Modified: Mon, 08 Dec 2025 22:33:38 GMT  
		Size: 3.9 MB (3871688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4f6720f4c1ae0c1d00a2529f2a9b5961420036342041a664ceb2aa792c7d7f`  
		Last Modified: Mon, 08 Dec 2025 22:33:38 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:ea28eb37a0f2ed39da63abb42419b2e45ceac2f87d77ac6dcfc79bbade9e92e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e8534a0fbf39350ff049ce1770f6eab3cf5159887c6a866ced97dd6944c5bb`

```dockerfile
```

-	Layers:
	-	`sha256:39efa46ca8d3aabc01e59cffdde2081707946d7f27da767cc1b4a32e5ae80eb3`  
		Last Modified: Tue, 09 Dec 2025 01:47:04 GMT  
		Size: 2.5 MB (2531615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad19fc3d9734e347986795b4059b0eb73c138ba6a8e2775958d213a09373a97e`  
		Last Modified: Tue, 09 Dec 2025 01:47:05 GMT  
		Size: 13.7 KB (13698 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; 386

```console
$ docker pull hitch@sha256:ac5056d4ffcb6d5676e63ee43fb455e7bec8335336f9d46fcf21eb55e6cd7b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33226136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7f5e7fe75cfc8cde9e9dff12afa783993fc90191536207b3f6879d2dfe9892`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:36:11 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:36:11 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:36:11 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:36:11 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:36:11 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:36:11 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:36:11 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:36:11 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:11 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:36:11 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a077194ed7ec145f4f6772fbfbd563b41be1d1ea7524e0041a266f4cc1a711`  
		Last Modified: Mon, 08 Dec 2025 22:36:24 GMT  
		Size: 4.0 MB (4015962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5732e83715eb2e1b8bfa444dcc10e458d52a7341f955f7769649a2d480d134`  
		Last Modified: Mon, 08 Dec 2025 22:36:23 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:49277a97a2518d3a564cc3febf0fbd174072605a3eddd98dba1631ccf64aff09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6009a480cb12adb3b8f47931596924d42fcbe66ff669fcf1d7b4e2067c2f0393`

```dockerfile
```

-	Layers:
	-	`sha256:2d10de457e78b892961f31ea28bc8d20f57515f7397c7bb8b9b1e4b0ef7b9a81`  
		Last Modified: Tue, 09 Dec 2025 01:47:08 GMT  
		Size: 2.5 MB (2528521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7070cee358ef4a7a2b0b88274c5d1dd8fe63aa2072b154decfe397e5ba2cfaab`  
		Last Modified: Tue, 09 Dec 2025 01:47:09 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:1.8.0`

```console
$ docker pull hitch@sha256:3d6c9c81c3c0000514f0329e09a2ccd78d02830958f649b0df409521b76c7234
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hitch:1.8.0` - linux; amd64

```console
$ docker pull hitch@sha256:d8cdbbb65fd280e0a179e479b53f8a9bc09fb5f47fcb54486ca25d34d4433727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32250164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b111ec9be9d13c03e7481e1ac42fb7f831836f6a74dac81a39cf4d0c7d499f4e`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:38:30 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:38:30 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:38:30 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:38:30 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:38:30 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:38:30 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:38:31 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:38:31 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:38:31 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:38:31 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:38:31 GMT
CMD []
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4948d1c638f9e53a7907ed5cc86e6ea390c97f7ca87f0eff02c5ca74400364f1`  
		Last Modified: Mon, 08 Dec 2025 22:38:42 GMT  
		Size: 4.0 MB (4021302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1607c536ced231ececdaf8bea9cc360b67ed066ebe3320112b312db1c0f0051e`  
		Last Modified: Mon, 08 Dec 2025 22:38:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:50a6d2d5e692f5b853ffd4b81d82a8ab308ef83a4ed5f14989b48c144451c55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2544927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf7a07ab0231a85c30b953c694b73d5eaaa3493536ecbe70158357569c7869e`

```dockerfile
```

-	Layers:
	-	`sha256:21b205514099547dbcc1fbdfcb76a4a929c3812cb0fa92df4695970c41d3401b`  
		Last Modified: Tue, 09 Dec 2025 01:46:55 GMT  
		Size: 2.5 MB (2531345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff9d5cde017c428fa4c55dceae78d8464babb564c2ad342500c17d8e6b2be46`  
		Last Modified: Tue, 09 Dec 2025 01:46:55 GMT  
		Size: 13.6 KB (13582 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7fa72fc14e86cdae66d0f5308109a0fc91e72219af1da87900c3c7f265404df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27319297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0fba3ab800c9f6851d460d228002f3492d8a2dbaee3d0af2f67d1169417f3b`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:36:36 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:36:36 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:36:36 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:36:36 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:36:36 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:36:36 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:36:36 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:36:36 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:36 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:36:36 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:36:36 GMT
CMD []
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e12d05562656f2ada4a6c1a89e279d71ae7d4607341c4fd6ed3872a3a165f2`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 3.4 MB (3384831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe81099c0ae18944a3828de6408d45e95ca967b18f95d4edcebb9265d04ccb0`  
		Last Modified: Mon, 08 Dec 2025 22:36:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:033a5f91c9acbce1b5c80de845f633049dad17b96003148783e8e1fe7b0d4f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2547245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f70caa6fb9a5550c239a8d1e3d9d352b6fc3bce599d9c7f27011e7195ce46`

```dockerfile
```

-	Layers:
	-	`sha256:600e7dca7e4a224abdd71f7b55bfd2d32bb002bfb0711d352061914e9d1615ff`  
		Last Modified: Tue, 09 Dec 2025 01:46:59 GMT  
		Size: 2.5 MB (2533577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe0d13cbf4054021a7b33839da223983ac75c99a8ec422c14fa48022c4f3a3b`  
		Last Modified: Tue, 09 Dec 2025 01:47:00 GMT  
		Size: 13.7 KB (13668 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:1dc00ac4dc445a0dca2dcbbf2c1e448340542cabe97861e238264ba4429846be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31974362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e53ad05e8a2a3533254dfabd07450dd9d5d9b413df3d05c7251de4d069d0111`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:33:25 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:33:25 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:33:25 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:33:25 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:33:25 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:33:25 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:33:25 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:33:25 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:25 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:33:25 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:33:25 GMT
CMD []
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7669bcb0960a42101f23697817bdb33540df27a24a66e9747affd47c401057`  
		Last Modified: Mon, 08 Dec 2025 22:33:38 GMT  
		Size: 3.9 MB (3871688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4f6720f4c1ae0c1d00a2529f2a9b5961420036342041a664ceb2aa792c7d7f`  
		Last Modified: Mon, 08 Dec 2025 22:33:38 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:ea28eb37a0f2ed39da63abb42419b2e45ceac2f87d77ac6dcfc79bbade9e92e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e8534a0fbf39350ff049ce1770f6eab3cf5159887c6a866ced97dd6944c5bb`

```dockerfile
```

-	Layers:
	-	`sha256:39efa46ca8d3aabc01e59cffdde2081707946d7f27da767cc1b4a32e5ae80eb3`  
		Last Modified: Tue, 09 Dec 2025 01:47:04 GMT  
		Size: 2.5 MB (2531615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad19fc3d9734e347986795b4059b0eb73c138ba6a8e2775958d213a09373a97e`  
		Last Modified: Tue, 09 Dec 2025 01:47:05 GMT  
		Size: 13.7 KB (13698 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; 386

```console
$ docker pull hitch@sha256:ac5056d4ffcb6d5676e63ee43fb455e7bec8335336f9d46fcf21eb55e6cd7b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33226136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7f5e7fe75cfc8cde9e9dff12afa783993fc90191536207b3f6879d2dfe9892`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:36:11 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:36:11 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:36:11 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:36:11 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:36:11 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:36:11 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:36:11 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:36:11 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:11 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:36:11 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a077194ed7ec145f4f6772fbfbd563b41be1d1ea7524e0041a266f4cc1a711`  
		Last Modified: Mon, 08 Dec 2025 22:36:24 GMT  
		Size: 4.0 MB (4015962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5732e83715eb2e1b8bfa444dcc10e458d52a7341f955f7769649a2d480d134`  
		Last Modified: Mon, 08 Dec 2025 22:36:23 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:49277a97a2518d3a564cc3febf0fbd174072605a3eddd98dba1631ccf64aff09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6009a480cb12adb3b8f47931596924d42fcbe66ff669fcf1d7b4e2067c2f0393`

```dockerfile
```

-	Layers:
	-	`sha256:2d10de457e78b892961f31ea28bc8d20f57515f7397c7bb8b9b1e4b0ef7b9a81`  
		Last Modified: Tue, 09 Dec 2025 01:47:08 GMT  
		Size: 2.5 MB (2528521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7070cee358ef4a7a2b0b88274c5d1dd8fe63aa2072b154decfe397e5ba2cfaab`  
		Last Modified: Tue, 09 Dec 2025 01:47:09 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:1.8.0-1`

```console
$ docker pull hitch@sha256:3d6c9c81c3c0000514f0329e09a2ccd78d02830958f649b0df409521b76c7234
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hitch:1.8.0-1` - linux; amd64

```console
$ docker pull hitch@sha256:d8cdbbb65fd280e0a179e479b53f8a9bc09fb5f47fcb54486ca25d34d4433727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32250164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b111ec9be9d13c03e7481e1ac42fb7f831836f6a74dac81a39cf4d0c7d499f4e`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:38:30 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:38:30 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:38:30 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:38:30 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:38:30 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:38:30 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:38:31 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:38:31 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:38:31 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:38:31 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:38:31 GMT
CMD []
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4948d1c638f9e53a7907ed5cc86e6ea390c97f7ca87f0eff02c5ca74400364f1`  
		Last Modified: Mon, 08 Dec 2025 22:38:42 GMT  
		Size: 4.0 MB (4021302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1607c536ced231ececdaf8bea9cc360b67ed066ebe3320112b312db1c0f0051e`  
		Last Modified: Mon, 08 Dec 2025 22:38:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:50a6d2d5e692f5b853ffd4b81d82a8ab308ef83a4ed5f14989b48c144451c55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2544927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf7a07ab0231a85c30b953c694b73d5eaaa3493536ecbe70158357569c7869e`

```dockerfile
```

-	Layers:
	-	`sha256:21b205514099547dbcc1fbdfcb76a4a929c3812cb0fa92df4695970c41d3401b`  
		Last Modified: Tue, 09 Dec 2025 01:46:55 GMT  
		Size: 2.5 MB (2531345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff9d5cde017c428fa4c55dceae78d8464babb564c2ad342500c17d8e6b2be46`  
		Last Modified: Tue, 09 Dec 2025 01:46:55 GMT  
		Size: 13.6 KB (13582 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7fa72fc14e86cdae66d0f5308109a0fc91e72219af1da87900c3c7f265404df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27319297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0fba3ab800c9f6851d460d228002f3492d8a2dbaee3d0af2f67d1169417f3b`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:36:36 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:36:36 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:36:36 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:36:36 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:36:36 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:36:36 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:36:36 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:36:36 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:36 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:36:36 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:36:36 GMT
CMD []
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e12d05562656f2ada4a6c1a89e279d71ae7d4607341c4fd6ed3872a3a165f2`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 3.4 MB (3384831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe81099c0ae18944a3828de6408d45e95ca967b18f95d4edcebb9265d04ccb0`  
		Last Modified: Mon, 08 Dec 2025 22:36:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:033a5f91c9acbce1b5c80de845f633049dad17b96003148783e8e1fe7b0d4f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2547245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f70caa6fb9a5550c239a8d1e3d9d352b6fc3bce599d9c7f27011e7195ce46`

```dockerfile
```

-	Layers:
	-	`sha256:600e7dca7e4a224abdd71f7b55bfd2d32bb002bfb0711d352061914e9d1615ff`  
		Last Modified: Tue, 09 Dec 2025 01:46:59 GMT  
		Size: 2.5 MB (2533577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe0d13cbf4054021a7b33839da223983ac75c99a8ec422c14fa48022c4f3a3b`  
		Last Modified: Tue, 09 Dec 2025 01:47:00 GMT  
		Size: 13.7 KB (13668 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:1dc00ac4dc445a0dca2dcbbf2c1e448340542cabe97861e238264ba4429846be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31974362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e53ad05e8a2a3533254dfabd07450dd9d5d9b413df3d05c7251de4d069d0111`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:33:25 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:33:25 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:33:25 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:33:25 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:33:25 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:33:25 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:33:25 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:33:25 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:25 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:33:25 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:33:25 GMT
CMD []
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7669bcb0960a42101f23697817bdb33540df27a24a66e9747affd47c401057`  
		Last Modified: Mon, 08 Dec 2025 22:33:38 GMT  
		Size: 3.9 MB (3871688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4f6720f4c1ae0c1d00a2529f2a9b5961420036342041a664ceb2aa792c7d7f`  
		Last Modified: Mon, 08 Dec 2025 22:33:38 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:ea28eb37a0f2ed39da63abb42419b2e45ceac2f87d77ac6dcfc79bbade9e92e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e8534a0fbf39350ff049ce1770f6eab3cf5159887c6a866ced97dd6944c5bb`

```dockerfile
```

-	Layers:
	-	`sha256:39efa46ca8d3aabc01e59cffdde2081707946d7f27da767cc1b4a32e5ae80eb3`  
		Last Modified: Tue, 09 Dec 2025 01:47:04 GMT  
		Size: 2.5 MB (2531615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad19fc3d9734e347986795b4059b0eb73c138ba6a8e2775958d213a09373a97e`  
		Last Modified: Tue, 09 Dec 2025 01:47:05 GMT  
		Size: 13.7 KB (13698 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; 386

```console
$ docker pull hitch@sha256:ac5056d4ffcb6d5676e63ee43fb455e7bec8335336f9d46fcf21eb55e6cd7b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33226136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7f5e7fe75cfc8cde9e9dff12afa783993fc90191536207b3f6879d2dfe9892`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:36:11 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:36:11 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:36:11 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:36:11 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:36:11 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:36:11 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:36:11 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:36:11 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:11 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:36:11 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a077194ed7ec145f4f6772fbfbd563b41be1d1ea7524e0041a266f4cc1a711`  
		Last Modified: Mon, 08 Dec 2025 22:36:24 GMT  
		Size: 4.0 MB (4015962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5732e83715eb2e1b8bfa444dcc10e458d52a7341f955f7769649a2d480d134`  
		Last Modified: Mon, 08 Dec 2025 22:36:23 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:49277a97a2518d3a564cc3febf0fbd174072605a3eddd98dba1631ccf64aff09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6009a480cb12adb3b8f47931596924d42fcbe66ff669fcf1d7b4e2067c2f0393`

```dockerfile
```

-	Layers:
	-	`sha256:2d10de457e78b892961f31ea28bc8d20f57515f7397c7bb8b9b1e4b0ef7b9a81`  
		Last Modified: Tue, 09 Dec 2025 01:47:08 GMT  
		Size: 2.5 MB (2528521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7070cee358ef4a7a2b0b88274c5d1dd8fe63aa2072b154decfe397e5ba2cfaab`  
		Last Modified: Tue, 09 Dec 2025 01:47:09 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:latest`

```console
$ docker pull hitch@sha256:3d6c9c81c3c0000514f0329e09a2ccd78d02830958f649b0df409521b76c7234
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hitch:latest` - linux; amd64

```console
$ docker pull hitch@sha256:d8cdbbb65fd280e0a179e479b53f8a9bc09fb5f47fcb54486ca25d34d4433727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32250164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b111ec9be9d13c03e7481e1ac42fb7f831836f6a74dac81a39cf4d0c7d499f4e`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:38:30 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:38:30 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:38:30 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:38:30 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:38:30 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:38:30 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:38:31 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:38:31 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:38:31 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:38:31 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:38:31 GMT
CMD []
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4948d1c638f9e53a7907ed5cc86e6ea390c97f7ca87f0eff02c5ca74400364f1`  
		Last Modified: Mon, 08 Dec 2025 22:38:42 GMT  
		Size: 4.0 MB (4021302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1607c536ced231ececdaf8bea9cc360b67ed066ebe3320112b312db1c0f0051e`  
		Last Modified: Mon, 08 Dec 2025 22:38:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:50a6d2d5e692f5b853ffd4b81d82a8ab308ef83a4ed5f14989b48c144451c55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2544927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf7a07ab0231a85c30b953c694b73d5eaaa3493536ecbe70158357569c7869e`

```dockerfile
```

-	Layers:
	-	`sha256:21b205514099547dbcc1fbdfcb76a4a929c3812cb0fa92df4695970c41d3401b`  
		Last Modified: Tue, 09 Dec 2025 01:46:55 GMT  
		Size: 2.5 MB (2531345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff9d5cde017c428fa4c55dceae78d8464babb564c2ad342500c17d8e6b2be46`  
		Last Modified: Tue, 09 Dec 2025 01:46:55 GMT  
		Size: 13.6 KB (13582 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7fa72fc14e86cdae66d0f5308109a0fc91e72219af1da87900c3c7f265404df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27319297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0fba3ab800c9f6851d460d228002f3492d8a2dbaee3d0af2f67d1169417f3b`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:36:36 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:36:36 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:36:36 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:36:36 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:36:36 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:36:36 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:36:36 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:36:36 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:36 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:36:36 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:36:36 GMT
CMD []
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e12d05562656f2ada4a6c1a89e279d71ae7d4607341c4fd6ed3872a3a165f2`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 3.4 MB (3384831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe81099c0ae18944a3828de6408d45e95ca967b18f95d4edcebb9265d04ccb0`  
		Last Modified: Mon, 08 Dec 2025 22:36:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:033a5f91c9acbce1b5c80de845f633049dad17b96003148783e8e1fe7b0d4f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2547245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f70caa6fb9a5550c239a8d1e3d9d352b6fc3bce599d9c7f27011e7195ce46`

```dockerfile
```

-	Layers:
	-	`sha256:600e7dca7e4a224abdd71f7b55bfd2d32bb002bfb0711d352061914e9d1615ff`  
		Last Modified: Tue, 09 Dec 2025 01:46:59 GMT  
		Size: 2.5 MB (2533577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe0d13cbf4054021a7b33839da223983ac75c99a8ec422c14fa48022c4f3a3b`  
		Last Modified: Tue, 09 Dec 2025 01:47:00 GMT  
		Size: 13.7 KB (13668 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:1dc00ac4dc445a0dca2dcbbf2c1e448340542cabe97861e238264ba4429846be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31974362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e53ad05e8a2a3533254dfabd07450dd9d5d9b413df3d05c7251de4d069d0111`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:33:25 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:33:25 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:33:25 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:33:25 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:33:25 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:33:25 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:33:25 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:33:25 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:25 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:33:25 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:33:25 GMT
CMD []
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7669bcb0960a42101f23697817bdb33540df27a24a66e9747affd47c401057`  
		Last Modified: Mon, 08 Dec 2025 22:33:38 GMT  
		Size: 3.9 MB (3871688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4f6720f4c1ae0c1d00a2529f2a9b5961420036342041a664ceb2aa792c7d7f`  
		Last Modified: Mon, 08 Dec 2025 22:33:38 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:ea28eb37a0f2ed39da63abb42419b2e45ceac2f87d77ac6dcfc79bbade9e92e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e8534a0fbf39350ff049ce1770f6eab3cf5159887c6a866ced97dd6944c5bb`

```dockerfile
```

-	Layers:
	-	`sha256:39efa46ca8d3aabc01e59cffdde2081707946d7f27da767cc1b4a32e5ae80eb3`  
		Last Modified: Tue, 09 Dec 2025 01:47:04 GMT  
		Size: 2.5 MB (2531615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad19fc3d9734e347986795b4059b0eb73c138ba6a8e2775958d213a09373a97e`  
		Last Modified: Tue, 09 Dec 2025 01:47:05 GMT  
		Size: 13.7 KB (13698 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; 386

```console
$ docker pull hitch@sha256:ac5056d4ffcb6d5676e63ee43fb455e7bec8335336f9d46fcf21eb55e6cd7b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33226136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7f5e7fe75cfc8cde9e9dff12afa783993fc90191536207b3f6879d2dfe9892`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:36:11 GMT
ARG SRCVER=1.8.0
# Mon, 08 Dec 2025 22:36:11 GMT
ARG PKGVER=1
# Mon, 08 Dec 2025 22:36:11 GMT
ARG DISTVER=bullseye
# Mon, 08 Dec 2025 22:36:11 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 08 Dec 2025 22:36:11 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 08 Dec 2025 22:36:11 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 08 Dec 2025 22:36:11 GMT
WORKDIR /etc/hitch
# Mon, 08 Dec 2025 22:36:11 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:11 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 08 Dec 2025 22:36:11 GMT
EXPOSE map[443/tcp:{}]
# Mon, 08 Dec 2025 22:36:11 GMT
CMD []
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a077194ed7ec145f4f6772fbfbd563b41be1d1ea7524e0041a266f4cc1a711`  
		Last Modified: Mon, 08 Dec 2025 22:36:24 GMT  
		Size: 4.0 MB (4015962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5732e83715eb2e1b8bfa444dcc10e458d52a7341f955f7769649a2d480d134`  
		Last Modified: Mon, 08 Dec 2025 22:36:23 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:49277a97a2518d3a564cc3febf0fbd174072605a3eddd98dba1631ccf64aff09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6009a480cb12adb3b8f47931596924d42fcbe66ff669fcf1d7b4e2067c2f0393`

```dockerfile
```

-	Layers:
	-	`sha256:2d10de457e78b892961f31ea28bc8d20f57515f7397c7bb8b9b1e4b0ef7b9a81`  
		Last Modified: Tue, 09 Dec 2025 01:47:08 GMT  
		Size: 2.5 MB (2528521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7070cee358ef4a7a2b0b88274c5d1dd8fe63aa2072b154decfe397e5ba2cfaab`  
		Last Modified: Tue, 09 Dec 2025 01:47:09 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json
