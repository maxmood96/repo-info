## `hitch:latest`

```console
$ docker pull hitch@sha256:d347bb997cc6aac86a42ad8a7c14ef5f0c7d8990f76975efb5fd7b045594be75
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
$ docker pull hitch@sha256:af245b9a5db4937b60b7a7ebe7a4d1bf1c9cda58eb827b036e26ef63d22b315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27327750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf430d9d22096d99deedf069911cea59e08e8ba5c138541ca8252fd710103b6`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:15 GMT
ARG SRCVER=1.8.0
# Tue, 07 Apr 2026 01:18:15 GMT
ARG PKGVER=1
# Tue, 07 Apr 2026 01:18:15 GMT
ARG DISTVER=bullseye
# Tue, 07 Apr 2026 01:18:15 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 07 Apr 2026 01:18:15 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 07 Apr 2026 01:18:15 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 07 Apr 2026 01:18:15 GMT
WORKDIR /etc/hitch
# Tue, 07 Apr 2026 01:18:15 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:18:15 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 07 Apr 2026 01:18:15 GMT
EXPOSE map[443/tcp:{}]
# Tue, 07 Apr 2026 01:18:15 GMT
CMD []
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8baf91025a3580903beb18cc59a45416d9e667a195350c67fd6b78d76a182c8a`  
		Last Modified: Tue, 07 Apr 2026 01:18:22 GMT  
		Size: 3.4 MB (3385844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9aa9989dc0839878976cf4495370d6eb0448f5e860ad8a1475b6fd8e4f649a`  
		Last Modified: Tue, 07 Apr 2026 01:18:21 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:bf08d351cec66f9c8283a2cf12fad6f290ea79bfebcc1d11593cbb39c4e06f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2547257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a3de56dba152c99054302e437a4198e4c6d34f3f00b9d125a7b9230f54e1dc`

```dockerfile
```

-	Layers:
	-	`sha256:67ac7631bdc78b7d76607bca6e57c4d6421edea6e9c414e0d1124598c96328d8`  
		Last Modified: Tue, 07 Apr 2026 01:18:22 GMT  
		Size: 2.5 MB (2533587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74bdde4a0cdbcbcf4db6a11d8eacfd7816a86c2b4689349312807c0d6e4f4fe1`  
		Last Modified: Tue, 07 Apr 2026 01:18:21 GMT  
		Size: 13.7 KB (13670 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:669772aa2940bd2ed649af186a651acf9682fd00456e837301bc8e7ae26c1d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31989219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bac412a9adef828b8a60037689684eb2a369df57fc6f321c7a36a949878c2f`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:22:27 GMT
ARG SRCVER=1.8.0
# Tue, 07 Apr 2026 01:22:27 GMT
ARG PKGVER=1
# Tue, 07 Apr 2026 01:22:27 GMT
ARG DISTVER=bullseye
# Tue, 07 Apr 2026 01:22:27 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 07 Apr 2026 01:22:27 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 07 Apr 2026 01:22:27 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 07 Apr 2026 01:22:27 GMT
WORKDIR /etc/hitch
# Tue, 07 Apr 2026 01:22:27 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:22:27 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 07 Apr 2026 01:22:27 GMT
EXPOSE map[443/tcp:{}]
# Tue, 07 Apr 2026 01:22:27 GMT
CMD []
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89721740df1d13f0f6562a60c6757f96df217aa9e25f6da75d910252b6695a99`  
		Last Modified: Tue, 07 Apr 2026 01:22:34 GMT  
		Size: 3.9 MB (3872606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50121c2753739e26f5437fab24a6423c0740662e93ec580b249cc4679eeacca8`  
		Last Modified: Tue, 07 Apr 2026 01:22:33 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:57c14b1c0d51e160fef916f7764501d6092fa77a4f042cadfc6c9f158bb889a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32760223a8df278412a1652b8b3c30bbb980a04d3a1c474246e66fba38d2de25`

```dockerfile
```

-	Layers:
	-	`sha256:505e2f0bd0e7c71cb00d86c10209a27409d4c57d0045cc88679c5558932aaa5f`  
		Last Modified: Tue, 07 Apr 2026 01:22:34 GMT  
		Size: 2.5 MB (2531625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce4ee5a267c5f938f50b3d10ad9081bf0101457d1a7216d897f5168d9bac18b8`  
		Last Modified: Tue, 07 Apr 2026 01:22:33 GMT  
		Size: 13.7 KB (13698 bytes)  
		MIME: application/vnd.in-toto+json

### `hitch:latest` - linux; 386

```console
$ docker pull hitch@sha256:917c52c0139f82af957ef178b7f7237d10909c3a31ee52074da8bb7ac63edc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33239409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00779cb64629837374efb9c4ab3b16b0e849d40e845f9a4821bb709cca136608`
-	Entrypoint: `["docker-hitch-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:56 GMT
ARG SRCVER=1.8.0
# Tue, 07 Apr 2026 01:18:56 GMT
ARG PKGVER=1
# Tue, 07 Apr 2026 01:18:56 GMT
ARG DISTVER=bullseye
# Tue, 07 Apr 2026 01:18:56 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 07 Apr 2026 01:18:56 GMT
ARG SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
# Tue, 07 Apr 2026 01:18:56 GMT
# ARGS: SRCVER=1.8.0 PKGVER=1 DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 SHASUM=62b3554d668c9d17382415db10898bf661ee76343e4ee364f904457efda6cb1eeee7cb81d7a3897734024812b64b1c0e2dc305605706d81a0c1f6030508bf7e2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y --no-install-recommends install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir" # buildkit
# Tue, 07 Apr 2026 01:18:56 GMT
WORKDIR /etc/hitch
# Tue, 07 Apr 2026 01:18:56 GMT
COPY docker-hitch-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:18:56 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 07 Apr 2026 01:18:56 GMT
EXPOSE map[443/tcp:{}]
# Tue, 07 Apr 2026 01:18:56 GMT
CMD []
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1958b3e26ad065624baeb77279ab467df86ec099fc8d3dd9132fd2c7806e096e`  
		Last Modified: Tue, 07 Apr 2026 01:19:02 GMT  
		Size: 4.0 MB (4017199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e007b638e73123ffb08f473529c3470bcd64a2e71551caa0348a6e0b73ff5d`  
		Last Modified: Tue, 07 Apr 2026 01:19:02 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hitch:latest` - unknown; unknown

```console
$ docker pull hitch@sha256:00a97b74353bb0735c8d69ac8c37a05248f0053263acbccb2c441d4ad788a906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a590c8a724f2a13c16575022aeed9648efd61f6210e9e38cd2f1a39e088d919`

```dockerfile
```

-	Layers:
	-	`sha256:4446a834bc58ddb39b3792f22d5a95bd1e60132e23e9ee981f54fe69bad29387`  
		Last Modified: Tue, 07 Apr 2026 01:19:02 GMT  
		Size: 2.5 MB (2528531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca0302c13df6a2fc2fa15aa1f85d6d5b86224ecfda02971b05f2eda10e8dc765`  
		Last Modified: Tue, 07 Apr 2026 01:19:02 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json
