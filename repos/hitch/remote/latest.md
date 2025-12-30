## `hitch:latest`

```console
$ docker pull hitch@sha256:ed16f88ed94daf13aed858a30c69a42d6e216ceb8be2e797466e161b0dfcf5df
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
$ docker pull hitch@sha256:623cc9f677bbb11c47db0fb4b3cbeb962667c45e2987559d6dca09ff12af8b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32250212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b3a8183fce353303dbb72ed6d1ca73e2e282a2e01277b6cd5d1e5e6f880bd6`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:21:50 GMT
ARG SRCVER=1.8.0
# Mon, 29 Dec 2025 23:21:50 GMT
ARG PKGVER=1
# Mon, 29 Dec 2025 23:21:50 GMT
ARG DISTVER=bullseye
# Mon, 29 Dec 2025 23:21:50 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 29 Dec 2025 23:21:50 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 29 Dec 2025 23:21:50 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 29 Dec 2025 23:21:50 GMT
WORKDIR /etc/hitch
# Mon, 29 Dec 2025 23:21:50 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:21:50 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 29 Dec 2025 23:21:50 GMT
EXPOSE map[443/tcp:{}]
# Mon, 29 Dec 2025 23:21:50 GMT
CMD []
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690075e761bcfdaac7c599c03020007ba3b699a7aa1f2046e855820f4b22ce0e`  
		Last Modified: Mon, 29 Dec 2025 23:22:03 GMT  
		Size: 4.0 MB (4021343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38fb992c10095254851ad20ae1c3efd871138ce489dcb5d7d6d86c62e1c4a3b`  
		Last Modified: Mon, 29 Dec 2025 23:22:02 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:97dab22f3d9d394932308b9a80d1b6ed81da97046e3fd0045faac839825e0b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2544927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798fe93cefd53999acdd99a58831c3189eb2570104af59b97171198f44c9011c`

```dockerfile
```

-	Layers:
	-	`sha256:c4edbc7b4b9f27ac8e9446da03e17946f0309258e08c40c3b0387b0043af114d`  
		Last Modified: Tue, 30 Dec 2025 01:47:26 GMT  
		Size: 2.5 MB (2531345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf69f6074d14af324c571a7b5c23b2dac287f8276b36c6f08e30f070197043c`  
		Last Modified: Tue, 30 Dec 2025 01:47:27 GMT  
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
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
$ docker pull hitch@sha256:90e4a4431802afe8806acbc085027e97da1d3d8e97849344d8f2027f1ff3a8f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31974361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca3d951be504d7747da48ca9158e77c8695d600ff551dc352377d12558dde24`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:20:45 GMT
ARG SRCVER=1.8.0
# Mon, 29 Dec 2025 23:20:45 GMT
ARG PKGVER=1
# Mon, 29 Dec 2025 23:20:45 GMT
ARG DISTVER=bullseye
# Mon, 29 Dec 2025 23:20:45 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 29 Dec 2025 23:20:45 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 29 Dec 2025 23:20:45 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 29 Dec 2025 23:20:45 GMT
WORKDIR /etc/hitch
# Mon, 29 Dec 2025 23:20:45 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:45 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 29 Dec 2025 23:20:45 GMT
EXPOSE map[443/tcp:{}]
# Mon, 29 Dec 2025 23:20:45 GMT
CMD []
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64a74f75f541492b13524b731dd1e69266e618d1d99654ff0725a1bb9e2ada7`  
		Last Modified: Mon, 29 Dec 2025 23:20:58 GMT  
		Size: 3.9 MB (3871707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0f6ef9869f8f4a4f73de93faaf73e05a207079c7d1703bb4cf6b6941fab7e3`  
		Last Modified: Mon, 29 Dec 2025 23:20:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:8fd2a705062c5dd4d8d4b73546ac9f081ec761973478b54ffef8d22f0857f760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a429f0326b12e8a445904cda077d8bf465ba098d56f06169aa1ad61132d8b8`

```dockerfile
```

-	Layers:
	-	`sha256:f76fd25982a59978b541178935e5274b1f3946170fa97af1fbbfaa96fd63d45b`  
		Last Modified: Tue, 30 Dec 2025 01:47:37 GMT  
		Size: 2.5 MB (2531615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55cb523cc0441449d449b15c7782bd487904932fae7ec52773fb720835fe6836`  
		Last Modified: Tue, 30 Dec 2025 01:47:38 GMT  
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
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
