<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `hitch`

-	[`hitch:1`](#hitch1)
-	[`hitch:1.8`](#hitch18)
-	[`hitch:1.8.0`](#hitch180)
-	[`hitch:1.8.0-1`](#hitch180-1)
-	[`hitch:latest`](#hitchlatest)

## `hitch:1`

```console
$ docker pull hitch@sha256:41adecff316882f40c871cd1973c67d0096464ee5da1248766dcace99468ae96
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

### `hitch:1` - unknown; unknown

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

### `hitch:1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:f255de6b3f0e93b685f382e08d9bf6c9f94ce269d7cc7ada48360709c2656e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27319354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6066c78e772ff2c72d2876d5ef18b9036231e44225eceba427a9eb093494a685`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:48 GMT
ARG SRCVER=1.8.0
# Mon, 29 Dec 2025 23:16:48 GMT
ARG PKGVER=1
# Mon, 29 Dec 2025 23:16:48 GMT
ARG DISTVER=bullseye
# Mon, 29 Dec 2025 23:16:48 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 29 Dec 2025 23:16:48 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
WORKDIR /etc/hitch
# Mon, 29 Dec 2025 23:16:49 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:49 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 29 Dec 2025 23:16:49 GMT
EXPOSE map[443/tcp:{}]
# Mon, 29 Dec 2025 23:16:49 GMT
CMD []
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b97e0a25f3464b5b2bfacd1091d2965d4a32115e0976a5fa1ea7daabb6e607`  
		Last Modified: Mon, 29 Dec 2025 23:17:02 GMT  
		Size: 3.4 MB (3384857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382609cf608109d94579883040aa5147358c87a53abd8056d768de2e1b580528`  
		Last Modified: Mon, 29 Dec 2025 23:17:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:84e9b16efede565705672eaba05d25e6322d00e899610c831f1ddbb8d75103e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2547247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c1c40c73ac2e499eee3fdf162ced1b7af68079eed879b8db20d98408919d8f`

```dockerfile
```

-	Layers:
	-	`sha256:c331516a8268af5220cd41193482cecd00be6c9b9086e8d53b96d6fadfd84f96`  
		Last Modified: Tue, 30 Dec 2025 04:46:41 GMT  
		Size: 2.5 MB (2533577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06ebfff45dae9dd8ebd5683436a697fd66e3c5179f361a992d5d056b8340ef33`  
		Last Modified: Tue, 30 Dec 2025 04:46:41 GMT  
		Size: 13.7 KB (13670 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1` - linux; arm64 variant v8

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

### `hitch:1` - unknown; unknown

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

### `hitch:1` - linux; 386

```console
$ docker pull hitch@sha256:6824a0dac0fac7e3df73ba805c93b14e0f587ee2b234d4f128ae031f4d122f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33226209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc6099f762e5c4845ac04cee1783c9370bf26beb58737da76fc102cc60e1ab0`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:32 GMT
ARG SRCVER=1.8.0
# Mon, 29 Dec 2025 23:16:32 GMT
ARG PKGVER=1
# Mon, 29 Dec 2025 23:16:32 GMT
ARG DISTVER=bullseye
# Mon, 29 Dec 2025 23:16:32 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 29 Dec 2025 23:16:32 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 29 Dec 2025 23:16:32 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 29 Dec 2025 23:16:32 GMT
WORKDIR /etc/hitch
# Mon, 29 Dec 2025 23:16:32 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:32 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 29 Dec 2025 23:16:32 GMT
EXPOSE map[443/tcp:{}]
# Mon, 29 Dec 2025 23:16:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806584feaff2f52a4517342638bc04a5a59cbfe09f308772c407f8602d574132`  
		Last Modified: Mon, 29 Dec 2025 23:16:46 GMT  
		Size: 4.0 MB (4015993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38833e89f5684a4bdd79544c1e3ec5d1a4735a91001143c87d53695a7a797f5`  
		Last Modified: Mon, 29 Dec 2025 23:16:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1` - unknown; unknown

```console
$ docker pull hitch@sha256:36a843a8c4df8bb111181bdaf627d85a77130b9cf0c9c4334d2df2a3260a44fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d74ca66d9efda3d40cfee79cea010ad56862ef118c42b3d25da6334b7f320ad`

```dockerfile
```

-	Layers:
	-	`sha256:9db033fb966cc53c22ed0c9ebf2ebc457aebf831aee790ec0ed773efda39ceb2`  
		Last Modified: Tue, 30 Dec 2025 04:46:47 GMT  
		Size: 2.5 MB (2528521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7414bee4507eb97fd6a6f9b182cecdcb5b364d076fc4a52acb964dc6827bc56d`  
		Last Modified: Tue, 30 Dec 2025 04:46:48 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:1.8`

```console
$ docker pull hitch@sha256:41adecff316882f40c871cd1973c67d0096464ee5da1248766dcace99468ae96
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

### `hitch:1.8` - unknown; unknown

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

### `hitch:1.8` - linux; arm variant v7

```console
$ docker pull hitch@sha256:f255de6b3f0e93b685f382e08d9bf6c9f94ce269d7cc7ada48360709c2656e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27319354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6066c78e772ff2c72d2876d5ef18b9036231e44225eceba427a9eb093494a685`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:48 GMT
ARG SRCVER=1.8.0
# Mon, 29 Dec 2025 23:16:48 GMT
ARG PKGVER=1
# Mon, 29 Dec 2025 23:16:48 GMT
ARG DISTVER=bullseye
# Mon, 29 Dec 2025 23:16:48 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 29 Dec 2025 23:16:48 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
WORKDIR /etc/hitch
# Mon, 29 Dec 2025 23:16:49 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:49 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 29 Dec 2025 23:16:49 GMT
EXPOSE map[443/tcp:{}]
# Mon, 29 Dec 2025 23:16:49 GMT
CMD []
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b97e0a25f3464b5b2bfacd1091d2965d4a32115e0976a5fa1ea7daabb6e607`  
		Last Modified: Mon, 29 Dec 2025 23:17:02 GMT  
		Size: 3.4 MB (3384857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382609cf608109d94579883040aa5147358c87a53abd8056d768de2e1b580528`  
		Last Modified: Mon, 29 Dec 2025 23:17:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:84e9b16efede565705672eaba05d25e6322d00e899610c831f1ddbb8d75103e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2547247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c1c40c73ac2e499eee3fdf162ced1b7af68079eed879b8db20d98408919d8f`

```dockerfile
```

-	Layers:
	-	`sha256:c331516a8268af5220cd41193482cecd00be6c9b9086e8d53b96d6fadfd84f96`  
		Last Modified: Tue, 30 Dec 2025 04:46:41 GMT  
		Size: 2.5 MB (2533577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06ebfff45dae9dd8ebd5683436a697fd66e3c5179f361a992d5d056b8340ef33`  
		Last Modified: Tue, 30 Dec 2025 04:46:41 GMT  
		Size: 13.7 KB (13670 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8` - linux; arm64 variant v8

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

### `hitch:1.8` - unknown; unknown

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

### `hitch:1.8` - linux; 386

```console
$ docker pull hitch@sha256:6824a0dac0fac7e3df73ba805c93b14e0f587ee2b234d4f128ae031f4d122f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33226209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc6099f762e5c4845ac04cee1783c9370bf26beb58737da76fc102cc60e1ab0`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:32 GMT
ARG SRCVER=1.8.0
# Mon, 29 Dec 2025 23:16:32 GMT
ARG PKGVER=1
# Mon, 29 Dec 2025 23:16:32 GMT
ARG DISTVER=bullseye
# Mon, 29 Dec 2025 23:16:32 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 29 Dec 2025 23:16:32 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 29 Dec 2025 23:16:32 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 29 Dec 2025 23:16:32 GMT
WORKDIR /etc/hitch
# Mon, 29 Dec 2025 23:16:32 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:32 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 29 Dec 2025 23:16:32 GMT
EXPOSE map[443/tcp:{}]
# Mon, 29 Dec 2025 23:16:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806584feaff2f52a4517342638bc04a5a59cbfe09f308772c407f8602d574132`  
		Last Modified: Mon, 29 Dec 2025 23:16:46 GMT  
		Size: 4.0 MB (4015993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38833e89f5684a4bdd79544c1e3ec5d1a4735a91001143c87d53695a7a797f5`  
		Last Modified: Mon, 29 Dec 2025 23:16:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8` - unknown; unknown

```console
$ docker pull hitch@sha256:36a843a8c4df8bb111181bdaf627d85a77130b9cf0c9c4334d2df2a3260a44fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d74ca66d9efda3d40cfee79cea010ad56862ef118c42b3d25da6334b7f320ad`

```dockerfile
```

-	Layers:
	-	`sha256:9db033fb966cc53c22ed0c9ebf2ebc457aebf831aee790ec0ed773efda39ceb2`  
		Last Modified: Tue, 30 Dec 2025 04:46:47 GMT  
		Size: 2.5 MB (2528521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7414bee4507eb97fd6a6f9b182cecdcb5b364d076fc4a52acb964dc6827bc56d`  
		Last Modified: Tue, 30 Dec 2025 04:46:48 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:1.8.0`

```console
$ docker pull hitch@sha256:41adecff316882f40c871cd1973c67d0096464ee5da1248766dcace99468ae96
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

### `hitch:1.8.0` - unknown; unknown

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

### `hitch:1.8.0` - linux; arm variant v7

```console
$ docker pull hitch@sha256:f255de6b3f0e93b685f382e08d9bf6c9f94ce269d7cc7ada48360709c2656e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27319354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6066c78e772ff2c72d2876d5ef18b9036231e44225eceba427a9eb093494a685`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:48 GMT
ARG SRCVER=1.8.0
# Mon, 29 Dec 2025 23:16:48 GMT
ARG PKGVER=1
# Mon, 29 Dec 2025 23:16:48 GMT
ARG DISTVER=bullseye
# Mon, 29 Dec 2025 23:16:48 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 29 Dec 2025 23:16:48 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
WORKDIR /etc/hitch
# Mon, 29 Dec 2025 23:16:49 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:49 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 29 Dec 2025 23:16:49 GMT
EXPOSE map[443/tcp:{}]
# Mon, 29 Dec 2025 23:16:49 GMT
CMD []
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b97e0a25f3464b5b2bfacd1091d2965d4a32115e0976a5fa1ea7daabb6e607`  
		Last Modified: Mon, 29 Dec 2025 23:17:02 GMT  
		Size: 3.4 MB (3384857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382609cf608109d94579883040aa5147358c87a53abd8056d768de2e1b580528`  
		Last Modified: Mon, 29 Dec 2025 23:17:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:84e9b16efede565705672eaba05d25e6322d00e899610c831f1ddbb8d75103e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2547247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c1c40c73ac2e499eee3fdf162ced1b7af68079eed879b8db20d98408919d8f`

```dockerfile
```

-	Layers:
	-	`sha256:c331516a8268af5220cd41193482cecd00be6c9b9086e8d53b96d6fadfd84f96`  
		Last Modified: Tue, 30 Dec 2025 04:46:41 GMT  
		Size: 2.5 MB (2533577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06ebfff45dae9dd8ebd5683436a697fd66e3c5179f361a992d5d056b8340ef33`  
		Last Modified: Tue, 30 Dec 2025 04:46:41 GMT  
		Size: 13.7 KB (13670 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0` - linux; arm64 variant v8

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

### `hitch:1.8.0` - unknown; unknown

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

### `hitch:1.8.0` - linux; 386

```console
$ docker pull hitch@sha256:6824a0dac0fac7e3df73ba805c93b14e0f587ee2b234d4f128ae031f4d122f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33226209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc6099f762e5c4845ac04cee1783c9370bf26beb58737da76fc102cc60e1ab0`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:32 GMT
ARG SRCVER=1.8.0
# Mon, 29 Dec 2025 23:16:32 GMT
ARG PKGVER=1
# Mon, 29 Dec 2025 23:16:32 GMT
ARG DISTVER=bullseye
# Mon, 29 Dec 2025 23:16:32 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 29 Dec 2025 23:16:32 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 29 Dec 2025 23:16:32 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 29 Dec 2025 23:16:32 GMT
WORKDIR /etc/hitch
# Mon, 29 Dec 2025 23:16:32 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:32 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 29 Dec 2025 23:16:32 GMT
EXPOSE map[443/tcp:{}]
# Mon, 29 Dec 2025 23:16:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806584feaff2f52a4517342638bc04a5a59cbfe09f308772c407f8602d574132`  
		Last Modified: Mon, 29 Dec 2025 23:16:46 GMT  
		Size: 4.0 MB (4015993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38833e89f5684a4bdd79544c1e3ec5d1a4735a91001143c87d53695a7a797f5`  
		Last Modified: Mon, 29 Dec 2025 23:16:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0` - unknown; unknown

```console
$ docker pull hitch@sha256:36a843a8c4df8bb111181bdaf627d85a77130b9cf0c9c4334d2df2a3260a44fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d74ca66d9efda3d40cfee79cea010ad56862ef118c42b3d25da6334b7f320ad`

```dockerfile
```

-	Layers:
	-	`sha256:9db033fb966cc53c22ed0c9ebf2ebc457aebf831aee790ec0ed773efda39ceb2`  
		Last Modified: Tue, 30 Dec 2025 04:46:47 GMT  
		Size: 2.5 MB (2528521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7414bee4507eb97fd6a6f9b182cecdcb5b364d076fc4a52acb964dc6827bc56d`  
		Last Modified: Tue, 30 Dec 2025 04:46:48 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:1.8.0-1`

```console
$ docker pull hitch@sha256:41adecff316882f40c871cd1973c67d0096464ee5da1248766dcace99468ae96
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

### `hitch:1.8.0-1` - unknown; unknown

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

### `hitch:1.8.0-1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:f255de6b3f0e93b685f382e08d9bf6c9f94ce269d7cc7ada48360709c2656e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27319354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6066c78e772ff2c72d2876d5ef18b9036231e44225eceba427a9eb093494a685`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:48 GMT
ARG SRCVER=1.8.0
# Mon, 29 Dec 2025 23:16:48 GMT
ARG PKGVER=1
# Mon, 29 Dec 2025 23:16:48 GMT
ARG DISTVER=bullseye
# Mon, 29 Dec 2025 23:16:48 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 29 Dec 2025 23:16:48 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
WORKDIR /etc/hitch
# Mon, 29 Dec 2025 23:16:49 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:49 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 29 Dec 2025 23:16:49 GMT
EXPOSE map[443/tcp:{}]
# Mon, 29 Dec 2025 23:16:49 GMT
CMD []
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b97e0a25f3464b5b2bfacd1091d2965d4a32115e0976a5fa1ea7daabb6e607`  
		Last Modified: Mon, 29 Dec 2025 23:17:02 GMT  
		Size: 3.4 MB (3384857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382609cf608109d94579883040aa5147358c87a53abd8056d768de2e1b580528`  
		Last Modified: Mon, 29 Dec 2025 23:17:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:84e9b16efede565705672eaba05d25e6322d00e899610c831f1ddbb8d75103e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2547247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c1c40c73ac2e499eee3fdf162ced1b7af68079eed879b8db20d98408919d8f`

```dockerfile
```

-	Layers:
	-	`sha256:c331516a8268af5220cd41193482cecd00be6c9b9086e8d53b96d6fadfd84f96`  
		Last Modified: Tue, 30 Dec 2025 04:46:41 GMT  
		Size: 2.5 MB (2533577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06ebfff45dae9dd8ebd5683436a697fd66e3c5179f361a992d5d056b8340ef33`  
		Last Modified: Tue, 30 Dec 2025 04:46:41 GMT  
		Size: 13.7 KB (13670 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:1.8.0-1` - linux; arm64 variant v8

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

### `hitch:1.8.0-1` - unknown; unknown

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

### `hitch:1.8.0-1` - linux; 386

```console
$ docker pull hitch@sha256:6824a0dac0fac7e3df73ba805c93b14e0f587ee2b234d4f128ae031f4d122f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33226209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc6099f762e5c4845ac04cee1783c9370bf26beb58737da76fc102cc60e1ab0`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:32 GMT
ARG SRCVER=1.8.0
# Mon, 29 Dec 2025 23:16:32 GMT
ARG PKGVER=1
# Mon, 29 Dec 2025 23:16:32 GMT
ARG DISTVER=bullseye
# Mon, 29 Dec 2025 23:16:32 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 29 Dec 2025 23:16:32 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 29 Dec 2025 23:16:32 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 29 Dec 2025 23:16:32 GMT
WORKDIR /etc/hitch
# Mon, 29 Dec 2025 23:16:32 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:32 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 29 Dec 2025 23:16:32 GMT
EXPOSE map[443/tcp:{}]
# Mon, 29 Dec 2025 23:16:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806584feaff2f52a4517342638bc04a5a59cbfe09f308772c407f8602d574132`  
		Last Modified: Mon, 29 Dec 2025 23:16:46 GMT  
		Size: 4.0 MB (4015993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38833e89f5684a4bdd79544c1e3ec5d1a4735a91001143c87d53695a7a797f5`  
		Last Modified: Mon, 29 Dec 2025 23:16:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:1.8.0-1` - unknown; unknown

```console
$ docker pull hitch@sha256:36a843a8c4df8bb111181bdaf627d85a77130b9cf0c9c4334d2df2a3260a44fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d74ca66d9efda3d40cfee79cea010ad56862ef118c42b3d25da6334b7f320ad`

```dockerfile
```

-	Layers:
	-	`sha256:9db033fb966cc53c22ed0c9ebf2ebc457aebf831aee790ec0ed773efda39ceb2`  
		Last Modified: Tue, 30 Dec 2025 04:46:47 GMT  
		Size: 2.5 MB (2528521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7414bee4507eb97fd6a6f9b182cecdcb5b364d076fc4a52acb964dc6827bc56d`  
		Last Modified: Tue, 30 Dec 2025 04:46:48 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

## `hitch:latest`

```console
$ docker pull hitch@sha256:41adecff316882f40c871cd1973c67d0096464ee5da1248766dcace99468ae96
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
$ docker pull hitch@sha256:f255de6b3f0e93b685f382e08d9bf6c9f94ce269d7cc7ada48360709c2656e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27319354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6066c78e772ff2c72d2876d5ef18b9036231e44225eceba427a9eb093494a685`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:48 GMT
ARG SRCVER=1.8.0
# Mon, 29 Dec 2025 23:16:48 GMT
ARG PKGVER=1
# Mon, 29 Dec 2025 23:16:48 GMT
ARG DISTVER=bullseye
# Mon, 29 Dec 2025 23:16:48 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 29 Dec 2025 23:16:48 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
WORKDIR /etc/hitch
# Mon, 29 Dec 2025 23:16:49 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:49 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 29 Dec 2025 23:16:49 GMT
EXPOSE map[443/tcp:{}]
# Mon, 29 Dec 2025 23:16:49 GMT
CMD []
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b97e0a25f3464b5b2bfacd1091d2965d4a32115e0976a5fa1ea7daabb6e607`  
		Last Modified: Mon, 29 Dec 2025 23:17:02 GMT  
		Size: 3.4 MB (3384857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382609cf608109d94579883040aa5147358c87a53abd8056d768de2e1b580528`  
		Last Modified: Mon, 29 Dec 2025 23:17:02 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:84e9b16efede565705672eaba05d25e6322d00e899610c831f1ddbb8d75103e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2547247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c1c40c73ac2e499eee3fdf162ced1b7af68079eed879b8db20d98408919d8f`

```dockerfile
```

-	Layers:
	-	`sha256:c331516a8268af5220cd41193482cecd00be6c9b9086e8d53b96d6fadfd84f96`  
		Last Modified: Tue, 30 Dec 2025 04:46:41 GMT  
		Size: 2.5 MB (2533577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06ebfff45dae9dd8ebd5683436a697fd66e3c5179f361a992d5d056b8340ef33`  
		Last Modified: Tue, 30 Dec 2025 04:46:41 GMT  
		Size: 13.7 KB (13670 bytes)  
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
$ docker pull hitch@sha256:6824a0dac0fac7e3df73ba805c93b14e0f587ee2b234d4f128ae031f4d122f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33226209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc6099f762e5c4845ac04cee1783c9370bf26beb58737da76fc102cc60e1ab0`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:32 GMT
ARG SRCVER=1.8.0
# Mon, 29 Dec 2025 23:16:32 GMT
ARG PKGVER=1
# Mon, 29 Dec 2025 23:16:32 GMT
ARG DISTVER=bullseye
# Mon, 29 Dec 2025 23:16:32 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 29 Dec 2025 23:16:32 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Mon, 29 Dec 2025 23:16:32 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Mon, 29 Dec 2025 23:16:32 GMT
WORKDIR /etc/hitch
# Mon, 29 Dec 2025 23:16:32 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:32 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 29 Dec 2025 23:16:32 GMT
EXPOSE map[443/tcp:{}]
# Mon, 29 Dec 2025 23:16:32 GMT
CMD []
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806584feaff2f52a4517342638bc04a5a59cbfe09f308772c407f8602d574132`  
		Last Modified: Mon, 29 Dec 2025 23:16:46 GMT  
		Size: 4.0 MB (4015993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38833e89f5684a4bdd79544c1e3ec5d1a4735a91001143c87d53695a7a797f5`  
		Last Modified: Mon, 29 Dec 2025 23:16:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:36a843a8c4df8bb111181bdaf627d85a77130b9cf0c9c4334d2df2a3260a44fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d74ca66d9efda3d40cfee79cea010ad56862ef118c42b3d25da6334b7f320ad`

```dockerfile
```

-	Layers:
	-	`sha256:9db033fb966cc53c22ed0c9ebf2ebc457aebf831aee790ec0ed773efda39ceb2`  
		Last Modified: Tue, 30 Dec 2025 04:46:47 GMT  
		Size: 2.5 MB (2528521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7414bee4507eb97fd6a6f9b182cecdcb5b364d076fc4a52acb964dc6827bc56d`  
		Last Modified: Tue, 30 Dec 2025 04:46:48 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json
