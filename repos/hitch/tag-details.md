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
$ docker pull hitch@sha256:2914c4c32db343875ad37f8ff10d29c6b42c2e569092d987184be52853c0cd51
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
$ docker pull hitch@sha256:36d995e4c365800b5c06add5c708d87d502069fea394c1d621e107804cc611cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33047349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31eaa012aff9da55a8ee56277169c8165d45a24d920c94c24e03018c7a8bb497`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:52:47 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 03:52:47 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 03:52:47 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 03:52:47 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 03:52:47 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 03:55:09 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 03:55:09 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 03:55:09 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 03:55:09 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 03:55:09 GMT
EXPOSE 443
# Tue, 25 Oct 2022 03:55:09 GMT
CMD []
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb58d7c4ae58e46e9f7f3a133a63fbbeb7fbbbb32e33966f5154e47c3ceec12`  
		Last Modified: Tue, 25 Oct 2022 03:57:30 GMT  
		Size: 1.6 MB (1626893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf6c8e8f72cac1af4a352a706377c56b7874956cf78cc69b2497b88a77e5352`  
		Last Modified: Tue, 25 Oct 2022 03:57:29 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7e5243c2e7681a7975d54b7188512f87cc0cd96400bd7607e73bfae4c04c32b1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28125419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec155d6e7d7ca5dd6520af2e4b3da7bf3555ede0850d6e151949c3fdcd6cc908`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 13:20:44 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 13:20:44 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 13:20:44 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 13:20:44 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 13:20:44 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 13:22:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 13:22:38 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 13:22:38 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 13:22:38 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 13:22:38 GMT
EXPOSE 443
# Tue, 25 Oct 2022 13:22:38 GMT
CMD []
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2560f5c440bcb344e07b93f0c453a8556e43c63bdd2eb54f6ac9188019b84cfc`  
		Last Modified: Tue, 25 Oct 2022 13:25:17 GMT  
		Size: 1.5 MB (1545709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103a95fdd02870ff462a20b0a7fea3fb250c528613536827c3f968e7d72d4ae`  
		Last Modified: Tue, 25 Oct 2022 13:25:17 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:e5ba13441f1a7085b9fea5024970ea2f370c6c8d61f0b1f8bbe9fe4e4be6511b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31668403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dface7840d899a8d9a685768e01d1e52a0708ff895d95d8a5cab70776066b5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:21:08 GMT
ARG SRCVER=1.7.3
# Tue, 15 Nov 2022 06:21:08 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 06:21:08 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 06:21:08 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 06:21:08 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 15 Nov 2022 06:23:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 06:23:37 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 06:23:38 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:23:38 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 06:23:38 GMT
EXPOSE 443
# Tue, 15 Nov 2022 06:23:38 GMT
CMD []
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313592145e823db6cb42dcfc2b587a67f1ab9657dd998105888b98a44c7704ac`  
		Last Modified: Tue, 15 Nov 2022 06:25:35 GMT  
		Size: 1.6 MB (1607381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0604703f3796f0b2b9605adee33e12d5c4112761a0001ae6518301e8f33f51f`  
		Last Modified: Tue, 15 Nov 2022 06:25:35 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; 386

```console
$ docker pull hitch@sha256:63b2fa866cb3b80aea85010b644c541723bcc1192d7ca41c159e910afa0ccea7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34027295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fde1440811f3f87556e6c3a840dafa6dcbd31db3bd7611372e2267b73b49c6b`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 02:22:34 GMT
ADD file:14adaece72e410cf04ac21a101e5b530aab1d5e5a189a2be72d195ec0ac5e6d4 in / 
# Tue, 25 Oct 2022 02:22:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:05:58 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 07:05:58 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 07:05:59 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 07:06:00 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 07:06:01 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 07:07:46 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 07:07:46 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 07:07:48 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:07:48 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 07:07:49 GMT
EXPOSE 443
# Tue, 25 Oct 2022 07:07:50 GMT
CMD []
```

-	Layers:
	-	`sha256:3c83067056c0f1bc4e162249831ac686f3a9a9c64c5366b903581580de8fcac2`  
		Last Modified: Tue, 25 Oct 2022 02:28:26 GMT  
		Size: 32.4 MB (32396384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a23a52a14eac897ff94c5663255f63ac00f47e3f92d56ce150927369a540f3`  
		Last Modified: Tue, 25 Oct 2022 07:08:48 GMT  
		Size: 1.6 MB (1630494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743da65dbf1956a87b5553dab51ceb17026da945adc6ea0d618c2786e93a7bd5`  
		Last Modified: Tue, 25 Oct 2022 07:08:47 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; ppc64le

```console
$ docker pull hitch@sha256:6ecf72a31dd4fcf3206c47608bdfc4f15eec1759d52cf3377f28420a084a946c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36977221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176ea8122edd48dc36abfbae685be31a83c0e2f78408178eb1fdf8b762cf0807`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:38:49 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 07:38:50 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 07:38:50 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 07:38:50 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 07:38:50 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 07:43:12 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 07:43:13 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 07:43:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:43:13 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 07:43:13 GMT
EXPOSE 443
# Tue, 25 Oct 2022 07:43:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9b139b300fbd61f2373a116840d3fc190ae40bde3e6fa0b5acfbe59b4d9533`  
		Last Modified: Tue, 25 Oct 2022 07:47:29 GMT  
		Size: 1.7 MB (1686718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5121dc1d0d1e79aa369638f89f421a8ae8c417002e27c91d5f1f59364431615d`  
		Last Modified: Tue, 25 Oct 2022 07:47:28 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1` - linux; s390x

```console
$ docker pull hitch@sha256:1ab9c81e5b9627e31ba303f1433b2e80d5189f1a988450a43c12b67372c7a395
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31268285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c62498018939442bf71e27b8fc3d99033db65a84a675110eeb3170766a8e327`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:28:17 GMT
ARG SRCVER=1.7.3
# Tue, 15 Nov 2022 07:28:18 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 07:28:18 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 07:28:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 07:28:19 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 15 Nov 2022 07:32:11 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 07:32:11 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 07:32:11 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 07:32:12 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 07:32:12 GMT
EXPOSE 443
# Tue, 15 Nov 2022 07:32:13 GMT
CMD []
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfd8cca9e94f77e0f23a9eec5b0cd1500c9594aebad7d086e5a6b76677eebaa`  
		Last Modified: Tue, 15 Nov 2022 07:36:40 GMT  
		Size: 1.6 MB (1624085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad7c5c28c45885655376f6fb553eacefd3fac7d9ae5238a69bec74371c656e0`  
		Last Modified: Tue, 15 Nov 2022 07:36:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7`

```console
$ docker pull hitch@sha256:2914c4c32db343875ad37f8ff10d29c6b42c2e569092d987184be52853c0cd51
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
$ docker pull hitch@sha256:36d995e4c365800b5c06add5c708d87d502069fea394c1d621e107804cc611cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33047349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31eaa012aff9da55a8ee56277169c8165d45a24d920c94c24e03018c7a8bb497`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:52:47 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 03:52:47 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 03:52:47 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 03:52:47 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 03:52:47 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 03:55:09 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 03:55:09 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 03:55:09 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 03:55:09 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 03:55:09 GMT
EXPOSE 443
# Tue, 25 Oct 2022 03:55:09 GMT
CMD []
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb58d7c4ae58e46e9f7f3a133a63fbbeb7fbbbb32e33966f5154e47c3ceec12`  
		Last Modified: Tue, 25 Oct 2022 03:57:30 GMT  
		Size: 1.6 MB (1626893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf6c8e8f72cac1af4a352a706377c56b7874956cf78cc69b2497b88a77e5352`  
		Last Modified: Tue, 25 Oct 2022 03:57:29 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7e5243c2e7681a7975d54b7188512f87cc0cd96400bd7607e73bfae4c04c32b1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28125419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec155d6e7d7ca5dd6520af2e4b3da7bf3555ede0850d6e151949c3fdcd6cc908`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 13:20:44 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 13:20:44 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 13:20:44 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 13:20:44 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 13:20:44 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 13:22:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 13:22:38 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 13:22:38 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 13:22:38 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 13:22:38 GMT
EXPOSE 443
# Tue, 25 Oct 2022 13:22:38 GMT
CMD []
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2560f5c440bcb344e07b93f0c453a8556e43c63bdd2eb54f6ac9188019b84cfc`  
		Last Modified: Tue, 25 Oct 2022 13:25:17 GMT  
		Size: 1.5 MB (1545709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103a95fdd02870ff462a20b0a7fea3fb250c528613536827c3f968e7d72d4ae`  
		Last Modified: Tue, 25 Oct 2022 13:25:17 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:e5ba13441f1a7085b9fea5024970ea2f370c6c8d61f0b1f8bbe9fe4e4be6511b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31668403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dface7840d899a8d9a685768e01d1e52a0708ff895d95d8a5cab70776066b5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:21:08 GMT
ARG SRCVER=1.7.3
# Tue, 15 Nov 2022 06:21:08 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 06:21:08 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 06:21:08 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 06:21:08 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 15 Nov 2022 06:23:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 06:23:37 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 06:23:38 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:23:38 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 06:23:38 GMT
EXPOSE 443
# Tue, 15 Nov 2022 06:23:38 GMT
CMD []
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313592145e823db6cb42dcfc2b587a67f1ab9657dd998105888b98a44c7704ac`  
		Last Modified: Tue, 15 Nov 2022 06:25:35 GMT  
		Size: 1.6 MB (1607381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0604703f3796f0b2b9605adee33e12d5c4112761a0001ae6518301e8f33f51f`  
		Last Modified: Tue, 15 Nov 2022 06:25:35 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; 386

```console
$ docker pull hitch@sha256:63b2fa866cb3b80aea85010b644c541723bcc1192d7ca41c159e910afa0ccea7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34027295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fde1440811f3f87556e6c3a840dafa6dcbd31db3bd7611372e2267b73b49c6b`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 02:22:34 GMT
ADD file:14adaece72e410cf04ac21a101e5b530aab1d5e5a189a2be72d195ec0ac5e6d4 in / 
# Tue, 25 Oct 2022 02:22:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:05:58 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 07:05:58 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 07:05:59 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 07:06:00 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 07:06:01 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 07:07:46 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 07:07:46 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 07:07:48 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:07:48 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 07:07:49 GMT
EXPOSE 443
# Tue, 25 Oct 2022 07:07:50 GMT
CMD []
```

-	Layers:
	-	`sha256:3c83067056c0f1bc4e162249831ac686f3a9a9c64c5366b903581580de8fcac2`  
		Last Modified: Tue, 25 Oct 2022 02:28:26 GMT  
		Size: 32.4 MB (32396384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a23a52a14eac897ff94c5663255f63ac00f47e3f92d56ce150927369a540f3`  
		Last Modified: Tue, 25 Oct 2022 07:08:48 GMT  
		Size: 1.6 MB (1630494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743da65dbf1956a87b5553dab51ceb17026da945adc6ea0d618c2786e93a7bd5`  
		Last Modified: Tue, 25 Oct 2022 07:08:47 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; ppc64le

```console
$ docker pull hitch@sha256:6ecf72a31dd4fcf3206c47608bdfc4f15eec1759d52cf3377f28420a084a946c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36977221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176ea8122edd48dc36abfbae685be31a83c0e2f78408178eb1fdf8b762cf0807`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:38:49 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 07:38:50 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 07:38:50 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 07:38:50 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 07:38:50 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 07:43:12 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 07:43:13 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 07:43:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:43:13 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 07:43:13 GMT
EXPOSE 443
# Tue, 25 Oct 2022 07:43:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9b139b300fbd61f2373a116840d3fc190ae40bde3e6fa0b5acfbe59b4d9533`  
		Last Modified: Tue, 25 Oct 2022 07:47:29 GMT  
		Size: 1.7 MB (1686718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5121dc1d0d1e79aa369638f89f421a8ae8c417002e27c91d5f1f59364431615d`  
		Last Modified: Tue, 25 Oct 2022 07:47:28 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7` - linux; s390x

```console
$ docker pull hitch@sha256:1ab9c81e5b9627e31ba303f1433b2e80d5189f1a988450a43c12b67372c7a395
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31268285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c62498018939442bf71e27b8fc3d99033db65a84a675110eeb3170766a8e327`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:28:17 GMT
ARG SRCVER=1.7.3
# Tue, 15 Nov 2022 07:28:18 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 07:28:18 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 07:28:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 07:28:19 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 15 Nov 2022 07:32:11 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 07:32:11 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 07:32:11 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 07:32:12 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 07:32:12 GMT
EXPOSE 443
# Tue, 15 Nov 2022 07:32:13 GMT
CMD []
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfd8cca9e94f77e0f23a9eec5b0cd1500c9594aebad7d086e5a6b76677eebaa`  
		Last Modified: Tue, 15 Nov 2022 07:36:40 GMT  
		Size: 1.6 MB (1624085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad7c5c28c45885655376f6fb553eacefd3fac7d9ae5238a69bec74371c656e0`  
		Last Modified: Tue, 15 Nov 2022 07:36:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7.2`

```console
$ docker pull hitch@sha256:538edb9ed80da4ac41a2ab28a19630b1e3b59e9a440564f8df1ef104565d6085
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
$ docker pull hitch@sha256:2f667d7958c58f2ee96cafeaac1d82ca741960282d80fa3e988c1c77beb3d535
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33046227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f855af8178e5070ed35e221972893da2b6202f1fa533a702c0e191f402dede`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:55:25 GMT
ARG SRCVER=1.7.2
# Tue, 25 Oct 2022 03:55:25 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 03:55:25 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 03:55:25 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 03:55:25 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 25 Oct 2022 03:57:13 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 03:57:13 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 03:57:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 03:57:13 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 03:57:14 GMT
EXPOSE 443
# Tue, 25 Oct 2022 03:57:14 GMT
CMD []
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4503a8a7409de4d531fe522901cff0da45c9c61f5fa806c1fbf8388fd3978e93`  
		Last Modified: Tue, 25 Oct 2022 03:57:45 GMT  
		Size: 1.6 MB (1625773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1d40f25f4a4d92fb51aec663869c43d020de66a8b4e0b8426af694677f49c0`  
		Last Modified: Tue, 25 Oct 2022 03:57:45 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; arm variant v7

```console
$ docker pull hitch@sha256:02eaebb6185069bd7aa7b3215e71de01dd14cd5e3f5b36f2731e3ee19f20983a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28124466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35a833288996572e9f88adeeece328f259a1cd07b9c5cbf457562ed8336411`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 13:22:56 GMT
ARG SRCVER=1.7.2
# Tue, 25 Oct 2022 13:22:56 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 13:22:56 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 13:22:56 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 13:22:56 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 25 Oct 2022 13:24:39 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 13:24:39 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 13:24:40 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 13:24:40 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 13:24:40 GMT
EXPOSE 443
# Tue, 25 Oct 2022 13:24:40 GMT
CMD []
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e0ac2afd7c3f82709dfecc011293ac7dddd0036dcc6758423f5317540dc338`  
		Last Modified: Tue, 25 Oct 2022 13:25:40 GMT  
		Size: 1.5 MB (1544756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bbe47cab9689f08f7b4a276f26d381476ef8d8758c1f3e53f79e2c106d66d1`  
		Last Modified: Tue, 25 Oct 2022 13:25:40 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:5323935fe4ac5ce2c0d949d51a80136694c6c464015478a0b4137b3e27f03618
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31667734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8c05b20615c7a9eae2c3f319116ca2203421d475b3af600a6116f2d91e21a7`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:23:45 GMT
ARG SRCVER=1.7.2
# Tue, 15 Nov 2022 06:23:45 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 06:23:46 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 06:23:46 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 06:23:46 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 15 Nov 2022 06:25:07 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 06:25:08 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 06:25:08 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:25:08 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 06:25:08 GMT
EXPOSE 443
# Tue, 15 Nov 2022 06:25:08 GMT
CMD []
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d457713150959fe10e3955162dfdd6bfa40d529d008a71c78b29347626af60f`  
		Last Modified: Tue, 15 Nov 2022 06:25:50 GMT  
		Size: 1.6 MB (1606712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a951f399b31d5e5953864b60e7fd2984f1a1b29071d7375e550406af8de02fe6`  
		Last Modified: Tue, 15 Nov 2022 06:25:50 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; 386

```console
$ docker pull hitch@sha256:dd6edcc259311a21b2c9873b5810604fa14287460a863ed502d19f06ba543374
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34011499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072fbd64b95bea887d6dd2dfc3aea87e96e5ab467e7b1772e237207d764794ec`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:35:32 GMT
ARG SRCVER=1.7.2
# Tue, 13 Sep 2022 06:35:32 GMT
ARG PKGVER=1
# Tue, 13 Sep 2022 06:35:33 GMT
ARG DISTVER=bullseye
# Tue, 13 Sep 2022 06:35:34 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Sep 2022 06:35:35 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 13 Sep 2022 06:37:21 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Sep 2022 06:37:22 GMT
WORKDIR /etc/hitch
# Tue, 13 Sep 2022 06:37:24 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Sep 2022 06:37:24 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Sep 2022 06:37:25 GMT
EXPOSE 443
# Tue, 13 Sep 2022 06:37:26 GMT
CMD []
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cced29c1fdf41682e20f38086673848dbbbc5b3a8d7447aaed6ea4f5a6ecce`  
		Last Modified: Tue, 13 Sep 2022 06:37:57 GMT  
		Size: 1.6 MB (1627294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb21f2723f56a8d7bd10678a17e8a61a5165a952b37976a8195da7f36298be12`  
		Last Modified: Tue, 13 Sep 2022 06:37:57 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; ppc64le

```console
$ docker pull hitch@sha256:e6580ff328e25e6cc07eaaff9583e165c4061a748b9423b2d908c45f95834e3f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36976408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebebc5c78c1b99a8bd26175f4030e9a3f96b1ceea570e98e5464dc9ebc687c13`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:43:30 GMT
ARG SRCVER=1.7.2
# Tue, 25 Oct 2022 07:43:30 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 07:43:30 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 07:43:31 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 07:43:31 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 25 Oct 2022 07:46:51 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 07:46:52 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 07:46:52 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:46:52 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 07:46:52 GMT
EXPOSE 443
# Tue, 25 Oct 2022 07:46:53 GMT
CMD []
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e80fb0ab2644e9c2cbf3b0628fd64c7fa1b35b98d387b87c404f74fd42c34f`  
		Last Modified: Tue, 25 Oct 2022 07:47:50 GMT  
		Size: 1.7 MB (1685904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ff1f378c255ffce77726356d88a54b5276cd1e7a5849e280fdfb9bfaac490`  
		Last Modified: Tue, 25 Oct 2022 07:47:50 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2` - linux; s390x

```console
$ docker pull hitch@sha256:a42cfc73e321984bd6a445c2f9b7b451fd1e6cc4a6a0caed67831fc8ddb513b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31267713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92129562716d2a501b3e1544cae093f66956267d0dc505cdf1f2a4fe523ec62f`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:32:25 GMT
ARG SRCVER=1.7.2
# Tue, 15 Nov 2022 07:32:26 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 07:32:26 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 07:32:26 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 07:32:27 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 15 Nov 2022 07:36:02 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 07:36:03 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 07:36:03 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 07:36:04 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 07:36:05 GMT
EXPOSE 443
# Tue, 15 Nov 2022 07:36:05 GMT
CMD []
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632b59b31fbe6f41581395920113fe1c5e30fabac2f965cd736be2cd5730c99`  
		Last Modified: Tue, 15 Nov 2022 07:36:53 GMT  
		Size: 1.6 MB (1623516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc768d6af3ce7ff5ae48a3829fde0b22268716f46ccf99e4dfaaaf3d67d32328`  
		Last Modified: Tue, 15 Nov 2022 07:36:53 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7.2-1`

```console
$ docker pull hitch@sha256:538edb9ed80da4ac41a2ab28a19630b1e3b59e9a440564f8df1ef104565d6085
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
$ docker pull hitch@sha256:2f667d7958c58f2ee96cafeaac1d82ca741960282d80fa3e988c1c77beb3d535
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33046227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f855af8178e5070ed35e221972893da2b6202f1fa533a702c0e191f402dede`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:55:25 GMT
ARG SRCVER=1.7.2
# Tue, 25 Oct 2022 03:55:25 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 03:55:25 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 03:55:25 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 03:55:25 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 25 Oct 2022 03:57:13 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 03:57:13 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 03:57:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 03:57:13 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 03:57:14 GMT
EXPOSE 443
# Tue, 25 Oct 2022 03:57:14 GMT
CMD []
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4503a8a7409de4d531fe522901cff0da45c9c61f5fa806c1fbf8388fd3978e93`  
		Last Modified: Tue, 25 Oct 2022 03:57:45 GMT  
		Size: 1.6 MB (1625773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1d40f25f4a4d92fb51aec663869c43d020de66a8b4e0b8426af694677f49c0`  
		Last Modified: Tue, 25 Oct 2022 03:57:45 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:02eaebb6185069bd7aa7b3215e71de01dd14cd5e3f5b36f2731e3ee19f20983a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28124466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d35a833288996572e9f88adeeece328f259a1cd07b9c5cbf457562ed8336411`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 13:22:56 GMT
ARG SRCVER=1.7.2
# Tue, 25 Oct 2022 13:22:56 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 13:22:56 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 13:22:56 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 13:22:56 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 25 Oct 2022 13:24:39 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 13:24:39 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 13:24:40 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 13:24:40 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 13:24:40 GMT
EXPOSE 443
# Tue, 25 Oct 2022 13:24:40 GMT
CMD []
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e0ac2afd7c3f82709dfecc011293ac7dddd0036dcc6758423f5317540dc338`  
		Last Modified: Tue, 25 Oct 2022 13:25:40 GMT  
		Size: 1.5 MB (1544756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bbe47cab9689f08f7b4a276f26d381476ef8d8758c1f3e53f79e2c106d66d1`  
		Last Modified: Tue, 25 Oct 2022 13:25:40 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:5323935fe4ac5ce2c0d949d51a80136694c6c464015478a0b4137b3e27f03618
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31667734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8c05b20615c7a9eae2c3f319116ca2203421d475b3af600a6116f2d91e21a7`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:23:45 GMT
ARG SRCVER=1.7.2
# Tue, 15 Nov 2022 06:23:45 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 06:23:46 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 06:23:46 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 06:23:46 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 15 Nov 2022 06:25:07 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 06:25:08 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 06:25:08 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:25:08 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 06:25:08 GMT
EXPOSE 443
# Tue, 15 Nov 2022 06:25:08 GMT
CMD []
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d457713150959fe10e3955162dfdd6bfa40d529d008a71c78b29347626af60f`  
		Last Modified: Tue, 15 Nov 2022 06:25:50 GMT  
		Size: 1.6 MB (1606712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a951f399b31d5e5953864b60e7fd2984f1a1b29071d7375e550406af8de02fe6`  
		Last Modified: Tue, 15 Nov 2022 06:25:50 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; 386

```console
$ docker pull hitch@sha256:dd6edcc259311a21b2c9873b5810604fa14287460a863ed502d19f06ba543374
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34011499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072fbd64b95bea887d6dd2dfc3aea87e96e5ab467e7b1772e237207d764794ec`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:35:32 GMT
ARG SRCVER=1.7.2
# Tue, 13 Sep 2022 06:35:32 GMT
ARG PKGVER=1
# Tue, 13 Sep 2022 06:35:33 GMT
ARG DISTVER=bullseye
# Tue, 13 Sep 2022 06:35:34 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 13 Sep 2022 06:35:35 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 13 Sep 2022 06:37:21 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 13 Sep 2022 06:37:22 GMT
WORKDIR /etc/hitch
# Tue, 13 Sep 2022 06:37:24 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 13 Sep 2022 06:37:24 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 13 Sep 2022 06:37:25 GMT
EXPOSE 443
# Tue, 13 Sep 2022 06:37:26 GMT
CMD []
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cced29c1fdf41682e20f38086673848dbbbc5b3a8d7447aaed6ea4f5a6ecce`  
		Last Modified: Tue, 13 Sep 2022 06:37:57 GMT  
		Size: 1.6 MB (1627294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb21f2723f56a8d7bd10678a17e8a61a5165a952b37976a8195da7f36298be12`  
		Last Modified: Tue, 13 Sep 2022 06:37:57 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; ppc64le

```console
$ docker pull hitch@sha256:e6580ff328e25e6cc07eaaff9583e165c4061a748b9423b2d908c45f95834e3f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36976408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebebc5c78c1b99a8bd26175f4030e9a3f96b1ceea570e98e5464dc9ebc687c13`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:43:30 GMT
ARG SRCVER=1.7.2
# Tue, 25 Oct 2022 07:43:30 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 07:43:30 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 07:43:31 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 07:43:31 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 25 Oct 2022 07:46:51 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 07:46:52 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 07:46:52 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:46:52 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 07:46:52 GMT
EXPOSE 443
# Tue, 25 Oct 2022 07:46:53 GMT
CMD []
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e80fb0ab2644e9c2cbf3b0628fd64c7fa1b35b98d387b87c404f74fd42c34f`  
		Last Modified: Tue, 25 Oct 2022 07:47:50 GMT  
		Size: 1.7 MB (1685904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231ff1f378c255ffce77726356d88a54b5276cd1e7a5849e280fdfb9bfaac490`  
		Last Modified: Tue, 25 Oct 2022 07:47:50 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.2-1` - linux; s390x

```console
$ docker pull hitch@sha256:a42cfc73e321984bd6a445c2f9b7b451fd1e6cc4a6a0caed67831fc8ddb513b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31267713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92129562716d2a501b3e1544cae093f66956267d0dc505cdf1f2a4fe523ec62f`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:32:25 GMT
ARG SRCVER=1.7.2
# Tue, 15 Nov 2022 07:32:26 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 07:32:26 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 07:32:26 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 07:32:27 GMT
ARG SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf
# Tue, 15 Nov 2022 07:36:02 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=7b35b5f4a3b6dab2599643c0bc90880a77ea518a627b31813f45a7ee8c52982ba4ac07228b640a0bcf90ea7d63421b62884a091fed6664732585585e5ec15bcf SRCVER=1.7.2
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 07:36:03 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 07:36:03 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 07:36:04 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 07:36:05 GMT
EXPOSE 443
# Tue, 15 Nov 2022 07:36:05 GMT
CMD []
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632b59b31fbe6f41581395920113fe1c5e30fabac2f965cd736be2cd5730c99`  
		Last Modified: Tue, 15 Nov 2022 07:36:53 GMT  
		Size: 1.6 MB (1623516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc768d6af3ce7ff5ae48a3829fde0b22268716f46ccf99e4dfaaaf3d67d32328`  
		Last Modified: Tue, 15 Nov 2022 07:36:53 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7.3`

```console
$ docker pull hitch@sha256:2914c4c32db343875ad37f8ff10d29c6b42c2e569092d987184be52853c0cd51
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
$ docker pull hitch@sha256:36d995e4c365800b5c06add5c708d87d502069fea394c1d621e107804cc611cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33047349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31eaa012aff9da55a8ee56277169c8165d45a24d920c94c24e03018c7a8bb497`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:52:47 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 03:52:47 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 03:52:47 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 03:52:47 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 03:52:47 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 03:55:09 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 03:55:09 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 03:55:09 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 03:55:09 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 03:55:09 GMT
EXPOSE 443
# Tue, 25 Oct 2022 03:55:09 GMT
CMD []
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb58d7c4ae58e46e9f7f3a133a63fbbeb7fbbbb32e33966f5154e47c3ceec12`  
		Last Modified: Tue, 25 Oct 2022 03:57:30 GMT  
		Size: 1.6 MB (1626893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf6c8e8f72cac1af4a352a706377c56b7874956cf78cc69b2497b88a77e5352`  
		Last Modified: Tue, 25 Oct 2022 03:57:29 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7e5243c2e7681a7975d54b7188512f87cc0cd96400bd7607e73bfae4c04c32b1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28125419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec155d6e7d7ca5dd6520af2e4b3da7bf3555ede0850d6e151949c3fdcd6cc908`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 13:20:44 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 13:20:44 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 13:20:44 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 13:20:44 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 13:20:44 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 13:22:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 13:22:38 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 13:22:38 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 13:22:38 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 13:22:38 GMT
EXPOSE 443
# Tue, 25 Oct 2022 13:22:38 GMT
CMD []
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2560f5c440bcb344e07b93f0c453a8556e43c63bdd2eb54f6ac9188019b84cfc`  
		Last Modified: Tue, 25 Oct 2022 13:25:17 GMT  
		Size: 1.5 MB (1545709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103a95fdd02870ff462a20b0a7fea3fb250c528613536827c3f968e7d72d4ae`  
		Last Modified: Tue, 25 Oct 2022 13:25:17 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:e5ba13441f1a7085b9fea5024970ea2f370c6c8d61f0b1f8bbe9fe4e4be6511b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31668403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dface7840d899a8d9a685768e01d1e52a0708ff895d95d8a5cab70776066b5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:21:08 GMT
ARG SRCVER=1.7.3
# Tue, 15 Nov 2022 06:21:08 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 06:21:08 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 06:21:08 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 06:21:08 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 15 Nov 2022 06:23:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 06:23:37 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 06:23:38 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:23:38 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 06:23:38 GMT
EXPOSE 443
# Tue, 15 Nov 2022 06:23:38 GMT
CMD []
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313592145e823db6cb42dcfc2b587a67f1ab9657dd998105888b98a44c7704ac`  
		Last Modified: Tue, 15 Nov 2022 06:25:35 GMT  
		Size: 1.6 MB (1607381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0604703f3796f0b2b9605adee33e12d5c4112761a0001ae6518301e8f33f51f`  
		Last Modified: Tue, 15 Nov 2022 06:25:35 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; 386

```console
$ docker pull hitch@sha256:63b2fa866cb3b80aea85010b644c541723bcc1192d7ca41c159e910afa0ccea7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34027295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fde1440811f3f87556e6c3a840dafa6dcbd31db3bd7611372e2267b73b49c6b`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 02:22:34 GMT
ADD file:14adaece72e410cf04ac21a101e5b530aab1d5e5a189a2be72d195ec0ac5e6d4 in / 
# Tue, 25 Oct 2022 02:22:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:05:58 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 07:05:58 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 07:05:59 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 07:06:00 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 07:06:01 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 07:07:46 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 07:07:46 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 07:07:48 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:07:48 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 07:07:49 GMT
EXPOSE 443
# Tue, 25 Oct 2022 07:07:50 GMT
CMD []
```

-	Layers:
	-	`sha256:3c83067056c0f1bc4e162249831ac686f3a9a9c64c5366b903581580de8fcac2`  
		Last Modified: Tue, 25 Oct 2022 02:28:26 GMT  
		Size: 32.4 MB (32396384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a23a52a14eac897ff94c5663255f63ac00f47e3f92d56ce150927369a540f3`  
		Last Modified: Tue, 25 Oct 2022 07:08:48 GMT  
		Size: 1.6 MB (1630494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743da65dbf1956a87b5553dab51ceb17026da945adc6ea0d618c2786e93a7bd5`  
		Last Modified: Tue, 25 Oct 2022 07:08:47 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; ppc64le

```console
$ docker pull hitch@sha256:6ecf72a31dd4fcf3206c47608bdfc4f15eec1759d52cf3377f28420a084a946c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36977221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176ea8122edd48dc36abfbae685be31a83c0e2f78408178eb1fdf8b762cf0807`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:38:49 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 07:38:50 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 07:38:50 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 07:38:50 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 07:38:50 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 07:43:12 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 07:43:13 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 07:43:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:43:13 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 07:43:13 GMT
EXPOSE 443
# Tue, 25 Oct 2022 07:43:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9b139b300fbd61f2373a116840d3fc190ae40bde3e6fa0b5acfbe59b4d9533`  
		Last Modified: Tue, 25 Oct 2022 07:47:29 GMT  
		Size: 1.7 MB (1686718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5121dc1d0d1e79aa369638f89f421a8ae8c417002e27c91d5f1f59364431615d`  
		Last Modified: Tue, 25 Oct 2022 07:47:28 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3` - linux; s390x

```console
$ docker pull hitch@sha256:1ab9c81e5b9627e31ba303f1433b2e80d5189f1a988450a43c12b67372c7a395
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31268285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c62498018939442bf71e27b8fc3d99033db65a84a675110eeb3170766a8e327`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:28:17 GMT
ARG SRCVER=1.7.3
# Tue, 15 Nov 2022 07:28:18 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 07:28:18 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 07:28:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 07:28:19 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 15 Nov 2022 07:32:11 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 07:32:11 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 07:32:11 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 07:32:12 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 07:32:12 GMT
EXPOSE 443
# Tue, 15 Nov 2022 07:32:13 GMT
CMD []
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfd8cca9e94f77e0f23a9eec5b0cd1500c9594aebad7d086e5a6b76677eebaa`  
		Last Modified: Tue, 15 Nov 2022 07:36:40 GMT  
		Size: 1.6 MB (1624085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad7c5c28c45885655376f6fb553eacefd3fac7d9ae5238a69bec74371c656e0`  
		Last Modified: Tue, 15 Nov 2022 07:36:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:1.7.3-1`

```console
$ docker pull hitch@sha256:2914c4c32db343875ad37f8ff10d29c6b42c2e569092d987184be52853c0cd51
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
$ docker pull hitch@sha256:36d995e4c365800b5c06add5c708d87d502069fea394c1d621e107804cc611cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33047349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31eaa012aff9da55a8ee56277169c8165d45a24d920c94c24e03018c7a8bb497`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:52:47 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 03:52:47 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 03:52:47 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 03:52:47 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 03:52:47 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 03:55:09 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 03:55:09 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 03:55:09 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 03:55:09 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 03:55:09 GMT
EXPOSE 443
# Tue, 25 Oct 2022 03:55:09 GMT
CMD []
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb58d7c4ae58e46e9f7f3a133a63fbbeb7fbbbb32e33966f5154e47c3ceec12`  
		Last Modified: Tue, 25 Oct 2022 03:57:30 GMT  
		Size: 1.6 MB (1626893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf6c8e8f72cac1af4a352a706377c56b7874956cf78cc69b2497b88a77e5352`  
		Last Modified: Tue, 25 Oct 2022 03:57:29 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7e5243c2e7681a7975d54b7188512f87cc0cd96400bd7607e73bfae4c04c32b1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28125419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec155d6e7d7ca5dd6520af2e4b3da7bf3555ede0850d6e151949c3fdcd6cc908`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 13:20:44 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 13:20:44 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 13:20:44 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 13:20:44 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 13:20:44 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 13:22:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 13:22:38 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 13:22:38 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 13:22:38 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 13:22:38 GMT
EXPOSE 443
# Tue, 25 Oct 2022 13:22:38 GMT
CMD []
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2560f5c440bcb344e07b93f0c453a8556e43c63bdd2eb54f6ac9188019b84cfc`  
		Last Modified: Tue, 25 Oct 2022 13:25:17 GMT  
		Size: 1.5 MB (1545709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103a95fdd02870ff462a20b0a7fea3fb250c528613536827c3f968e7d72d4ae`  
		Last Modified: Tue, 25 Oct 2022 13:25:17 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:e5ba13441f1a7085b9fea5024970ea2f370c6c8d61f0b1f8bbe9fe4e4be6511b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31668403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dface7840d899a8d9a685768e01d1e52a0708ff895d95d8a5cab70776066b5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:21:08 GMT
ARG SRCVER=1.7.3
# Tue, 15 Nov 2022 06:21:08 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 06:21:08 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 06:21:08 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 06:21:08 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 15 Nov 2022 06:23:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 06:23:37 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 06:23:38 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:23:38 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 06:23:38 GMT
EXPOSE 443
# Tue, 15 Nov 2022 06:23:38 GMT
CMD []
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313592145e823db6cb42dcfc2b587a67f1ab9657dd998105888b98a44c7704ac`  
		Last Modified: Tue, 15 Nov 2022 06:25:35 GMT  
		Size: 1.6 MB (1607381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0604703f3796f0b2b9605adee33e12d5c4112761a0001ae6518301e8f33f51f`  
		Last Modified: Tue, 15 Nov 2022 06:25:35 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; 386

```console
$ docker pull hitch@sha256:63b2fa866cb3b80aea85010b644c541723bcc1192d7ca41c159e910afa0ccea7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34027295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fde1440811f3f87556e6c3a840dafa6dcbd31db3bd7611372e2267b73b49c6b`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 02:22:34 GMT
ADD file:14adaece72e410cf04ac21a101e5b530aab1d5e5a189a2be72d195ec0ac5e6d4 in / 
# Tue, 25 Oct 2022 02:22:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:05:58 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 07:05:58 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 07:05:59 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 07:06:00 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 07:06:01 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 07:07:46 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 07:07:46 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 07:07:48 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:07:48 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 07:07:49 GMT
EXPOSE 443
# Tue, 25 Oct 2022 07:07:50 GMT
CMD []
```

-	Layers:
	-	`sha256:3c83067056c0f1bc4e162249831ac686f3a9a9c64c5366b903581580de8fcac2`  
		Last Modified: Tue, 25 Oct 2022 02:28:26 GMT  
		Size: 32.4 MB (32396384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a23a52a14eac897ff94c5663255f63ac00f47e3f92d56ce150927369a540f3`  
		Last Modified: Tue, 25 Oct 2022 07:08:48 GMT  
		Size: 1.6 MB (1630494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743da65dbf1956a87b5553dab51ceb17026da945adc6ea0d618c2786e93a7bd5`  
		Last Modified: Tue, 25 Oct 2022 07:08:47 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; ppc64le

```console
$ docker pull hitch@sha256:6ecf72a31dd4fcf3206c47608bdfc4f15eec1759d52cf3377f28420a084a946c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36977221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176ea8122edd48dc36abfbae685be31a83c0e2f78408178eb1fdf8b762cf0807`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:38:49 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 07:38:50 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 07:38:50 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 07:38:50 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 07:38:50 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 07:43:12 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 07:43:13 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 07:43:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:43:13 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 07:43:13 GMT
EXPOSE 443
# Tue, 25 Oct 2022 07:43:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9b139b300fbd61f2373a116840d3fc190ae40bde3e6fa0b5acfbe59b4d9533`  
		Last Modified: Tue, 25 Oct 2022 07:47:29 GMT  
		Size: 1.7 MB (1686718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5121dc1d0d1e79aa369638f89f421a8ae8c417002e27c91d5f1f59364431615d`  
		Last Modified: Tue, 25 Oct 2022 07:47:28 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:1.7.3-1` - linux; s390x

```console
$ docker pull hitch@sha256:1ab9c81e5b9627e31ba303f1433b2e80d5189f1a988450a43c12b67372c7a395
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31268285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c62498018939442bf71e27b8fc3d99033db65a84a675110eeb3170766a8e327`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:28:17 GMT
ARG SRCVER=1.7.3
# Tue, 15 Nov 2022 07:28:18 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 07:28:18 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 07:28:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 07:28:19 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 15 Nov 2022 07:32:11 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 07:32:11 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 07:32:11 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 07:32:12 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 07:32:12 GMT
EXPOSE 443
# Tue, 15 Nov 2022 07:32:13 GMT
CMD []
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfd8cca9e94f77e0f23a9eec5b0cd1500c9594aebad7d086e5a6b76677eebaa`  
		Last Modified: Tue, 15 Nov 2022 07:36:40 GMT  
		Size: 1.6 MB (1624085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad7c5c28c45885655376f6fb553eacefd3fac7d9ae5238a69bec74371c656e0`  
		Last Modified: Tue, 15 Nov 2022 07:36:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hitch:latest`

```console
$ docker pull hitch@sha256:2914c4c32db343875ad37f8ff10d29c6b42c2e569092d987184be52853c0cd51
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
$ docker pull hitch@sha256:36d995e4c365800b5c06add5c708d87d502069fea394c1d621e107804cc611cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33047349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31eaa012aff9da55a8ee56277169c8165d45a24d920c94c24e03018c7a8bb497`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:52:47 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 03:52:47 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 03:52:47 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 03:52:47 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 03:52:47 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 03:55:09 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 03:55:09 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 03:55:09 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 03:55:09 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 03:55:09 GMT
EXPOSE 443
# Tue, 25 Oct 2022 03:55:09 GMT
CMD []
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb58d7c4ae58e46e9f7f3a133a63fbbeb7fbbbb32e33966f5154e47c3ceec12`  
		Last Modified: Tue, 25 Oct 2022 03:57:30 GMT  
		Size: 1.6 MB (1626893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf6c8e8f72cac1af4a352a706377c56b7874956cf78cc69b2497b88a77e5352`  
		Last Modified: Tue, 25 Oct 2022 03:57:29 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; arm variant v7

```console
$ docker pull hitch@sha256:7e5243c2e7681a7975d54b7188512f87cc0cd96400bd7607e73bfae4c04c32b1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28125419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec155d6e7d7ca5dd6520af2e4b3da7bf3555ede0850d6e151949c3fdcd6cc908`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 13:20:44 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 13:20:44 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 13:20:44 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 13:20:44 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 13:20:44 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 13:22:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 13:22:38 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 13:22:38 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 13:22:38 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 13:22:38 GMT
EXPOSE 443
# Tue, 25 Oct 2022 13:22:38 GMT
CMD []
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2560f5c440bcb344e07b93f0c453a8556e43c63bdd2eb54f6ac9188019b84cfc`  
		Last Modified: Tue, 25 Oct 2022 13:25:17 GMT  
		Size: 1.5 MB (1545709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c103a95fdd02870ff462a20b0a7fea3fb250c528613536827c3f968e7d72d4ae`  
		Last Modified: Tue, 25 Oct 2022 13:25:17 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:e5ba13441f1a7085b9fea5024970ea2f370c6c8d61f0b1f8bbe9fe4e4be6511b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31668403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dface7840d899a8d9a685768e01d1e52a0708ff895d95d8a5cab70776066b5`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:21:08 GMT
ARG SRCVER=1.7.3
# Tue, 15 Nov 2022 06:21:08 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 06:21:08 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 06:21:08 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 06:21:08 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 15 Nov 2022 06:23:37 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 06:23:37 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 06:23:38 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 06:23:38 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 06:23:38 GMT
EXPOSE 443
# Tue, 15 Nov 2022 06:23:38 GMT
CMD []
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313592145e823db6cb42dcfc2b587a67f1ab9657dd998105888b98a44c7704ac`  
		Last Modified: Tue, 15 Nov 2022 06:25:35 GMT  
		Size: 1.6 MB (1607381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0604703f3796f0b2b9605adee33e12d5c4112761a0001ae6518301e8f33f51f`  
		Last Modified: Tue, 15 Nov 2022 06:25:35 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; 386

```console
$ docker pull hitch@sha256:63b2fa866cb3b80aea85010b644c541723bcc1192d7ca41c159e910afa0ccea7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34027295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fde1440811f3f87556e6c3a840dafa6dcbd31db3bd7611372e2267b73b49c6b`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 02:22:34 GMT
ADD file:14adaece72e410cf04ac21a101e5b530aab1d5e5a189a2be72d195ec0ac5e6d4 in / 
# Tue, 25 Oct 2022 02:22:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:05:58 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 07:05:58 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 07:05:59 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 07:06:00 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 07:06:01 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 07:07:46 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 07:07:46 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 07:07:48 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:07:48 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 07:07:49 GMT
EXPOSE 443
# Tue, 25 Oct 2022 07:07:50 GMT
CMD []
```

-	Layers:
	-	`sha256:3c83067056c0f1bc4e162249831ac686f3a9a9c64c5366b903581580de8fcac2`  
		Last Modified: Tue, 25 Oct 2022 02:28:26 GMT  
		Size: 32.4 MB (32396384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a23a52a14eac897ff94c5663255f63ac00f47e3f92d56ce150927369a540f3`  
		Last Modified: Tue, 25 Oct 2022 07:08:48 GMT  
		Size: 1.6 MB (1630494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743da65dbf1956a87b5553dab51ceb17026da945adc6ea0d618c2786e93a7bd5`  
		Last Modified: Tue, 25 Oct 2022 07:08:47 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; ppc64le

```console
$ docker pull hitch@sha256:6ecf72a31dd4fcf3206c47608bdfc4f15eec1759d52cf3377f28420a084a946c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36977221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176ea8122edd48dc36abfbae685be31a83c0e2f78408178eb1fdf8b762cf0807`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:38:49 GMT
ARG SRCVER=1.7.3
# Tue, 25 Oct 2022 07:38:50 GMT
ARG PKGVER=1
# Tue, 25 Oct 2022 07:38:50 GMT
ARG DISTVER=bullseye
# Tue, 25 Oct 2022 07:38:50 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 25 Oct 2022 07:38:50 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 25 Oct 2022 07:43:12 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 25 Oct 2022 07:43:13 GMT
WORKDIR /etc/hitch
# Tue, 25 Oct 2022 07:43:13 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:43:13 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 25 Oct 2022 07:43:13 GMT
EXPOSE 443
# Tue, 25 Oct 2022 07:43:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9b139b300fbd61f2373a116840d3fc190ae40bde3e6fa0b5acfbe59b4d9533`  
		Last Modified: Tue, 25 Oct 2022 07:47:29 GMT  
		Size: 1.7 MB (1686718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5121dc1d0d1e79aa369638f89f421a8ae8c417002e27c91d5f1f59364431615d`  
		Last Modified: Tue, 25 Oct 2022 07:47:28 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; s390x

```console
$ docker pull hitch@sha256:1ab9c81e5b9627e31ba303f1433b2e80d5189f1a988450a43c12b67372c7a395
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31268285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c62498018939442bf71e27b8fc3d99033db65a84a675110eeb3170766a8e327`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 15 Nov 2022 01:42:51 GMT
ADD file:af482bbfc85f1f292de8bd5f2751ee2b67ec9e057eab3684f96984f0e4ecf943 in / 
# Tue, 15 Nov 2022 01:42:56 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:28:17 GMT
ARG SRCVER=1.7.3
# Tue, 15 Nov 2022 07:28:18 GMT
ARG PKGVER=1
# Tue, 15 Nov 2022 07:28:18 GMT
ARG DISTVER=bullseye
# Tue, 15 Nov 2022 07:28:18 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Tue, 15 Nov 2022 07:28:19 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Tue, 15 Nov 2022 07:32:11 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Tue, 15 Nov 2022 07:32:11 GMT
WORKDIR /etc/hitch
# Tue, 15 Nov 2022 07:32:11 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Tue, 15 Nov 2022 07:32:12 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Tue, 15 Nov 2022 07:32:12 GMT
EXPOSE 443
# Tue, 15 Nov 2022 07:32:13 GMT
CMD []
```

-	Layers:
	-	`sha256:a6ad801d746b7bdde3a0ef72107d05694a38101de03b6eed340af802bdf13957`  
		Last Modified: Tue, 15 Nov 2022 01:47:33 GMT  
		Size: 29.6 MB (29643781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfd8cca9e94f77e0f23a9eec5b0cd1500c9594aebad7d086e5a6b76677eebaa`  
		Last Modified: Tue, 15 Nov 2022 07:36:40 GMT  
		Size: 1.6 MB (1624085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad7c5c28c45885655376f6fb553eacefd3fac7d9ae5238a69bec74371c656e0`  
		Last Modified: Tue, 15 Nov 2022 07:36:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
