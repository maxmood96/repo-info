<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `hitch`

-	[`hitch:1`](#hitch1)
-	[`hitch:1.8`](#hitch18)
-	[`hitch:1.8.0`](#hitch180)
-	[`hitch:1.8.0-1`](#hitch180-1)
-	[`hitch:latest`](#hitchlatest)

## `hitch:1`

```console
$ docker pull hitch@sha256:e5fccf50546ab1724f3a7e958c504140fb466bf2d27fc4d90bc527b7dddb585f
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

### `hitch:1` - linux; amd64

```console
$ docker pull hitch@sha256:634b262073d168d62c44baf0ee8b6579ec1dc6399b673544adaa39dc2b677bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32998464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7dea6f1510ed8dd4ee69b4241944b010e43307ddc2979c92661ef4115cc624`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4883567b4bb0fc1fa52acd4cb857168ad41baa9654c83027dfbc914948097990`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 1.6 MB (1569690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad116d0fcf6cbbb125c7c50740f67eb330a3b288c01a2492a1faeb66262ec5b5`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:30eb4f014b0df465074ff89e278bb79bb2919c728865b5adc2c6c23200082c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebb6cc9a352a3ac41f3c5cdd006f2a690758b37d99ec0a54e74e8aa65a86aef`

```dockerfile
```

-	Layers:
	-	`sha256:8925509d70a772fbbcea0958493fae2fc014cc9d9cafe2afc19d2de0ede9d25e`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 2.7 MB (2680963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbbdbf33bccad2a44acdbfba5338fa4a218e802388289fde911052d7a3b8b30`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 13.4 KB (13418 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:981d450a3e81145a9b2130fe1c7dbe443a2eea38ab972e756aa3e3716b045355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28078165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144090bd5c4246795c40b8cc1e0997123d807d4c873a1d59fac30cdaa7de3049`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
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
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9c2aa502d43acbcb5595150f593e1a0efb15cd856419d09c0f1be5d981dfff`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 1.5 MB (1488591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e127634bebf3abf5444ea33fab4571e990ec450543485d0d886835048376ccdb`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:004b4069765b12a0d2adc95d51b9d45410849c9af6aa810484b4b78f0756e0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25eba83e05d9e2558a232d07ae49fe26c9a5018af842a460f55c137cc669f470`

```dockerfile
```

-	Layers:
	-	`sha256:5e91e859c9b01c135d7d5cceda113f8caa92c170592ce436e56f4cbd8d2cf581`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 2.7 MB (2683194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1c8f004fa7967294a167804dc0cac2fecfefa353171e717b765ae145610d0ec`  
		Last Modified: Tue, 23 Jul 2024 17:53:38 GMT  
		Size: 13.5 KB (13497 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:fa75d0ea0162e7206228236ad85d7d15ff505273ee0015cefca06eb7b4176df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31624473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59df3aa7896cf31e3f5a0dc59e0cb05461d995a394c7d2fe5c707afc2bd9c3b7`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f934bb8adda65d7f158f8c504468174b4e8b30dd16998bb715d13460c72487`  
		Last Modified: Tue, 23 Jul 2024 18:02:56 GMT  
		Size: 1.5 MB (1547947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82995ad423fbc7a98db968925112c88ee990c4ccce3e50353091ae79f8db00e4`  
		Last Modified: Tue, 23 Jul 2024 18:02:55 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:a73dbb5f3ad2edc9f18e01af81db961c928f153c776876d522818aa0305e90c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7456a191710babae6d9d3379d5079efad82b1f5b86bda1af033baa8ccc9701`

```dockerfile
```

-	Layers:
	-	`sha256:625a25d0461783c4afc3583811a1aacbacad0b67d3cc5c957781fa540b84ac39`  
		Last Modified: Tue, 23 Jul 2024 18:02:56 GMT  
		Size: 2.7 MB (2681226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:851a4b9b5477b11379ebc8427770cb8e1730529dade424cc1af5d052e45acad2`  
		Last Modified: Tue, 23 Jul 2024 18:02:55 GMT  
		Size: 13.7 KB (13740 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; 386

```console
$ docker pull hitch@sha256:637cb4e821c4601ba7f8589306abdcc278ceb540629d07511a26205f2ee546a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33987907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d66b1e16ff12161364c33b548eecfabe456c0deda623de2b00c0000dd0182c`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
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
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b334d2b26b3df7d9cbdd70f000a5c822ce4e7bb7066b74fb9031116dffa0e9c2`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 1.6 MB (1573655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dded04ace82dcdddba7b8b99a9c2b2cd1c00760df660a5654ccdf64faad1d616`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:565d9a35732e29ad5f72de9c4e0aa495204408f4acf7626a288d7d594857ec2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b497475d79dff7880f114285f4c0c5913c13ff4ab5fdad8cec24415c42d2660c`

```dockerfile
```

-	Layers:
	-	`sha256:0d912c72abe92dde4d8c7632ed173709b2f674c57b409daa521eae5ae42632ce`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 2.7 MB (2678086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337dae020c5431496b7a528cb6fbf11b4516ee309576895f215b6282a8ef8493`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 13.4 KB (13385 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; ppc64le

```console
$ docker pull hitch@sha256:97692cd5e86b5195cd960ede47c604faa873df60847065434fe5b55221a00ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36934052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd149623778b2443477f6eb5471cc83ea80aff40dc5c8073928c7e83c2bd11f`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
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
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daadd4be7446559c1170eaca7a01cfd46dfd1ec9319f4d038ecc80726c01df16`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 1.6 MB (1628405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5f8c11dcbedaf561050b71774d65ab300bec506c09cdc0c06ac19e5d8de8b`  
		Last Modified: Tue, 23 Jul 2024 17:15:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:db51106e83229bbe9cef11353b5c88ebdc5def9516cf6884f61e7a7c0894055d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b904ce56fd81e73cf9baa0a00b9bdc55f05c3c0cd89b40fc85bbb418c6b02a1`

```dockerfile
```

-	Layers:
	-	`sha256:520693713f87c110c79d828e280b7b46608507dbc13592156c87488a3950d93f`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 2.7 MB (2685293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be4b9240eb3a724b62c55728cdfaf0cd84810adb1610676f1ea8e1a58734478`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 13.5 KB (13463 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; s390x

```console
$ docker pull hitch@sha256:9ad9f59d1df7555a273c466fc16578784dc8d2bc3d2de5502d5afacbbfa5b35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31236664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7f61b597a013e007953f1026f56325114016d13f50270be0360432c7bc25f8`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
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
	-	`sha256:de4a305fc1af45cc7ae97020dfe639e8990f6d00b7e0ef222c4cdd720f0fc373`  
		Last Modified: Tue, 23 Jul 2024 02:33:12 GMT  
		Size: 29.7 MB (29669018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ad7a78b5b5d0fe5197110ddffe7968cd045a7944d897e6723083f9849631c1`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 1.6 MB (1567201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38710f5e1ec9096f8e9bffa426e0c75fbbe6e4f3568a1a6424720fec7874864`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:ff4969b45fae8337c40248720ca6f0a2cd44dcb9bf6e1a206f4a092137450497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d023046794e03598606f38e9e3ff72622c9f0a48937c7142fefe1a24e4e7ef3d`

```dockerfile
```

-	Layers:
	-	`sha256:52830f4dbc84668719e910e07b7980877f12c0ebf64f4d81ca200bf7a7b0910f`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 2.7 MB (2681168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e501c35fa58c72fcd61d817750f828b8e17e72a6bf3b6c9106fb85c9a7009e`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 13.4 KB (13419 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:1.8`

```console
$ docker pull hitch@sha256:e5fccf50546ab1724f3a7e958c504140fb466bf2d27fc4d90bc527b7dddb585f
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

### `hitch:1.8` - linux; amd64

```console
$ docker pull hitch@sha256:634b262073d168d62c44baf0ee8b6579ec1dc6399b673544adaa39dc2b677bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32998464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7dea6f1510ed8dd4ee69b4241944b010e43307ddc2979c92661ef4115cc624`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4883567b4bb0fc1fa52acd4cb857168ad41baa9654c83027dfbc914948097990`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 1.6 MB (1569690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad116d0fcf6cbbb125c7c50740f67eb330a3b288c01a2492a1faeb66262ec5b5`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:30eb4f014b0df465074ff89e278bb79bb2919c728865b5adc2c6c23200082c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebb6cc9a352a3ac41f3c5cdd006f2a690758b37d99ec0a54e74e8aa65a86aef`

```dockerfile
```

-	Layers:
	-	`sha256:8925509d70a772fbbcea0958493fae2fc014cc9d9cafe2afc19d2de0ede9d25e`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 2.7 MB (2680963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbbdbf33bccad2a44acdbfba5338fa4a218e802388289fde911052d7a3b8b30`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 13.4 KB (13418 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; arm variant v7

```console
$ docker pull hitch@sha256:981d450a3e81145a9b2130fe1c7dbe443a2eea38ab972e756aa3e3716b045355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28078165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144090bd5c4246795c40b8cc1e0997123d807d4c873a1d59fac30cdaa7de3049`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
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
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9c2aa502d43acbcb5595150f593e1a0efb15cd856419d09c0f1be5d981dfff`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 1.5 MB (1488591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e127634bebf3abf5444ea33fab4571e990ec450543485d0d886835048376ccdb`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:004b4069765b12a0d2adc95d51b9d45410849c9af6aa810484b4b78f0756e0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25eba83e05d9e2558a232d07ae49fe26c9a5018af842a460f55c137cc669f470`

```dockerfile
```

-	Layers:
	-	`sha256:5e91e859c9b01c135d7d5cceda113f8caa92c170592ce436e56f4cbd8d2cf581`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 2.7 MB (2683194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1c8f004fa7967294a167804dc0cac2fecfefa353171e717b765ae145610d0ec`  
		Last Modified: Tue, 23 Jul 2024 17:53:38 GMT  
		Size: 13.5 KB (13497 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:fa75d0ea0162e7206228236ad85d7d15ff505273ee0015cefca06eb7b4176df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31624473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59df3aa7896cf31e3f5a0dc59e0cb05461d995a394c7d2fe5c707afc2bd9c3b7`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f934bb8adda65d7f158f8c504468174b4e8b30dd16998bb715d13460c72487`  
		Last Modified: Tue, 23 Jul 2024 18:02:56 GMT  
		Size: 1.5 MB (1547947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82995ad423fbc7a98db968925112c88ee990c4ccce3e50353091ae79f8db00e4`  
		Last Modified: Tue, 23 Jul 2024 18:02:55 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:a73dbb5f3ad2edc9f18e01af81db961c928f153c776876d522818aa0305e90c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7456a191710babae6d9d3379d5079efad82b1f5b86bda1af033baa8ccc9701`

```dockerfile
```

-	Layers:
	-	`sha256:625a25d0461783c4afc3583811a1aacbacad0b67d3cc5c957781fa540b84ac39`  
		Last Modified: Tue, 23 Jul 2024 18:02:56 GMT  
		Size: 2.7 MB (2681226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:851a4b9b5477b11379ebc8427770cb8e1730529dade424cc1af5d052e45acad2`  
		Last Modified: Tue, 23 Jul 2024 18:02:55 GMT  
		Size: 13.7 KB (13740 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; 386

```console
$ docker pull hitch@sha256:637cb4e821c4601ba7f8589306abdcc278ceb540629d07511a26205f2ee546a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33987907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d66b1e16ff12161364c33b548eecfabe456c0deda623de2b00c0000dd0182c`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
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
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b334d2b26b3df7d9cbdd70f000a5c822ce4e7bb7066b74fb9031116dffa0e9c2`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 1.6 MB (1573655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dded04ace82dcdddba7b8b99a9c2b2cd1c00760df660a5654ccdf64faad1d616`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:565d9a35732e29ad5f72de9c4e0aa495204408f4acf7626a288d7d594857ec2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b497475d79dff7880f114285f4c0c5913c13ff4ab5fdad8cec24415c42d2660c`

```dockerfile
```

-	Layers:
	-	`sha256:0d912c72abe92dde4d8c7632ed173709b2f674c57b409daa521eae5ae42632ce`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 2.7 MB (2678086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337dae020c5431496b7a528cb6fbf11b4516ee309576895f215b6282a8ef8493`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 13.4 KB (13385 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; ppc64le

```console
$ docker pull hitch@sha256:97692cd5e86b5195cd960ede47c604faa873df60847065434fe5b55221a00ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36934052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd149623778b2443477f6eb5471cc83ea80aff40dc5c8073928c7e83c2bd11f`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
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
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daadd4be7446559c1170eaca7a01cfd46dfd1ec9319f4d038ecc80726c01df16`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 1.6 MB (1628405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5f8c11dcbedaf561050b71774d65ab300bec506c09cdc0c06ac19e5d8de8b`  
		Last Modified: Tue, 23 Jul 2024 17:15:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:db51106e83229bbe9cef11353b5c88ebdc5def9516cf6884f61e7a7c0894055d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b904ce56fd81e73cf9baa0a00b9bdc55f05c3c0cd89b40fc85bbb418c6b02a1`

```dockerfile
```

-	Layers:
	-	`sha256:520693713f87c110c79d828e280b7b46608507dbc13592156c87488a3950d93f`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 2.7 MB (2685293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be4b9240eb3a724b62c55728cdfaf0cd84810adb1610676f1ea8e1a58734478`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 13.5 KB (13463 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; s390x

```console
$ docker pull hitch@sha256:9ad9f59d1df7555a273c466fc16578784dc8d2bc3d2de5502d5afacbbfa5b35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31236664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7f61b597a013e007953f1026f56325114016d13f50270be0360432c7bc25f8`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
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
	-	`sha256:de4a305fc1af45cc7ae97020dfe639e8990f6d00b7e0ef222c4cdd720f0fc373`  
		Last Modified: Tue, 23 Jul 2024 02:33:12 GMT  
		Size: 29.7 MB (29669018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ad7a78b5b5d0fe5197110ddffe7968cd045a7944d897e6723083f9849631c1`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 1.6 MB (1567201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38710f5e1ec9096f8e9bffa426e0c75fbbe6e4f3568a1a6424720fec7874864`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:ff4969b45fae8337c40248720ca6f0a2cd44dcb9bf6e1a206f4a092137450497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d023046794e03598606f38e9e3ff72622c9f0a48937c7142fefe1a24e4e7ef3d`

```dockerfile
```

-	Layers:
	-	`sha256:52830f4dbc84668719e910e07b7980877f12c0ebf64f4d81ca200bf7a7b0910f`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 2.7 MB (2681168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e501c35fa58c72fcd61d817750f828b8e17e72a6bf3b6c9106fb85c9a7009e`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 13.4 KB (13419 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:1.8.0`

```console
$ docker pull hitch@sha256:e5fccf50546ab1724f3a7e958c504140fb466bf2d27fc4d90bc527b7dddb585f
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

### `hitch:1.8.0` - linux; amd64

```console
$ docker pull hitch@sha256:634b262073d168d62c44baf0ee8b6579ec1dc6399b673544adaa39dc2b677bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32998464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7dea6f1510ed8dd4ee69b4241944b010e43307ddc2979c92661ef4115cc624`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4883567b4bb0fc1fa52acd4cb857168ad41baa9654c83027dfbc914948097990`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 1.6 MB (1569690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad116d0fcf6cbbb125c7c50740f67eb330a3b288c01a2492a1faeb66262ec5b5`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:30eb4f014b0df465074ff89e278bb79bb2919c728865b5adc2c6c23200082c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebb6cc9a352a3ac41f3c5cdd006f2a690758b37d99ec0a54e74e8aa65a86aef`

```dockerfile
```

-	Layers:
	-	`sha256:8925509d70a772fbbcea0958493fae2fc014cc9d9cafe2afc19d2de0ede9d25e`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 2.7 MB (2680963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbbdbf33bccad2a44acdbfba5338fa4a218e802388289fde911052d7a3b8b30`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 13.4 KB (13418 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; arm variant v7

```console
$ docker pull hitch@sha256:981d450a3e81145a9b2130fe1c7dbe443a2eea38ab972e756aa3e3716b045355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28078165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144090bd5c4246795c40b8cc1e0997123d807d4c873a1d59fac30cdaa7de3049`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
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
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9c2aa502d43acbcb5595150f593e1a0efb15cd856419d09c0f1be5d981dfff`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 1.5 MB (1488591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e127634bebf3abf5444ea33fab4571e990ec450543485d0d886835048376ccdb`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:004b4069765b12a0d2adc95d51b9d45410849c9af6aa810484b4b78f0756e0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25eba83e05d9e2558a232d07ae49fe26c9a5018af842a460f55c137cc669f470`

```dockerfile
```

-	Layers:
	-	`sha256:5e91e859c9b01c135d7d5cceda113f8caa92c170592ce436e56f4cbd8d2cf581`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 2.7 MB (2683194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1c8f004fa7967294a167804dc0cac2fecfefa353171e717b765ae145610d0ec`  
		Last Modified: Tue, 23 Jul 2024 17:53:38 GMT  
		Size: 13.5 KB (13497 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:fa75d0ea0162e7206228236ad85d7d15ff505273ee0015cefca06eb7b4176df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31624473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59df3aa7896cf31e3f5a0dc59e0cb05461d995a394c7d2fe5c707afc2bd9c3b7`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f934bb8adda65d7f158f8c504468174b4e8b30dd16998bb715d13460c72487`  
		Last Modified: Tue, 23 Jul 2024 18:02:56 GMT  
		Size: 1.5 MB (1547947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82995ad423fbc7a98db968925112c88ee990c4ccce3e50353091ae79f8db00e4`  
		Last Modified: Tue, 23 Jul 2024 18:02:55 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:a73dbb5f3ad2edc9f18e01af81db961c928f153c776876d522818aa0305e90c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7456a191710babae6d9d3379d5079efad82b1f5b86bda1af033baa8ccc9701`

```dockerfile
```

-	Layers:
	-	`sha256:625a25d0461783c4afc3583811a1aacbacad0b67d3cc5c957781fa540b84ac39`  
		Last Modified: Tue, 23 Jul 2024 18:02:56 GMT  
		Size: 2.7 MB (2681226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:851a4b9b5477b11379ebc8427770cb8e1730529dade424cc1af5d052e45acad2`  
		Last Modified: Tue, 23 Jul 2024 18:02:55 GMT  
		Size: 13.7 KB (13740 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; 386

```console
$ docker pull hitch@sha256:637cb4e821c4601ba7f8589306abdcc278ceb540629d07511a26205f2ee546a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33987907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d66b1e16ff12161364c33b548eecfabe456c0deda623de2b00c0000dd0182c`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
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
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b334d2b26b3df7d9cbdd70f000a5c822ce4e7bb7066b74fb9031116dffa0e9c2`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 1.6 MB (1573655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dded04ace82dcdddba7b8b99a9c2b2cd1c00760df660a5654ccdf64faad1d616`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:565d9a35732e29ad5f72de9c4e0aa495204408f4acf7626a288d7d594857ec2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b497475d79dff7880f114285f4c0c5913c13ff4ab5fdad8cec24415c42d2660c`

```dockerfile
```

-	Layers:
	-	`sha256:0d912c72abe92dde4d8c7632ed173709b2f674c57b409daa521eae5ae42632ce`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 2.7 MB (2678086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337dae020c5431496b7a528cb6fbf11b4516ee309576895f215b6282a8ef8493`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 13.4 KB (13385 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; ppc64le

```console
$ docker pull hitch@sha256:97692cd5e86b5195cd960ede47c604faa873df60847065434fe5b55221a00ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36934052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd149623778b2443477f6eb5471cc83ea80aff40dc5c8073928c7e83c2bd11f`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
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
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daadd4be7446559c1170eaca7a01cfd46dfd1ec9319f4d038ecc80726c01df16`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 1.6 MB (1628405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5f8c11dcbedaf561050b71774d65ab300bec506c09cdc0c06ac19e5d8de8b`  
		Last Modified: Tue, 23 Jul 2024 17:15:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:db51106e83229bbe9cef11353b5c88ebdc5def9516cf6884f61e7a7c0894055d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b904ce56fd81e73cf9baa0a00b9bdc55f05c3c0cd89b40fc85bbb418c6b02a1`

```dockerfile
```

-	Layers:
	-	`sha256:520693713f87c110c79d828e280b7b46608507dbc13592156c87488a3950d93f`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 2.7 MB (2685293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be4b9240eb3a724b62c55728cdfaf0cd84810adb1610676f1ea8e1a58734478`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 13.5 KB (13463 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; s390x

```console
$ docker pull hitch@sha256:9ad9f59d1df7555a273c466fc16578784dc8d2bc3d2de5502d5afacbbfa5b35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31236664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7f61b597a013e007953f1026f56325114016d13f50270be0360432c7bc25f8`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
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
	-	`sha256:de4a305fc1af45cc7ae97020dfe639e8990f6d00b7e0ef222c4cdd720f0fc373`  
		Last Modified: Tue, 23 Jul 2024 02:33:12 GMT  
		Size: 29.7 MB (29669018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ad7a78b5b5d0fe5197110ddffe7968cd045a7944d897e6723083f9849631c1`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 1.6 MB (1567201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38710f5e1ec9096f8e9bffa426e0c75fbbe6e4f3568a1a6424720fec7874864`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:ff4969b45fae8337c40248720ca6f0a2cd44dcb9bf6e1a206f4a092137450497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d023046794e03598606f38e9e3ff72622c9f0a48937c7142fefe1a24e4e7ef3d`

```dockerfile
```

-	Layers:
	-	`sha256:52830f4dbc84668719e910e07b7980877f12c0ebf64f4d81ca200bf7a7b0910f`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 2.7 MB (2681168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e501c35fa58c72fcd61d817750f828b8e17e72a6bf3b6c9106fb85c9a7009e`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 13.4 KB (13419 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:1.8.0-1`

```console
$ docker pull hitch@sha256:e5fccf50546ab1724f3a7e958c504140fb466bf2d27fc4d90bc527b7dddb585f
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

### `hitch:1.8.0-1` - linux; amd64

```console
$ docker pull hitch@sha256:634b262073d168d62c44baf0ee8b6579ec1dc6399b673544adaa39dc2b677bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32998464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7dea6f1510ed8dd4ee69b4241944b010e43307ddc2979c92661ef4115cc624`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4883567b4bb0fc1fa52acd4cb857168ad41baa9654c83027dfbc914948097990`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 1.6 MB (1569690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad116d0fcf6cbbb125c7c50740f67eb330a3b288c01a2492a1faeb66262ec5b5`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:30eb4f014b0df465074ff89e278bb79bb2919c728865b5adc2c6c23200082c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebb6cc9a352a3ac41f3c5cdd006f2a690758b37d99ec0a54e74e8aa65a86aef`

```dockerfile
```

-	Layers:
	-	`sha256:8925509d70a772fbbcea0958493fae2fc014cc9d9cafe2afc19d2de0ede9d25e`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 2.7 MB (2680963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbbdbf33bccad2a44acdbfba5338fa4a218e802388289fde911052d7a3b8b30`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 13.4 KB (13418 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:981d450a3e81145a9b2130fe1c7dbe443a2eea38ab972e756aa3e3716b045355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28078165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144090bd5c4246795c40b8cc1e0997123d807d4c873a1d59fac30cdaa7de3049`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
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
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9c2aa502d43acbcb5595150f593e1a0efb15cd856419d09c0f1be5d981dfff`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 1.5 MB (1488591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e127634bebf3abf5444ea33fab4571e990ec450543485d0d886835048376ccdb`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:004b4069765b12a0d2adc95d51b9d45410849c9af6aa810484b4b78f0756e0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25eba83e05d9e2558a232d07ae49fe26c9a5018af842a460f55c137cc669f470`

```dockerfile
```

-	Layers:
	-	`sha256:5e91e859c9b01c135d7d5cceda113f8caa92c170592ce436e56f4cbd8d2cf581`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 2.7 MB (2683194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1c8f004fa7967294a167804dc0cac2fecfefa353171e717b765ae145610d0ec`  
		Last Modified: Tue, 23 Jul 2024 17:53:38 GMT  
		Size: 13.5 KB (13497 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:fa75d0ea0162e7206228236ad85d7d15ff505273ee0015cefca06eb7b4176df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31624473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59df3aa7896cf31e3f5a0dc59e0cb05461d995a394c7d2fe5c707afc2bd9c3b7`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f934bb8adda65d7f158f8c504468174b4e8b30dd16998bb715d13460c72487`  
		Last Modified: Tue, 23 Jul 2024 18:02:56 GMT  
		Size: 1.5 MB (1547947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82995ad423fbc7a98db968925112c88ee990c4ccce3e50353091ae79f8db00e4`  
		Last Modified: Tue, 23 Jul 2024 18:02:55 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:a73dbb5f3ad2edc9f18e01af81db961c928f153c776876d522818aa0305e90c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7456a191710babae6d9d3379d5079efad82b1f5b86bda1af033baa8ccc9701`

```dockerfile
```

-	Layers:
	-	`sha256:625a25d0461783c4afc3583811a1aacbacad0b67d3cc5c957781fa540b84ac39`  
		Last Modified: Tue, 23 Jul 2024 18:02:56 GMT  
		Size: 2.7 MB (2681226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:851a4b9b5477b11379ebc8427770cb8e1730529dade424cc1af5d052e45acad2`  
		Last Modified: Tue, 23 Jul 2024 18:02:55 GMT  
		Size: 13.7 KB (13740 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; 386

```console
$ docker pull hitch@sha256:637cb4e821c4601ba7f8589306abdcc278ceb540629d07511a26205f2ee546a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33987907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d66b1e16ff12161364c33b548eecfabe456c0deda623de2b00c0000dd0182c`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
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
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b334d2b26b3df7d9cbdd70f000a5c822ce4e7bb7066b74fb9031116dffa0e9c2`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 1.6 MB (1573655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dded04ace82dcdddba7b8b99a9c2b2cd1c00760df660a5654ccdf64faad1d616`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:565d9a35732e29ad5f72de9c4e0aa495204408f4acf7626a288d7d594857ec2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b497475d79dff7880f114285f4c0c5913c13ff4ab5fdad8cec24415c42d2660c`

```dockerfile
```

-	Layers:
	-	`sha256:0d912c72abe92dde4d8c7632ed173709b2f674c57b409daa521eae5ae42632ce`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 2.7 MB (2678086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337dae020c5431496b7a528cb6fbf11b4516ee309576895f215b6282a8ef8493`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 13.4 KB (13385 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; ppc64le

```console
$ docker pull hitch@sha256:97692cd5e86b5195cd960ede47c604faa873df60847065434fe5b55221a00ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36934052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd149623778b2443477f6eb5471cc83ea80aff40dc5c8073928c7e83c2bd11f`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
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
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daadd4be7446559c1170eaca7a01cfd46dfd1ec9319f4d038ecc80726c01df16`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 1.6 MB (1628405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5f8c11dcbedaf561050b71774d65ab300bec506c09cdc0c06ac19e5d8de8b`  
		Last Modified: Tue, 23 Jul 2024 17:15:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:db51106e83229bbe9cef11353b5c88ebdc5def9516cf6884f61e7a7c0894055d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b904ce56fd81e73cf9baa0a00b9bdc55f05c3c0cd89b40fc85bbb418c6b02a1`

```dockerfile
```

-	Layers:
	-	`sha256:520693713f87c110c79d828e280b7b46608507dbc13592156c87488a3950d93f`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 2.7 MB (2685293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be4b9240eb3a724b62c55728cdfaf0cd84810adb1610676f1ea8e1a58734478`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 13.5 KB (13463 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; s390x

```console
$ docker pull hitch@sha256:9ad9f59d1df7555a273c466fc16578784dc8d2bc3d2de5502d5afacbbfa5b35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31236664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7f61b597a013e007953f1026f56325114016d13f50270be0360432c7bc25f8`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
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
	-	`sha256:de4a305fc1af45cc7ae97020dfe639e8990f6d00b7e0ef222c4cdd720f0fc373`  
		Last Modified: Tue, 23 Jul 2024 02:33:12 GMT  
		Size: 29.7 MB (29669018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ad7a78b5b5d0fe5197110ddffe7968cd045a7944d897e6723083f9849631c1`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 1.6 MB (1567201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38710f5e1ec9096f8e9bffa426e0c75fbbe6e4f3568a1a6424720fec7874864`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:ff4969b45fae8337c40248720ca6f0a2cd44dcb9bf6e1a206f4a092137450497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d023046794e03598606f38e9e3ff72622c9f0a48937c7142fefe1a24e4e7ef3d`

```dockerfile
```

-	Layers:
	-	`sha256:52830f4dbc84668719e910e07b7980877f12c0ebf64f4d81ca200bf7a7b0910f`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 2.7 MB (2681168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e501c35fa58c72fcd61d817750f828b8e17e72a6bf3b6c9106fb85c9a7009e`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 13.4 KB (13419 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:latest`

```console
$ docker pull hitch@sha256:e5fccf50546ab1724f3a7e958c504140fb466bf2d27fc4d90bc527b7dddb585f
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
$ docker pull hitch@sha256:634b262073d168d62c44baf0ee8b6579ec1dc6399b673544adaa39dc2b677bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32998464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7dea6f1510ed8dd4ee69b4241944b010e43307ddc2979c92661ef4115cc624`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4883567b4bb0fc1fa52acd4cb857168ad41baa9654c83027dfbc914948097990`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 1.6 MB (1569690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad116d0fcf6cbbb125c7c50740f67eb330a3b288c01a2492a1faeb66262ec5b5`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:30eb4f014b0df465074ff89e278bb79bb2919c728865b5adc2c6c23200082c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebb6cc9a352a3ac41f3c5cdd006f2a690758b37d99ec0a54e74e8aa65a86aef`

```dockerfile
```

-	Layers:
	-	`sha256:8925509d70a772fbbcea0958493fae2fc014cc9d9cafe2afc19d2de0ede9d25e`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 2.7 MB (2680963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbbdbf33bccad2a44acdbfba5338fa4a218e802388289fde911052d7a3b8b30`  
		Last Modified: Tue, 23 Jul 2024 07:15:25 GMT  
		Size: 13.4 KB (13418 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm variant v7

```console
$ docker pull hitch@sha256:981d450a3e81145a9b2130fe1c7dbe443a2eea38ab972e756aa3e3716b045355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28078165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144090bd5c4246795c40b8cc1e0997123d807d4c873a1d59fac30cdaa7de3049`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
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
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9c2aa502d43acbcb5595150f593e1a0efb15cd856419d09c0f1be5d981dfff`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 1.5 MB (1488591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e127634bebf3abf5444ea33fab4571e990ec450543485d0d886835048376ccdb`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:004b4069765b12a0d2adc95d51b9d45410849c9af6aa810484b4b78f0756e0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25eba83e05d9e2558a232d07ae49fe26c9a5018af842a460f55c137cc669f470`

```dockerfile
```

-	Layers:
	-	`sha256:5e91e859c9b01c135d7d5cceda113f8caa92c170592ce436e56f4cbd8d2cf581`  
		Last Modified: Tue, 23 Jul 2024 17:53:39 GMT  
		Size: 2.7 MB (2683194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1c8f004fa7967294a167804dc0cac2fecfefa353171e717b765ae145610d0ec`  
		Last Modified: Tue, 23 Jul 2024 17:53:38 GMT  
		Size: 13.5 KB (13497 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:fa75d0ea0162e7206228236ad85d7d15ff505273ee0015cefca06eb7b4176df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31624473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59df3aa7896cf31e3f5a0dc59e0cb05461d995a394c7d2fe5c707afc2bd9c3b7`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f934bb8adda65d7f158f8c504468174b4e8b30dd16998bb715d13460c72487`  
		Last Modified: Tue, 23 Jul 2024 18:02:56 GMT  
		Size: 1.5 MB (1547947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82995ad423fbc7a98db968925112c88ee990c4ccce3e50353091ae79f8db00e4`  
		Last Modified: Tue, 23 Jul 2024 18:02:55 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:a73dbb5f3ad2edc9f18e01af81db961c928f153c776876d522818aa0305e90c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7456a191710babae6d9d3379d5079efad82b1f5b86bda1af033baa8ccc9701`

```dockerfile
```

-	Layers:
	-	`sha256:625a25d0461783c4afc3583811a1aacbacad0b67d3cc5c957781fa540b84ac39`  
		Last Modified: Tue, 23 Jul 2024 18:02:56 GMT  
		Size: 2.7 MB (2681226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:851a4b9b5477b11379ebc8427770cb8e1730529dade424cc1af5d052e45acad2`  
		Last Modified: Tue, 23 Jul 2024 18:02:55 GMT  
		Size: 13.7 KB (13740 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; 386

```console
$ docker pull hitch@sha256:637cb4e821c4601ba7f8589306abdcc278ceb540629d07511a26205f2ee546a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33987907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d66b1e16ff12161364c33b548eecfabe456c0deda623de2b00c0000dd0182c`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
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
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b334d2b26b3df7d9cbdd70f000a5c822ce4e7bb7066b74fb9031116dffa0e9c2`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 1.6 MB (1573655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dded04ace82dcdddba7b8b99a9c2b2cd1c00760df660a5654ccdf64faad1d616`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:565d9a35732e29ad5f72de9c4e0aa495204408f4acf7626a288d7d594857ec2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b497475d79dff7880f114285f4c0c5913c13ff4ab5fdad8cec24415c42d2660c`

```dockerfile
```

-	Layers:
	-	`sha256:0d912c72abe92dde4d8c7632ed173709b2f674c57b409daa521eae5ae42632ce`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 2.7 MB (2678086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337dae020c5431496b7a528cb6fbf11b4516ee309576895f215b6282a8ef8493`  
		Last Modified: Tue, 23 Jul 2024 06:16:04 GMT  
		Size: 13.4 KB (13385 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; ppc64le

```console
$ docker pull hitch@sha256:97692cd5e86b5195cd960ede47c604faa873df60847065434fe5b55221a00ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36934052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd149623778b2443477f6eb5471cc83ea80aff40dc5c8073928c7e83c2bd11f`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
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
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daadd4be7446559c1170eaca7a01cfd46dfd1ec9319f4d038ecc80726c01df16`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 1.6 MB (1628405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5f8c11dcbedaf561050b71774d65ab300bec506c09cdc0c06ac19e5d8de8b`  
		Last Modified: Tue, 23 Jul 2024 17:15:13 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:db51106e83229bbe9cef11353b5c88ebdc5def9516cf6884f61e7a7c0894055d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b904ce56fd81e73cf9baa0a00b9bdc55f05c3c0cd89b40fc85bbb418c6b02a1`

```dockerfile
```

-	Layers:
	-	`sha256:520693713f87c110c79d828e280b7b46608507dbc13592156c87488a3950d93f`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 2.7 MB (2685293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be4b9240eb3a724b62c55728cdfaf0cd84810adb1610676f1ea8e1a58734478`  
		Last Modified: Tue, 23 Jul 2024 17:15:09 GMT  
		Size: 13.5 KB (13463 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; s390x

```console
$ docker pull hitch@sha256:9ad9f59d1df7555a273c466fc16578784dc8d2bc3d2de5502d5afacbbfa5b35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31236664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7f61b597a013e007953f1026f56325114016d13f50270be0360432c7bc25f8`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Tue, 22 Aug 2023 15:19:07 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
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
	-	`sha256:de4a305fc1af45cc7ae97020dfe639e8990f6d00b7e0ef222c4cdd720f0fc373`  
		Last Modified: Tue, 23 Jul 2024 02:33:12 GMT  
		Size: 29.7 MB (29669018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ad7a78b5b5d0fe5197110ddffe7968cd045a7944d897e6723083f9849631c1`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 1.6 MB (1567201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38710f5e1ec9096f8e9bffa426e0c75fbbe6e4f3568a1a6424720fec7874864`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:ff4969b45fae8337c40248720ca6f0a2cd44dcb9bf6e1a206f4a092137450497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d023046794e03598606f38e9e3ff72622c9f0a48937c7142fefe1a24e4e7ef3d`

```dockerfile
```

-	Layers:
	-	`sha256:52830f4dbc84668719e910e07b7980877f12c0ebf64f4d81ca200bf7a7b0910f`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 2.7 MB (2681168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e501c35fa58c72fcd61d817750f828b8e17e72a6bf3b6c9106fb85c9a7009e`  
		Last Modified: Tue, 23 Jul 2024 16:33:19 GMT  
		Size: 13.4 KB (13419 bytes)  
		MIME: application/vnd.in-toto+json
