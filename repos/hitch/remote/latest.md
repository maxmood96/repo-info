## `hitch:latest`

```console
$ docker pull hitch@sha256:6fb897300084f09217b48745dfda52bf4709f57786df47418ee53274742960c7
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

### `hitch:latest` - linux; amd64

```console
$ docker pull hitch@sha256:0fc40f9ea1d44458d9e049340792b017747b0807ac480207124e5bead6b17d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31827636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b55b33c7a8a6000b117f1da30ce88f6d4170b0e9166193248fbb6642a12939`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc57f09e1a1e64181331479579527ebea35299b9c48e8629d7744a4ebafd7dd`  
		Last Modified: Tue, 03 Jun 2025 20:40:15 GMT  
		Size: 1.6 MB (1571249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42ba5fb038af1861905397c88d7a1f9064a3fe1624032d0e091ab9db8be9848`  
		Last Modified: Tue, 03 Jun 2025 20:40:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:f8fe075157b99e4a69e6df1dc3fede89102999f2d645c509232161d885ff2de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b9ccc98ef382804e19756b6196449acdefe96f5445f03073d8a2bc62539fa`

```dockerfile
```

-	Layers:
	-	`sha256:a3edf26a1553cfa932389f12f1b7b21a0571a0f71db48f8b68c9f77393d9e111`  
		Last Modified: Sun, 08 Jun 2025 05:13:48 GMT  
		Size: 2.7 MB (2711895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94327af2f83c7c31412b43389027ac49f3b7f9b0f2f0028cf66091d706a903fc`  
		Last Modified: Sun, 08 Jun 2025 05:13:50 GMT  
		Size: 13.6 KB (13625 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm variant v7

```console
$ docker pull hitch@sha256:28e70375aedc6076966733e154aa9b7f316a2dca0449420334ffb828e33ed86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27034353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a537d705a1ebc663281085c9d3a490f608c0621986b438e9b6450292ab59d805`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:2091b63a268a34467e23520ae27c312421298f420abd278e760061e42a678899`  
		Last Modified: Tue, 03 Jun 2025 13:50:37 GMT  
		Size: 25.5 MB (25543902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878b1eaf6e94e68517775fd4433c78a3e0283b572cee8efa16bb38059e889b1c`  
		Last Modified: Wed, 21 May 2025 23:23:57 GMT  
		Size: 1.5 MB (1490006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3eb8b105f8dd7804f8de5ccaf843f16363d6e54b363d933ed8cd4e17be0671`  
		Last Modified: Sat, 07 Jun 2025 07:09:46 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:1f8a00fb76fb6617d1bd63eca424464fd7d6a15e8b4aa5202b78395ab04cf922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da277662aef27d8fab97797edc3489f6924675a9705e9a67d15137ee259dfa2`

```dockerfile
```

-	Layers:
	-	`sha256:d6bad2112c788e8b4b3584e74072f7ac2b8a79557ac98a0fcd3ae7ce9632c241`  
		Last Modified: Wed, 21 May 2025 23:23:57 GMT  
		Size: 2.7 MB (2714127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0493ba3766524795afdf8fe2612fe452368e29f42f4a9fe470793283ad92c96b`  
		Last Modified: Wed, 21 May 2025 23:23:57 GMT  
		Size: 13.7 KB (13708 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:f4cac8f7368e01dff6f93bf3ceb84a147b469bb4b4c3518cdf9d0b0dc373a7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30296167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab530bbd9f187271963bdcf759e8f88e3bad6f0b91f760c7236dc687c943ee88`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ca203bd355e7467dbb09461d270f577ef74ad2bf18690ff66f5ee7edcecea`  
		Last Modified: Tue, 03 Jun 2025 22:07:10 GMT  
		Size: 1.5 MB (1549464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ce167264ff1759192fb79553d50d726e5fc31c357878559929d4608a498893`  
		Last Modified: Tue, 03 Jun 2025 22:07:13 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:0ae262c01f740a33168d8c23c5b3c7b927324ed13a16587aa10c1387e086bbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1072138f76f10e712ee393a09ad048ae10ec8f1ff31611df79508dfd6b826d30`

```dockerfile
```

-	Layers:
	-	`sha256:74811bbd256b85b05497a5f1520d46ff462633b48b623cb400bc7610c8b4d0a1`  
		Last Modified: Wed, 21 May 2025 23:56:04 GMT  
		Size: 2.7 MB (2712159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf00a400b068846ee3c6dbc7b11ec8971ed25ae45b89d7cbedfca756a53bddb`  
		Last Modified: Wed, 21 May 2025 23:56:03 GMT  
		Size: 13.7 KB (13741 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; 386

```console
$ docker pull hitch@sha256:f9a4eec1c91d286d40cb1530587e6db006b22f0aec7e2ba414744375faeffa7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32764693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0204cacf3e9c85767071f15543fd4f7c5db163d85abc9170db0c1924ebb409f0`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Tue, 03 Jun 2025 13:42:18 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f4873a470756fa89848e617d53cdd22c970110d1946842efb3bbe090b0a074`  
		Last Modified: Wed, 21 May 2025 23:13:20 GMT  
		Size: 1.6 MB (1575047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5d06033d0c2b700bd68f96a076654cbf731fa1cd468d9fa4746fcc973d2ec8`  
		Last Modified: Sat, 07 Jun 2025 07:17:50 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:f036630983d2b20aad1d2e0d357b74609edbfb1e45fa1d969c64aebdbb12e459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edab1c0ec31927480a9ce44f34667000c4f6aa42270a48b76c2ed53ab281901`

```dockerfile
```

-	Layers:
	-	`sha256:54ac17d2d7628dccdccdcd9351added8bb9b375f2c7eee48e8cbf067fe79b82d`  
		Last Modified: Wed, 21 May 2025 23:13:20 GMT  
		Size: 2.7 MB (2709067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a02fb75d8deb611515b182e093f7de8877d8f21fd28d35ff3b9cd5f61df9e90`  
		Last Modified: Wed, 21 May 2025 23:13:20 GMT  
		Size: 13.6 KB (13588 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; ppc64le

```console
$ docker pull hitch@sha256:1bdcd7bcd169b8de699dae282ed9132427b99bb8f3bfbac1cacbc2ce1d5b104f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36928037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de96c4164756efbaae82116b7b72bb2095a5138cae636ec7e0a585c93ee52057`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Tue, 22 Aug 2023 15:19:07 GMT
CMD ["bash"]
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Tue, 07 Jan 2025 02:35:40 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b96d996552b8211abcb134c637a2ff1f40f8948acc4fc03da156fc00d2cb2dd`  
		Last Modified: Tue, 07 Jan 2025 20:35:45 GMT  
		Size: 1.6 MB (1628321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec36644e74cb980ba714eec6ecf5729391a63781a34991264fc61069a239d5db`  
		Last Modified: Mon, 06 Jan 2025 17:36:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:930b2a56783983d94990c5d8eb69841e1848a966f490e074c6f503c302919ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d1a71ab384aeac4980491883bcacb6682bb7ac79f99b75bdbef94246966341`

```dockerfile
```

-	Layers:
	-	`sha256:e83fceb4779f1817190640cf46aed07d46fd4b4cc148eb334f5dfafb1e675232`  
		Last Modified: Tue, 07 Jan 2025 01:35:16 GMT  
		Size: 2.7 MB (2685293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184e2f5c531bc52d63020dfb5cd44800780636aca7503a3adc510611f503d18c`  
		Last Modified: Wed, 08 Jan 2025 02:35:14 GMT  
		Size: 13.5 KB (13463 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; s390x

```console
$ docker pull hitch@sha256:d91204d37425e40a174c327556e101e756d3baae8af570d95d555175f76557b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31230843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae76908cceba307dde76e2e850f030d7571830f0b04f29b209232c4300010224`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Tue, 22 Aug 2023 15:19:07 GMT
CMD ["bash"]
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SRCVER=1.8.0
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGVER=1
# Tue, 22 Aug 2023 15:19:07 GMT
ARG DISTVER=bullseye
# Tue, 22 Aug 2023 15:19:07 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 22 Aug 2023 15:19:07 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 22 Aug 2023 15:19:07 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
WORKDIR /etc/hitch
# Tue, 22 Aug 2023 15:19:07 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 22 Aug 2023 15:19:07 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 22 Aug 2023 15:19:07 GMT
EXPOSE map[443/tcp:{}]
# Tue, 22 Aug 2023 15:19:07 GMT
CMD []
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Sun, 15 Dec 2024 19:17:08 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e973ddf7be7a3ef6ce409e675b83570f4141ba68727c4e5c2f375f48cc2bc67b`  
		Last Modified: Tue, 07 Jan 2025 05:35:08 GMT  
		Size: 1.6 MB (1566950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e660d42d0e4abfddbd5150c5fe8d04d19a455b3f0e9087d918b43b3324de5921`  
		Last Modified: Tue, 07 Jan 2025 22:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:03077a449c74e88e0f899654f6a39799feba8a345a61c14977d87473d71d3cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83d9dbc2df4829224947aa1ed659ad6749d36e63643e1abdfe15a0bf852fa77`

```dockerfile
```

-	Layers:
	-	`sha256:c77e4f53cec64a928050cca209f5b7c0d729347e768f45f7364466661e048246`  
		Last Modified: Mon, 06 Jan 2025 19:40:16 GMT  
		Size: 2.7 MB (2681168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be908d7cfac6586649e4fd45008a52ba458489d3ff11fa452c4ec31abe0fd571`  
		Last Modified: Tue, 07 Jan 2025 03:35:24 GMT  
		Size: 13.4 KB (13416 bytes)  
		MIME: application/vnd.in-toto+json
