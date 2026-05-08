## `hitch:latest`

```console
$ docker pull hitch@sha256:d992e61ce43045e905832c4b495d6059a555e8425ff0b92dce586fc8e315a360
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
$ docker pull hitch@sha256:7adf571567e3fab135e03ec2c66c9225f52b8f746a1972f1cd0ce210031d493e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32260649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156fa06220492b3d7e18fe0b4c663b809cb6089262ffdc1d0678937e8cab151b`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:21:21 GMT
ARG SRCVER=1.8.0
# Wed, 22 Apr 2026 01:21:21 GMT
ARG PKGVER=1
# Wed, 22 Apr 2026 01:21:21 GMT
ARG DISTVER=bullseye
# Wed, 22 Apr 2026 01:21:21 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 22 Apr 2026 01:21:21 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Wed, 22 Apr 2026 01:21:21 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Wed, 22 Apr 2026 01:21:21 GMT
WORKDIR /etc/hitch
# Wed, 22 Apr 2026 01:21:21 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:21 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 22 Apr 2026 01:21:21 GMT
EXPOSE map[443/tcp:{}]
# Wed, 22 Apr 2026 01:21:21 GMT
CMD []
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae73c28585de61732da08fafc41a62796dce8c707dfa14aff2133d2fc8cda455`  
		Last Modified: Wed, 22 Apr 2026 01:21:27 GMT  
		Size: 4.0 MB (4023952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108b0387d57729f282225475f004c779649075926171ca66bc5b30b94ca98c90`  
		Last Modified: Wed, 22 Apr 2026 01:21:27 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:c0f49e38e1bbf1581296366d01d7f3b0a8f699cea534dfe09c4c4f79f2ea684c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2544936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d7ae88c96e0b98ded0f0927fa37ff5e960893a6ee2e2932ce27406379cc6dc`

```dockerfile
```

-	Layers:
	-	`sha256:f59e0bc29be0dfa8834d68a9cb5594a323d20bea5b15a4c27fdfd59d23e6c3e0`  
		Last Modified: Wed, 22 Apr 2026 01:21:27 GMT  
		Size: 2.5 MB (2531355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3da69862a7ac265acccd004449b8ad61decfcd9510f296b5da1802feda4156ec`  
		Last Modified: Wed, 22 Apr 2026 01:21:27 GMT  
		Size: 13.6 KB (13581 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm variant v7

```console
$ docker pull hitch@sha256:0891784be7c41b45ff5313a755b3e3ad922fb1a11d10111a69f2e963acde66ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27328430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c71e7bc1cf8e47fdf9abed7abe38d2ebdf165f1e1ab497cd58130f76d039c89`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:18:55 GMT
ARG SRCVER=1.8.0
# Wed, 22 Apr 2026 01:18:55 GMT
ARG PKGVER=1
# Wed, 22 Apr 2026 01:18:55 GMT
ARG DISTVER=bullseye
# Wed, 22 Apr 2026 01:18:55 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 22 Apr 2026 01:18:55 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Wed, 22 Apr 2026 01:18:55 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Wed, 22 Apr 2026 01:18:56 GMT
WORKDIR /etc/hitch
# Wed, 22 Apr 2026 01:18:56 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:18:56 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 22 Apr 2026 01:18:56 GMT
EXPOSE map[443/tcp:{}]
# Wed, 22 Apr 2026 01:18:56 GMT
CMD []
```

-	Layers:
	-	`sha256:d3311d55816cf34cc663f098f8e93bb8dca4772ce9f25ac1e909fa7b0628d17b`  
		Last Modified: Wed, 22 Apr 2026 00:16:41 GMT  
		Size: 23.9 MB (23941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691b011616da4bf5a5e76b05343c949919a5e5e06160627f59ddde37100e76fd`  
		Last Modified: Wed, 22 Apr 2026 01:19:02 GMT  
		Size: 3.4 MB (3386562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e22f88a375a315ec5fc636993f04daa377f4d728aae21a2852588e5781838c9`  
		Last Modified: Wed, 22 Apr 2026 01:19:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:420b3b054364972863b33d1425338a098698ef862100caa14f6ed2aa5ea10ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2547256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d625d7fec00d40411515ec8e2f49ab36106d79be1cfd37d049787ddabef8610`

```dockerfile
```

-	Layers:
	-	`sha256:cd929e55de18a40acf5befc583a974b512dc30c12d6ef20e93fbf391e7c23daf`  
		Last Modified: Wed, 22 Apr 2026 01:19:02 GMT  
		Size: 2.5 MB (2533587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73fd3c47e8dc99e095a888476f3adf49703b679590042ce22c6ecf20ee1b10d3`  
		Last Modified: Wed, 22 Apr 2026 01:19:02 GMT  
		Size: 13.7 KB (13669 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:89be6633006c13aabc6661e22eff5098f112c527241cdcc2793664a216c06138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31989407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa86b88db95d82c7e4be072b33b3234d93d70cb97e20c9c8918b78f34ce7f5c`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:20:59 GMT
ARG SRCVER=1.8.0
# Fri, 08 May 2026 19:20:59 GMT
ARG PKGVER=1
# Fri, 08 May 2026 19:20:59 GMT
ARG DISTVER=bullseye
# Fri, 08 May 2026 19:20:59 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Fri, 08 May 2026 19:20:59 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Fri, 08 May 2026 19:20:59 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Fri, 08 May 2026 19:20:59 GMT
WORKDIR /etc/hitch
# Fri, 08 May 2026 19:20:59 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:20:59 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Fri, 08 May 2026 19:20:59 GMT
EXPOSE map[443/tcp:{}]
# Fri, 08 May 2026 19:20:59 GMT
CMD []
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ab97d7c90e4209d539d24daee88a4f23425193a703f6f6ab5289805fd94940`  
		Last Modified: Fri, 08 May 2026 19:21:06 GMT  
		Size: 3.9 MB (3872798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a685bdeb4f1c8f4cc0385da490e8e0abc9b9f3ba451c9f816424702217661507`  
		Last Modified: Fri, 08 May 2026 19:21:06 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:62738af6f3a0cd37dd62c2fc305721282a5c027feb8c4b12cc5dea54df3ee350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a9d4d5f55727e7a49450e6fd890d638cd560db1f0d2b8248dbac7d9ba4c5a7`

```dockerfile
```

-	Layers:
	-	`sha256:55a8813fd8ee6a3023e5e6b53dda0216907e4f19c3348567c4da3c6c2755bfea`  
		Last Modified: Fri, 08 May 2026 19:21:06 GMT  
		Size: 2.5 MB (2531625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4705b67c9caa4b6be71f128ef54e7eda706c14bc40625fd32fc77c2d6f481e00`  
		Last Modified: Fri, 08 May 2026 19:21:06 GMT  
		Size: 13.7 KB (13698 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; 386

```console
$ docker pull hitch@sha256:a78f816d1a06969b7aefc787226eb24b6da261edadea4e5c23cb2ce10d5755a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33240507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1ffbdd7c87e8d9481bfce8e5b5546d5fd9deee7daff0434efe21f074972ab`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:17:40 GMT
ARG SRCVER=1.8.0
# Wed, 22 Apr 2026 01:17:40 GMT
ARG PKGVER=1
# Wed, 22 Apr 2026 01:17:40 GMT
ARG DISTVER=bullseye
# Wed, 22 Apr 2026 01:17:40 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 22 Apr 2026 01:17:40 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Wed, 22 Apr 2026 01:17:40 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Wed, 22 Apr 2026 01:17:40 GMT
WORKDIR /etc/hitch
# Wed, 22 Apr 2026 01:17:40 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:17:40 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 22 Apr 2026 01:17:40 GMT
EXPOSE map[443/tcp:{}]
# Wed, 22 Apr 2026 01:17:40 GMT
CMD []
```

-	Layers:
	-	`sha256:ceab9188c99bb4807b7b5b31c76962e728b9040bd3676ebeeabf72b13d039523`  
		Last Modified: Wed, 22 Apr 2026 00:16:30 GMT  
		Size: 29.2 MB (29221696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce7e15ae02a5af795a0dc88bce95033aacfd1fff9245c4aa5ed912842e07e7c`  
		Last Modified: Wed, 22 Apr 2026 01:17:47 GMT  
		Size: 4.0 MB (4018367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbae3d839ab2d186b26b7d99ea02f2e2938de38a5e98426fff11d619155b1f6`  
		Last Modified: Wed, 22 Apr 2026 01:17:46 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:3cbfae7c16c4a1989f75db396814b30c4dafe1aed7bd6939fdfd7b0d7ae7edcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d6c5124aae41d612d66b2b02c79e4575f853f6c36ddbb5910024d544d86ceb`

```dockerfile
```

-	Layers:
	-	`sha256:b7931abc5cd73cb8b28643ef0c0b6dc855f2cf4738019a59cc2b7c335a5e1cbb`  
		Last Modified: Wed, 22 Apr 2026 01:17:46 GMT  
		Size: 2.5 MB (2528531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6524ed60231b14900fb248b4408c9abe96766459ffabbaed9eecbe998a9399d`  
		Last Modified: Wed, 22 Apr 2026 01:17:46 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json
