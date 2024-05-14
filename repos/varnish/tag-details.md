<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.12`](#varnish6012)
-	[`varnish:6.0.13`](#varnish6013)
-	[`varnish:7.3`](#varnish73)
-	[`varnish:7.3-alpine`](#varnish73-alpine)
-	[`varnish:7.3.1`](#varnish731)
-	[`varnish:7.3.1-alpine`](#varnish731-alpine)
-	[`varnish:7.4`](#varnish74)
-	[`varnish:7.4-alpine`](#varnish74-alpine)
-	[`varnish:7.4.2`](#varnish742)
-	[`varnish:7.4.2-alpine`](#varnish742-alpine)
-	[`varnish:7.4.3`](#varnish743)
-	[`varnish:7.4.3-alpine`](#varnish743-alpine)
-	[`varnish:7.5`](#varnish75)
-	[`varnish:7.5-alpine`](#varnish75-alpine)
-	[`varnish:7.5.0`](#varnish750)
-	[`varnish:7.5.0-alpine`](#varnish750-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:eb5b5923785da107b84db2f896cc90d654c14ed335123c16fbbf8d8fa17dacc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:3be84605f51934b662a1fd32c03d982f9235468fdb8427f2d20fa1c8429dc4a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95874783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9aa8a59b93ff62a0d1e53b9cbd4026c35668b03c79c4969bf8746954b5a9fbe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:26:32 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 14:26:32 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 14:26:32 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 14:26:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:28:21 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 14:28:21 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:28:21 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 14:28:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:28:21 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:28:22 GMT
CMD []
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359f8f3a4792f96c1720dfd7f4dd952889d4ab9344eb0fe9413ffffc2229b61a`  
		Last Modified: Tue, 14 May 2024 14:37:03 GMT  
		Size: 64.4 MB (64440136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0385c17efd750567c8ab5fce43768872bc80277f323daa30421423f5c8f598a`  
		Last Modified: Tue, 14 May 2024 14:36:54 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:56f3662203529fca4d1f77533683ba3d50392d0a8e33a7b17d00def46c101b65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72870716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7b9d0eb1054b63a01be7fe1c035340bf0a4ad3c10879eb62f9e0358c60f7fb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:35:00 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 09:35:00 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 09:35:00 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 09:35:00 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:36:47 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 09:36:47 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:36:48 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 09:36:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:36:48 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:36:48 GMT
CMD []
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f106de5cb49a4793119ff373fe3b357fc2eed6a8825ca5516e4b0f113a9271`  
		Last Modified: Tue, 14 May 2024 09:45:13 GMT  
		Size: 46.3 MB (46275509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4360686e3bc89571cb56e34c207bf1c03b274f41f9f0efc016795bf2ee8e822`  
		Last Modified: Tue, 14 May 2024 09:45:07 GMT  
		Size: 714.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a21d622cce0cfc37c7923b5405f569e8d5dd5434cc40583cfd5c6ed71544bd85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89977458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3d300d8903dff396e57d3e6e86b7f065db5cb2c7c0dbbd5e11e34adb97ca23`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:41:33 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 07:41:33 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 07:41:33 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 07:41:33 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:43:01 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 07:43:01 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:43:01 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 07:43:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:43:01 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:43:02 GMT
CMD []
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e142232f2ce3e867f9128875cf61777e5e40c82eb952700a7896f5a16901a0`  
		Last Modified: Tue, 14 May 2024 07:50:31 GMT  
		Size: 59.9 MB (59889832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c0ecccf7b958b1578b188ef2833a7365f17b5a62ba9227b337f41e137076e7`  
		Last Modified: Tue, 14 May 2024 07:50:25 GMT  
		Size: 718.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:fae67428c9fbfac1d3bafbb56d810446a2dc60497ac3341f640cfd4a24fd7aeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97146491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1d4b8a8f9c33f0bb44f64d7ad8166752b52f58da7a88086e0cac799831c38`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:34 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 14 May 2024 00:47:34 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:44:30 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 08:44:30 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 08:44:30 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 08:44:30 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:46:47 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 08:46:48 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:46:48 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 08:46:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:46:49 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:46:49 GMT
CMD []
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f907ff471f0851875703285eb6d0ef438811d491aadb5aba748aa312476aeda`  
		Last Modified: Tue, 14 May 2024 08:57:59 GMT  
		Size: 64.7 MB (64721732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18e6804a4d99f5cc0febeea741d31d1ed3388b1f166485bba629841e4a9fc6f`  
		Last Modified: Tue, 14 May 2024 08:57:47 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:cdc5925f33e2f3d2766f8f221d3f3dd8ce814a4387b8ce60bbde786d9ba097bc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94661580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98390a649c51397783ed4d8fe780ca0f05dc4f989c8d00aef9ac970fabff2136`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:25:05 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 06:25:05 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 06:25:06 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 06:25:06 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:28:35 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 06:28:38 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:28:38 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 06:28:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:28:38 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:28:39 GMT
CMD []
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dfefba4fba615398a7eab3e3342d67dcf7df7f8e6cac0f28d30001ab1684e5`  
		Last Modified: Tue, 14 May 2024 06:42:28 GMT  
		Size: 59.3 MB (59349704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f01dbfb3e2cfaa17b94584fd9fcb792d0ee168bcb7891a67a3d3d2feae19f5`  
		Last Modified: Tue, 14 May 2024 06:42:18 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:c9887b4336fa3addcaa27879c77b53e03af001a369ad6a8abff832e56c356b56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deacee544cdd187a45643da0b7bc6eeedf17ba7641ea2f1e758deeda3adbd530`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:43:11 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Tue, 14 May 2024 00:43:13 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:36:02 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 06:36:02 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 06:36:02 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 06:36:03 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:37:27 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 06:37:29 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:37:29 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 06:37:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:37:30 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:37:30 GMT
CMD []
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a4866f0e934710827a963ac4a2533e21008525af1ba9fdb2b354138060dd70`  
		Last Modified: Tue, 14 May 2024 06:45:13 GMT  
		Size: 46.6 MB (46596547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8339ee670ce12c69916f24743f49512e75d61dc5c928b10db3b0442836475`  
		Last Modified: Tue, 14 May 2024 06:45:07 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.12`

```console
$ docker pull varnish@sha256:f46b4866bde4cfe4ea3ff6a98b119cc00a9f57de9cb05caffb9a8ba224b1ee41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.0.12` - linux; amd64

```console
$ docker pull varnish@sha256:7bd3e46dded4246e712fdbc22f077b117b1cbe264bfa42f7433dc1bb1c1af022
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95870395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb27f0d6a3421a5730ae02bf6f8bf7719c0e9b5fe6adb192401cc63742746a63`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:33:49 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:35:29 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 14:35:29 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:35:29 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 14 May 2024 14:35:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:35:29 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:35:29 GMT
CMD []
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4e505122dbc1f983aac993b4ca6ef5ebf66e5028579153055296524292a3db`  
		Last Modified: Tue, 14 May 2024 14:38:01 GMT  
		Size: 64.4 MB (64435763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e69619d9ceaf3c370dba5ae097bcc263cc2ccf927318ecb04396d470d9b587a`  
		Last Modified: Tue, 14 May 2024 14:37:52 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.12` - linux; arm variant v7

```console
$ docker pull varnish@sha256:fa0687bec6fea6cf7e83fb3fe614436e3e9139d4bc9c8877ea098d4e73d7f857
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72868725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c964572fcdcd9d9dc5e5aa7078bbde94c6c97e4c773260b61cf0488addd2c1c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:42:12 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:43:53 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 09:43:53 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:43:54 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 14 May 2024 09:43:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:43:54 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:43:54 GMT
CMD []
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b3bbc395341d12af989d8437a48e7214b56d0ff774ac68d6841e9f002529d1`  
		Last Modified: Tue, 14 May 2024 09:46:03 GMT  
		Size: 46.3 MB (46273530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f4ea3d229a340dd3e1c0eb3141f38e41a03130f9117ddb859192f45a4084b`  
		Last Modified: Tue, 14 May 2024 09:45:57 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.12` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:1e5ace64ba97b9561563d4e78b40e0a27a107bff12fd625042e4e7d00cdc95b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89971366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb033bbd8bf3317c6c6d49cabe4cf210bae5b40cb88bb175802d9d586c7ee94c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:47:45 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:49:08 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 07:49:08 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:49:08 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 14 May 2024 07:49:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:49:09 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:49:09 GMT
CMD []
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfb6d8ae8de1d2328c8bc128ce9023dfe1ea6443a4457c93e7e698baa0e3932`  
		Last Modified: Tue, 14 May 2024 07:51:21 GMT  
		Size: 59.9 MB (59883758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e8860441b3bebdace36c445d58d5404f8c3cbc5c089fccbf7424864241f054`  
		Last Modified: Tue, 14 May 2024 07:51:14 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.12` - linux; 386

```console
$ docker pull varnish@sha256:38fe332649b9cede5eb5d7d34df122260cc756273c12d7ed441ae9d7f2cc4622
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97141733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e584586ad47ef67a8229c562940d0c22abcd09edce10416dc99600a3bed48ae`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:34 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 14 May 2024 00:47:34 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:53:58 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:56:06 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 08:56:07 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:56:07 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 14 May 2024 08:56:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:56:07 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:56:08 GMT
CMD []
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa9a0aab3d0ac25dca15665eeed7f28f375c1841a2ee1366fb40edac755b1f`  
		Last Modified: Tue, 14 May 2024 08:59:13 GMT  
		Size: 64.7 MB (64716991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a6b79ece410cf5cb9170cc02102eaf9d0dc6111956df402e8950dc13dacb0f`  
		Last Modified: Tue, 14 May 2024 08:59:01 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.12` - linux; ppc64le

```console
$ docker pull varnish@sha256:0e68a2ee42b8aaea03b5240348f55514b8d9504fb21a72bb3cebbb14be255281
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94656336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9482372d8899c407789abe7e93a443b832b3dc5c86e2fd69a0a5e71333ed5a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:37:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:40:52 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 06:40:55 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:40:55 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 14 May 2024 06:40:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:40:56 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:40:56 GMT
CMD []
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb67a4eb707a7d93dcab86ddc423edc9cfafb18d5f519ec44f474845c0a2cf7`  
		Last Modified: Tue, 14 May 2024 06:43:32 GMT  
		Size: 59.3 MB (59344479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb6887aea86b4c424d5c24895c15016beabdaabf6418de30ad88585b87e060`  
		Last Modified: Tue, 14 May 2024 06:43:22 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.12` - linux; s390x

```console
$ docker pull varnish@sha256:5b597ec14b5723926972d9d78d6e4885eb3d7f42065d0267f84e98b92bc73496
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76266630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d7910dee3fded5fe6f4e141f09f87b9d33a54f504c79ca8de7d51dbe1ad527`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:43:11 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Tue, 14 May 2024 00:43:13 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:42:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:43:44 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.12.tgz -o $tmpdir/orig.tgz;     echo "d80abb42380e85bc4be02278b3620b0a66d182465945146eecb2cdc022e77945ad815e897a5ed0bec2f458471617f647a80c743c0f72e73334ad92d3ac298af4  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.12|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 06:43:46 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:43:46 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Tue, 14 May 2024 06:43:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:43:46 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:43:46 GMT
CMD []
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bfbc3aa544718c59c905177b1a1c09b56d940266884540b0c674a67548166e`  
		Last Modified: Tue, 14 May 2024 06:45:56 GMT  
		Size: 46.6 MB (46592273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e1a65660f301582de4f5bcb81aa6ff0aebff668eb9b5299885a612583e2f3f`  
		Last Modified: Tue, 14 May 2024 06:45:50 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.13`

```console
$ docker pull varnish@sha256:eb5b5923785da107b84db2f896cc90d654c14ed335123c16fbbf8d8fa17dacc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:6.0.13` - linux; amd64

```console
$ docker pull varnish@sha256:3be84605f51934b662a1fd32c03d982f9235468fdb8427f2d20fa1c8429dc4a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95874783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9aa8a59b93ff62a0d1e53b9cbd4026c35668b03c79c4969bf8746954b5a9fbe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:26:32 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 14:26:32 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 14:26:32 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 14:26:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:28:21 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 14:28:21 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:28:21 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 14:28:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:28:21 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:28:22 GMT
CMD []
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359f8f3a4792f96c1720dfd7f4dd952889d4ab9344eb0fe9413ffffc2229b61a`  
		Last Modified: Tue, 14 May 2024 14:37:03 GMT  
		Size: 64.4 MB (64440136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0385c17efd750567c8ab5fce43768872bc80277f323daa30421423f5c8f598a`  
		Last Modified: Tue, 14 May 2024 14:36:54 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; arm variant v7

```console
$ docker pull varnish@sha256:56f3662203529fca4d1f77533683ba3d50392d0a8e33a7b17d00def46c101b65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72870716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7b9d0eb1054b63a01be7fe1c035340bf0a4ad3c10879eb62f9e0358c60f7fb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:35:00 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 09:35:00 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 09:35:00 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 09:35:00 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:36:47 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 09:36:47 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:36:48 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 09:36:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:36:48 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:36:48 GMT
CMD []
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f106de5cb49a4793119ff373fe3b357fc2eed6a8825ca5516e4b0f113a9271`  
		Last Modified: Tue, 14 May 2024 09:45:13 GMT  
		Size: 46.3 MB (46275509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4360686e3bc89571cb56e34c207bf1c03b274f41f9f0efc016795bf2ee8e822`  
		Last Modified: Tue, 14 May 2024 09:45:07 GMT  
		Size: 714.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a21d622cce0cfc37c7923b5405f569e8d5dd5434cc40583cfd5c6ed71544bd85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89977458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3d300d8903dff396e57d3e6e86b7f065db5cb2c7c0dbbd5e11e34adb97ca23`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:41:33 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 07:41:33 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 07:41:33 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 07:41:33 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:43:01 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 07:43:01 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:43:01 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 07:43:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:43:01 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:43:02 GMT
CMD []
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e142232f2ce3e867f9128875cf61777e5e40c82eb952700a7896f5a16901a0`  
		Last Modified: Tue, 14 May 2024 07:50:31 GMT  
		Size: 59.9 MB (59889832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c0ecccf7b958b1578b188ef2833a7365f17b5a62ba9227b337f41e137076e7`  
		Last Modified: Tue, 14 May 2024 07:50:25 GMT  
		Size: 718.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; 386

```console
$ docker pull varnish@sha256:fae67428c9fbfac1d3bafbb56d810446a2dc60497ac3341f640cfd4a24fd7aeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97146491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1d4b8a8f9c33f0bb44f64d7ad8166752b52f58da7a88086e0cac799831c38`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:34 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 14 May 2024 00:47:34 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:44:30 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 08:44:30 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 08:44:30 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 08:44:30 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:46:47 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 08:46:48 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:46:48 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 08:46:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:46:49 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:46:49 GMT
CMD []
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f907ff471f0851875703285eb6d0ef438811d491aadb5aba748aa312476aeda`  
		Last Modified: Tue, 14 May 2024 08:57:59 GMT  
		Size: 64.7 MB (64721732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18e6804a4d99f5cc0febeea741d31d1ed3388b1f166485bba629841e4a9fc6f`  
		Last Modified: Tue, 14 May 2024 08:57:47 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; ppc64le

```console
$ docker pull varnish@sha256:cdc5925f33e2f3d2766f8f221d3f3dd8ce814a4387b8ce60bbde786d9ba097bc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94661580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98390a649c51397783ed4d8fe780ca0f05dc4f989c8d00aef9ac970fabff2136`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:25:05 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 06:25:05 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 06:25:06 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 06:25:06 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:28:35 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 06:28:38 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:28:38 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 06:28:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:28:38 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:28:39 GMT
CMD []
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dfefba4fba615398a7eab3e3342d67dcf7df7f8e6cac0f28d30001ab1684e5`  
		Last Modified: Tue, 14 May 2024 06:42:28 GMT  
		Size: 59.3 MB (59349704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f01dbfb3e2cfaa17b94584fd9fcb792d0ee168bcb7891a67a3d3d2feae19f5`  
		Last Modified: Tue, 14 May 2024 06:42:18 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; s390x

```console
$ docker pull varnish@sha256:c9887b4336fa3addcaa27879c77b53e03af001a369ad6a8abff832e56c356b56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deacee544cdd187a45643da0b7bc6eeedf17ba7641ea2f1e758deeda3adbd530`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:43:11 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Tue, 14 May 2024 00:43:13 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:36:02 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 06:36:02 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 06:36:02 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 06:36:03 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:37:27 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 06:37:29 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:37:29 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 06:37:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:37:30 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:37:30 GMT
CMD []
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a4866f0e934710827a963ac4a2533e21008525af1ba9fdb2b354138060dd70`  
		Last Modified: Tue, 14 May 2024 06:45:13 GMT  
		Size: 46.6 MB (46596547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8339ee670ce12c69916f24743f49512e75d61dc5c928b10db3b0442836475`  
		Last Modified: Tue, 14 May 2024 06:45:07 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.3`

```console
$ docker pull varnish@sha256:47a924a2a18cfdd424d27e6048ba098cc766d1e5ac64a37d9b113bfe30a5fbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.3` - linux; amd64

```console
$ docker pull varnish@sha256:840b59a4a278d7b1b1fb8e396d1645955f2323d128836e51bd3b4d8f7f331c91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101984755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bd5630d3db4f40c7266a373a1df6125142279fbc8ccb57186023c6b59488fc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:31:08 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 14 May 2024 14:31:08 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 14 May 2024 14:31:08 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 14 May 2024 14:31:08 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 14:31:08 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 14:31:08 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 14 May 2024 14:31:08 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 14 May 2024 14:31:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 14 May 2024 14:31:08 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 14:31:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 14:31:09 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:33:28 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 14:33:29 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:33:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 14:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:33:29 GMT
USER varnish
# Tue, 14 May 2024 14:33:29 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc00d2213dde3d7d2650ac54348f2dc13d90d38bc1750e32a43af1478947640`  
		Last Modified: Tue, 14 May 2024 14:37:42 GMT  
		Size: 70.6 MB (70550332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b218d6209beec6e7cf39a30f489a7a9ba1bcc8e1ae46627f0c239b328ffb90f8`  
		Last Modified: Tue, 14 May 2024 14:37:33 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; arm variant v7

```console
$ docker pull varnish@sha256:60bc79fa00ceba842e64aec40cc1a74d70c155adf827cff332b87f803ccf1bd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78773803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4581aae05f27b46bd7578ed217cf71a26ebac433e7134719f0777e9f6ee848`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:39:33 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 14 May 2024 09:39:33 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 14 May 2024 09:39:33 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 14 May 2024 09:39:33 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 09:39:33 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 09:39:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 14 May 2024 09:39:33 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 14 May 2024 09:39:33 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 14 May 2024 09:39:33 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 09:39:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 09:39:34 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:41:53 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 09:41:54 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:41:55 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 09:41:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:41:55 GMT
USER varnish
# Tue, 14 May 2024 09:41:55 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:41:55 GMT
CMD []
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06e6e93e629fd5434e8b224f55f05bc75cb18a0b3b8babf9206a55e1efcb61b`  
		Last Modified: Tue, 14 May 2024 09:45:47 GMT  
		Size: 52.2 MB (52178819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e14458c5cc104fac659215989150a68536a63f21b5f0be81b5643b96c7c554`  
		Last Modified: Tue, 14 May 2024 09:45:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:427b81b86ba6a896aecdb699a589719ad637b53f64c9673c2e2ae594b6062fc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95810799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ee3b247f9479c43b34078308a02fcc96eeef32f14909f74976cc1306231ca6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:45:36 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 14 May 2024 07:45:36 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 14 May 2024 07:45:36 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 14 May 2024 07:45:36 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 07:45:36 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 07:45:36 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 14 May 2024 07:45:36 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 14 May 2024 07:45:36 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 14 May 2024 07:45:36 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 07:45:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 07:45:36 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:47:39 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 07:47:40 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:47:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 07:47:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:47:40 GMT
USER varnish
# Tue, 14 May 2024 07:47:40 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:47:40 GMT
CMD []
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fddf70dd1cc5d58a1e87267ee0fb20f3c9cc834927d8236f66b6ef48df0982b`  
		Last Modified: Tue, 14 May 2024 07:51:06 GMT  
		Size: 65.7 MB (65723399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d2f6b629bb7bd508e00e50421e914e7a52b475dc96ecf54749da8998ee4549`  
		Last Modified: Tue, 14 May 2024 07:50:59 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; 386

```console
$ docker pull varnish@sha256:86ab4dbf15eac1831811d09c2d94bdac41a17dc17a550e8960ea3b1155e52ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103236938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81919616c20e7db28db7c8a495d3d3782d8d099ccc4b7cb77108ea906da1ec10`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:34 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 14 May 2024 00:47:34 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:50:33 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 14 May 2024 08:50:33 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 14 May 2024 08:50:33 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 14 May 2024 08:50:33 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 08:50:33 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 08:50:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 14 May 2024 08:50:34 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 14 May 2024 08:50:34 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 14 May 2024 08:50:34 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 08:50:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 08:50:34 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:53:49 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 08:53:50 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:53:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 08:53:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:53:50 GMT
USER varnish
# Tue, 14 May 2024 08:53:50 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:53:51 GMT
CMD []
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c6d6b60927d0bcb0940b6b67be8c7e45d3fc6f9476a963b93f26a5e3bca7c1`  
		Last Modified: Tue, 14 May 2024 08:58:51 GMT  
		Size: 70.8 MB (70812403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099d81d2c5250b7d2cb3679a04844e15ab6fec69120bec760409f18767232a33`  
		Last Modified: Tue, 14 May 2024 08:58:38 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; ppc64le

```console
$ docker pull varnish@sha256:99689457d33d5df9c4434faac2e62ed8a095f637c03eb3fe35b4a97eb6c2a83d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100905864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b248e6c2f68cff646346a449c9a28e7de8bf70400068047a278d1e683b3a7889`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:33:12 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 14 May 2024 06:33:13 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 14 May 2024 06:33:13 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 14 May 2024 06:33:13 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 06:33:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 06:33:14 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 14 May 2024 06:33:14 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 14 May 2024 06:33:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 14 May 2024 06:33:15 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 06:33:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:33:15 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:37:43 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 06:37:46 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:37:46 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:37:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:37:47 GMT
USER varnish
# Tue, 14 May 2024 06:37:47 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:37:48 GMT
CMD []
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8aaef1920de56f90d5a026da0944152a7269ee2faf35896c7e26c4be95e61b6`  
		Last Modified: Tue, 14 May 2024 06:43:14 GMT  
		Size: 65.6 MB (65594215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46af03d12d1100630c8cd8c6df50092ca8afe24b6daa52091393b9c44a4b179`  
		Last Modified: Tue, 14 May 2024 06:43:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3` - linux; s390x

```console
$ docker pull varnish@sha256:6ffc1a127711495f20f57080e3c37cf8d598a5142f2c5de8ac595576a95419c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82355230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcba7be8f1f6c597e99bf28a07402eecc7ea4dd7a5277ac1a030f6dc2999153e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:43:11 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Tue, 14 May 2024 00:43:13 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:40:12 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 14 May 2024 06:40:12 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 14 May 2024 06:40:12 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 14 May 2024 06:40:12 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 06:40:12 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 06:40:13 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 14 May 2024 06:40:13 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 14 May 2024 06:40:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 14 May 2024 06:40:13 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 06:40:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:40:13 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:42:11 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 06:42:13 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:42:13 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:42:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:42:14 GMT
USER varnish
# Tue, 14 May 2024 06:42:14 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:42:14 GMT
CMD []
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7287661c2d019f969ad9841f1f016324728cad73e5583075b00b5c169703b088`  
		Last Modified: Tue, 14 May 2024 06:45:43 GMT  
		Size: 52.7 MB (52681082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad54b8e6db238df5224ef40ebb5b383b94f47686b92de602f04b53854a43ec75`  
		Last Modified: Tue, 14 May 2024 06:45:36 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.3-alpine`

```console
$ docker pull varnish@sha256:b478abea651eb4dfe376c3ff327892b21f3d73387aa5c5dee962fbee4df62172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.3-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:a095ad45949e2c813caa344707ce69434d2ba198216501aa0d28989fbc480433
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72969169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8114ab2dd8fd716f52b9bbc5d69ad0828648cdffe840d6234bbb598d584934f1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:59:45 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Sat, 16 Mar 2024 08:59:45 GMT
ARG VARNISH_VERSION=7.3.1
# Sat, 16 Mar 2024 08:59:45 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Sat, 16 Mar 2024 08:59:45 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 08:59:45 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 08:59:45 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Sat, 16 Mar 2024 08:59:45 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Sat, 16 Mar 2024 08:59:45 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Sat, 16 Mar 2024 08:59:45 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 08:59:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 08:59:45 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 09:01:01 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 09:01:02 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 09:01:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 09:01:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 09:01:02 GMT
USER varnish
# Sat, 16 Mar 2024 09:01:02 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 09:01:02 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab4a6d9b11c11ff12974f07c8c12e91b9dd09edeb8d09cdffe13e0920e0d802`  
		Last Modified: Sat, 16 Mar 2024 09:01:52 GMT  
		Size: 69.6 MB (69559944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667a749e39c8cd9e446a977f22d63edabfd3492686ef8e05b78b154f841065fe`  
		Last Modified: Sat, 16 Mar 2024 09:01:43 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:b91962a56b4514ec87d06e92220074f8d013ad1206332fd6971b69f570ea6bbe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57171164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fda5295597faefdc6ec13a195425860999cbbabd7dcb5be0daf9d9b45047f55`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:06:30 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Sat, 16 Mar 2024 06:06:30 GMT
ARG VARNISH_VERSION=7.3.1
# Sat, 16 Mar 2024 06:06:30 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Sat, 16 Mar 2024 06:06:30 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 06:06:30 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 06:06:31 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Sat, 16 Mar 2024 06:06:31 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Sat, 16 Mar 2024 06:06:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Sat, 16 Mar 2024 06:06:31 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 06:06:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 06:06:32 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 06:08:13 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 06:08:13 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 06:08:13 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:08:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 06:08:14 GMT
USER varnish
# Sat, 16 Mar 2024 06:08:14 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 06:08:14 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b89a54b98fc121c9a4daf33241422185d21947cd4dd453265625580a1ffed93`  
		Last Modified: Sat, 16 Mar 2024 06:09:06 GMT  
		Size: 54.3 MB (54251771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d447f32e1d4163f3f9a27022529a62f11426a5ddb815772520246f4510782d15`  
		Last Modified: Sat, 16 Mar 2024 06:08:58 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f021fa214f8baace946da336bf3dc81d1a68ed7bb83c00a2b9dd020215b2a953
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69668817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb5e9c67a0dab76b7f4ef5c2f5c1cbff4c86f6235125ad4f9bf3348028d7b50`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:45:59 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Sat, 16 Mar 2024 02:45:59 GMT
ARG VARNISH_VERSION=7.3.1
# Sat, 16 Mar 2024 02:45:59 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Sat, 16 Mar 2024 02:45:59 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 02:46:00 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 02:46:00 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Sat, 16 Mar 2024 02:46:00 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Sat, 16 Mar 2024 02:46:00 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Sat, 16 Mar 2024 02:46:00 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 02:46:00 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 02:46:00 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 02:47:09 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 02:47:09 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 02:47:09 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 02:47:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 02:47:09 GMT
USER varnish
# Sat, 16 Mar 2024 02:47:10 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 02:47:10 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820dd0bd90f2f2bfcd9357229f79932957a8ac42490ae0fca4073d4415873ca7`  
		Last Modified: Sat, 16 Mar 2024 02:48:00 GMT  
		Size: 66.3 MB (66320604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c8e208ed4baa597825095fb73597159e309cf2d67645283cc8a618cdfbb89`  
		Last Modified: Sat, 16 Mar 2024 02:47:54 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; 386

```console
$ docker pull varnish@sha256:52d8ea4b641d7a0eb00f3a0a988ce534e9a4e28a00768bb59fb14a07d2c7a94f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74997198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3693c10d194ae32738e91675d4fa6b43a83ae71f04cfcea1a0179324fa2fab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:13:14 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Sat, 16 Mar 2024 05:13:14 GMT
ARG VARNISH_VERSION=7.3.1
# Sat, 16 Mar 2024 05:13:14 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Sat, 16 Mar 2024 05:13:14 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 05:13:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 05:13:15 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Sat, 16 Mar 2024 05:13:15 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Sat, 16 Mar 2024 05:13:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Sat, 16 Mar 2024 05:13:15 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 05:13:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 05:13:15 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 05:15:17 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 05:15:17 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 05:15:17 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:15:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 05:15:18 GMT
USER varnish
# Sat, 16 Mar 2024 05:15:18 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 05:15:18 GMT
CMD []
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8dcc24e55bff74aca2a176980ef9ad3ef4243bb53a41ddb655d978f4b19f56`  
		Last Modified: Sat, 16 Mar 2024 05:16:17 GMT  
		Size: 71.8 MB (71752612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c956650092a3ae50bd09ced43e457024960ac5c1ef5db31ce4831c40ac2a8629`  
		Last Modified: Sat, 16 Mar 2024 05:16:04 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:fb71aaf8f3a99ff2c5e6be20f4c821ba2e4eb9d006fab7e250466d278172a1fa
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70483010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd67926a1b24102e88fc0cc19d2d5c7237dcfdcfbaa38978e00a4439ebc106ff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:06:48 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Sat, 16 Mar 2024 07:06:48 GMT
ARG VARNISH_VERSION=7.3.1
# Sat, 16 Mar 2024 07:06:48 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Sat, 16 Mar 2024 07:06:49 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 07:06:49 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 07:06:49 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Sat, 16 Mar 2024 07:06:50 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Sat, 16 Mar 2024 07:06:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Sat, 16 Mar 2024 07:06:50 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 07:06:50 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 07:06:51 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 07:08:14 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 07:08:16 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 07:08:16 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:08:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 07:08:17 GMT
USER varnish
# Sat, 16 Mar 2024 07:08:17 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 07:08:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0d6e340b3961406c2073611ffaa7548daf4548033aa404e217a8bbb5b73f88`  
		Last Modified: Sat, 16 Mar 2024 07:09:16 GMT  
		Size: 67.1 MB (67124160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fb58b7899506143b4976f256e27c810f46a5a2f50a93829f42d4f7e55c5e1c`  
		Last Modified: Sat, 16 Mar 2024 07:09:06 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ca83178c077f007d926a677a688439b64b7251d5fd70a6d1bba7f076e942366a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64856101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765f6cadd76addc7d2cda676679b3f15272966d50a3e986be7bdac16dcd7c5de`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 23:06:26 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Sat, 16 Mar 2024 23:06:26 GMT
ARG VARNISH_VERSION=7.3.1
# Sat, 16 Mar 2024 23:06:27 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Sat, 16 Mar 2024 23:06:27 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 23:06:27 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 23:06:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Sat, 16 Mar 2024 23:06:27 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Sat, 16 Mar 2024 23:06:27 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Sat, 16 Mar 2024 23:06:27 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 23:06:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 23:06:28 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 23:07:54 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 23:07:56 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 23:07:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 23:07:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 23:07:56 GMT
USER varnish
# Sat, 16 Mar 2024 23:07:56 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 23:07:57 GMT
CMD []
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fc0a6b4f05ea4ca23e76482563e821f3f0810f377876de06c5e6a3c5b183d6`  
		Last Modified: Sat, 16 Mar 2024 23:11:15 GMT  
		Size: 61.6 MB (61612967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ae77898131bdebf8ccce60090b516eb3aaa58e41639d5e20791e094ef328f6`  
		Last Modified: Sat, 16 Mar 2024 23:11:07 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.3.1`

```console
$ docker pull varnish@sha256:47a924a2a18cfdd424d27e6048ba098cc766d1e5ac64a37d9b113bfe30a5fbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.3.1` - linux; amd64

```console
$ docker pull varnish@sha256:840b59a4a278d7b1b1fb8e396d1645955f2323d128836e51bd3b4d8f7f331c91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101984755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bd5630d3db4f40c7266a373a1df6125142279fbc8ccb57186023c6b59488fc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:31:08 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 14 May 2024 14:31:08 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 14 May 2024 14:31:08 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 14 May 2024 14:31:08 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 14:31:08 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 14:31:08 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 14 May 2024 14:31:08 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 14 May 2024 14:31:08 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 14 May 2024 14:31:08 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 14:31:08 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 14:31:09 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:33:28 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 14:33:29 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:33:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 14:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:33:29 GMT
USER varnish
# Tue, 14 May 2024 14:33:29 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc00d2213dde3d7d2650ac54348f2dc13d90d38bc1750e32a43af1478947640`  
		Last Modified: Tue, 14 May 2024 14:37:42 GMT  
		Size: 70.6 MB (70550332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b218d6209beec6e7cf39a30f489a7a9ba1bcc8e1ae46627f0c239b328ffb90f8`  
		Last Modified: Tue, 14 May 2024 14:37:33 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1` - linux; arm variant v7

```console
$ docker pull varnish@sha256:60bc79fa00ceba842e64aec40cc1a74d70c155adf827cff332b87f803ccf1bd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78773803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4581aae05f27b46bd7578ed217cf71a26ebac433e7134719f0777e9f6ee848`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:39:33 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 14 May 2024 09:39:33 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 14 May 2024 09:39:33 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 14 May 2024 09:39:33 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 09:39:33 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 09:39:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 14 May 2024 09:39:33 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 14 May 2024 09:39:33 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 14 May 2024 09:39:33 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 09:39:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 09:39:34 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:41:53 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 09:41:54 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:41:55 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 09:41:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:41:55 GMT
USER varnish
# Tue, 14 May 2024 09:41:55 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:41:55 GMT
CMD []
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06e6e93e629fd5434e8b224f55f05bc75cb18a0b3b8babf9206a55e1efcb61b`  
		Last Modified: Tue, 14 May 2024 09:45:47 GMT  
		Size: 52.2 MB (52178819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e14458c5cc104fac659215989150a68536a63f21b5f0be81b5643b96c7c554`  
		Last Modified: Tue, 14 May 2024 09:45:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:427b81b86ba6a896aecdb699a589719ad637b53f64c9673c2e2ae594b6062fc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95810799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ee3b247f9479c43b34078308a02fcc96eeef32f14909f74976cc1306231ca6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:45:36 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 14 May 2024 07:45:36 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 14 May 2024 07:45:36 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 14 May 2024 07:45:36 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 07:45:36 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 07:45:36 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 14 May 2024 07:45:36 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 14 May 2024 07:45:36 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 14 May 2024 07:45:36 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 07:45:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 07:45:36 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:47:39 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 07:47:40 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:47:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 07:47:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:47:40 GMT
USER varnish
# Tue, 14 May 2024 07:47:40 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:47:40 GMT
CMD []
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fddf70dd1cc5d58a1e87267ee0fb20f3c9cc834927d8236f66b6ef48df0982b`  
		Last Modified: Tue, 14 May 2024 07:51:06 GMT  
		Size: 65.7 MB (65723399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d2f6b629bb7bd508e00e50421e914e7a52b475dc96ecf54749da8998ee4549`  
		Last Modified: Tue, 14 May 2024 07:50:59 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1` - linux; 386

```console
$ docker pull varnish@sha256:86ab4dbf15eac1831811d09c2d94bdac41a17dc17a550e8960ea3b1155e52ca4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103236938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81919616c20e7db28db7c8a495d3d3782d8d099ccc4b7cb77108ea906da1ec10`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:34 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 14 May 2024 00:47:34 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:50:33 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 14 May 2024 08:50:33 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 14 May 2024 08:50:33 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 14 May 2024 08:50:33 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 08:50:33 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 08:50:33 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 14 May 2024 08:50:34 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 14 May 2024 08:50:34 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 14 May 2024 08:50:34 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 08:50:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 08:50:34 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:53:49 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 08:53:50 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:53:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 08:53:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:53:50 GMT
USER varnish
# Tue, 14 May 2024 08:53:50 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:53:51 GMT
CMD []
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c6d6b60927d0bcb0940b6b67be8c7e45d3fc6f9476a963b93f26a5e3bca7c1`  
		Last Modified: Tue, 14 May 2024 08:58:51 GMT  
		Size: 70.8 MB (70812403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099d81d2c5250b7d2cb3679a04844e15ab6fec69120bec760409f18767232a33`  
		Last Modified: Tue, 14 May 2024 08:58:38 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1` - linux; ppc64le

```console
$ docker pull varnish@sha256:99689457d33d5df9c4434faac2e62ed8a095f637c03eb3fe35b4a97eb6c2a83d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100905864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b248e6c2f68cff646346a449c9a28e7de8bf70400068047a278d1e683b3a7889`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:33:12 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 14 May 2024 06:33:13 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 14 May 2024 06:33:13 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 14 May 2024 06:33:13 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 06:33:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 06:33:14 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 14 May 2024 06:33:14 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 14 May 2024 06:33:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 14 May 2024 06:33:15 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 06:33:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:33:15 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:37:43 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 06:37:46 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:37:46 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:37:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:37:47 GMT
USER varnish
# Tue, 14 May 2024 06:37:47 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:37:48 GMT
CMD []
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8aaef1920de56f90d5a026da0944152a7269ee2faf35896c7e26c4be95e61b6`  
		Last Modified: Tue, 14 May 2024 06:43:14 GMT  
		Size: 65.6 MB (65594215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46af03d12d1100630c8cd8c6df50092ca8afe24b6daa52091393b9c44a4b179`  
		Last Modified: Tue, 14 May 2024 06:43:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1` - linux; s390x

```console
$ docker pull varnish@sha256:6ffc1a127711495f20f57080e3c37cf8d598a5142f2c5de8ac595576a95419c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82355230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcba7be8f1f6c597e99bf28a07402eecc7ea4dd7a5277ac1a030f6dc2999153e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:43:11 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Tue, 14 May 2024 00:43:13 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:40:12 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Tue, 14 May 2024 06:40:12 GMT
ARG VARNISH_VERSION=7.3.1
# Tue, 14 May 2024 06:40:12 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Tue, 14 May 2024 06:40:12 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 06:40:12 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 06:40:13 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Tue, 14 May 2024 06:40:13 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Tue, 14 May 2024 06:40:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Tue, 14 May 2024 06:40:13 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 06:40:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:40:13 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:42:11 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 712667312304cbb1798f131caa0a98b7697a2cd9;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.3.1.tgz -o $tmpdir/orig.tgz;     echo "57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 06:42:13 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:42:13 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:42:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:42:14 GMT
USER varnish
# Tue, 14 May 2024 06:42:14 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:42:14 GMT
CMD []
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7287661c2d019f969ad9841f1f016324728cad73e5583075b00b5c169703b088`  
		Last Modified: Tue, 14 May 2024 06:45:43 GMT  
		Size: 52.7 MB (52681082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad54b8e6db238df5224ef40ebb5b383b94f47686b92de602f04b53854a43ec75`  
		Last Modified: Tue, 14 May 2024 06:45:36 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.3.1-alpine`

```console
$ docker pull varnish@sha256:b478abea651eb4dfe376c3ff327892b21f3d73387aa5c5dee962fbee4df62172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.3.1-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:a095ad45949e2c813caa344707ce69434d2ba198216501aa0d28989fbc480433
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72969169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8114ab2dd8fd716f52b9bbc5d69ad0828648cdffe840d6234bbb598d584934f1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:59:45 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Sat, 16 Mar 2024 08:59:45 GMT
ARG VARNISH_VERSION=7.3.1
# Sat, 16 Mar 2024 08:59:45 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Sat, 16 Mar 2024 08:59:45 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 08:59:45 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 08:59:45 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Sat, 16 Mar 2024 08:59:45 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Sat, 16 Mar 2024 08:59:45 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Sat, 16 Mar 2024 08:59:45 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 08:59:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 08:59:45 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 09:01:01 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 09:01:02 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 09:01:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 09:01:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 09:01:02 GMT
USER varnish
# Sat, 16 Mar 2024 09:01:02 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 09:01:02 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab4a6d9b11c11ff12974f07c8c12e91b9dd09edeb8d09cdffe13e0920e0d802`  
		Last Modified: Sat, 16 Mar 2024 09:01:52 GMT  
		Size: 69.6 MB (69559944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667a749e39c8cd9e446a977f22d63edabfd3492686ef8e05b78b154f841065fe`  
		Last Modified: Sat, 16 Mar 2024 09:01:43 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:b91962a56b4514ec87d06e92220074f8d013ad1206332fd6971b69f570ea6bbe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57171164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fda5295597faefdc6ec13a195425860999cbbabd7dcb5be0daf9d9b45047f55`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:06:30 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Sat, 16 Mar 2024 06:06:30 GMT
ARG VARNISH_VERSION=7.3.1
# Sat, 16 Mar 2024 06:06:30 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Sat, 16 Mar 2024 06:06:30 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 06:06:30 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 06:06:31 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Sat, 16 Mar 2024 06:06:31 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Sat, 16 Mar 2024 06:06:31 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Sat, 16 Mar 2024 06:06:31 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 06:06:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 06:06:32 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 06:08:13 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 06:08:13 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 06:08:13 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:08:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 06:08:14 GMT
USER varnish
# Sat, 16 Mar 2024 06:08:14 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 06:08:14 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b89a54b98fc121c9a4daf33241422185d21947cd4dd453265625580a1ffed93`  
		Last Modified: Sat, 16 Mar 2024 06:09:06 GMT  
		Size: 54.3 MB (54251771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d447f32e1d4163f3f9a27022529a62f11426a5ddb815772520246f4510782d15`  
		Last Modified: Sat, 16 Mar 2024 06:08:58 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f021fa214f8baace946da336bf3dc81d1a68ed7bb83c00a2b9dd020215b2a953
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69668817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb5e9c67a0dab76b7f4ef5c2f5c1cbff4c86f6235125ad4f9bf3348028d7b50`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:45:59 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Sat, 16 Mar 2024 02:45:59 GMT
ARG VARNISH_VERSION=7.3.1
# Sat, 16 Mar 2024 02:45:59 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Sat, 16 Mar 2024 02:45:59 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 02:46:00 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 02:46:00 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Sat, 16 Mar 2024 02:46:00 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Sat, 16 Mar 2024 02:46:00 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Sat, 16 Mar 2024 02:46:00 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 02:46:00 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 02:46:00 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 02:47:09 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 02:47:09 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 02:47:09 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 02:47:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 02:47:09 GMT
USER varnish
# Sat, 16 Mar 2024 02:47:10 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 02:47:10 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820dd0bd90f2f2bfcd9357229f79932957a8ac42490ae0fca4073d4415873ca7`  
		Last Modified: Sat, 16 Mar 2024 02:48:00 GMT  
		Size: 66.3 MB (66320604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c8e208ed4baa597825095fb73597159e309cf2d67645283cc8a618cdfbb89`  
		Last Modified: Sat, 16 Mar 2024 02:47:54 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1-alpine` - linux; 386

```console
$ docker pull varnish@sha256:52d8ea4b641d7a0eb00f3a0a988ce534e9a4e28a00768bb59fb14a07d2c7a94f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74997198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3693c10d194ae32738e91675d4fa6b43a83ae71f04cfcea1a0179324fa2fab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:13:14 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Sat, 16 Mar 2024 05:13:14 GMT
ARG VARNISH_VERSION=7.3.1
# Sat, 16 Mar 2024 05:13:14 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Sat, 16 Mar 2024 05:13:14 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 05:13:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 05:13:15 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Sat, 16 Mar 2024 05:13:15 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Sat, 16 Mar 2024 05:13:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Sat, 16 Mar 2024 05:13:15 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 05:13:15 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 05:13:15 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 05:15:17 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 05:15:17 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 05:15:17 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:15:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 05:15:18 GMT
USER varnish
# Sat, 16 Mar 2024 05:15:18 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 05:15:18 GMT
CMD []
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8dcc24e55bff74aca2a176980ef9ad3ef4243bb53a41ddb655d978f4b19f56`  
		Last Modified: Sat, 16 Mar 2024 05:16:17 GMT  
		Size: 71.8 MB (71752612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c956650092a3ae50bd09ced43e457024960ac5c1ef5db31ce4831c40ac2a8629`  
		Last Modified: Sat, 16 Mar 2024 05:16:04 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:fb71aaf8f3a99ff2c5e6be20f4c821ba2e4eb9d006fab7e250466d278172a1fa
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70483010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd67926a1b24102e88fc0cc19d2d5c7237dcfdcfbaa38978e00a4439ebc106ff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:06:48 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Sat, 16 Mar 2024 07:06:48 GMT
ARG VARNISH_VERSION=7.3.1
# Sat, 16 Mar 2024 07:06:48 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Sat, 16 Mar 2024 07:06:49 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 07:06:49 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 07:06:49 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Sat, 16 Mar 2024 07:06:50 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Sat, 16 Mar 2024 07:06:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Sat, 16 Mar 2024 07:06:50 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 07:06:50 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 07:06:51 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 07:08:14 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 07:08:16 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 07:08:16 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:08:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 07:08:17 GMT
USER varnish
# Sat, 16 Mar 2024 07:08:17 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 07:08:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0d6e340b3961406c2073611ffaa7548daf4548033aa404e217a8bbb5b73f88`  
		Last Modified: Sat, 16 Mar 2024 07:09:16 GMT  
		Size: 67.1 MB (67124160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fb58b7899506143b4976f256e27c810f46a5a2f50a93829f42d4f7e55c5e1c`  
		Last Modified: Sat, 16 Mar 2024 07:09:06 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.3.1-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ca83178c077f007d926a677a688439b64b7251d5fd70a6d1bba7f076e942366a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64856101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765f6cadd76addc7d2cda676679b3f15272966d50a3e986be7bdac16dcd7c5de`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 23:06:26 GMT
ARG PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9
# Sat, 16 Mar 2024 23:06:26 GMT
ARG VARNISH_VERSION=7.3.1
# Sat, 16 Mar 2024 23:06:27 GMT
ARG DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d
# Sat, 16 Mar 2024 23:06:27 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 23:06:27 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 23:06:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0
# Sat, 16 Mar 2024 23:06:27 GMT
ARG VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0
# Sat, 16 Mar 2024 23:06:27 GMT
ARG VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de
# Sat, 16 Mar 2024 23:06:27 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 23:06:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 23:06:28 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 23:07:54 GMT
# ARGS: DIST_SHA512=57de14ff47038752a151b704d7f629438bba74e258e7d88c6ca58e8a10bfc89368f36b7f32d5525ff032033d941f3e48dde5ae090e44ca928110d2eeb1db589d PKG_COMMIT=712667312304cbb1798f131caa0a98b7697a2cd9 TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.3.1 VMOD_DYNAMIC_COMMIT=af9c51cb53982b42eed6116960015c09171838b0 VMOD_DYNAMIC_SHA512SUM=4a91de4a1fc3e6eb925ac5e8c9d56d9786c368fbbb3b957285bd0edf4e955ee19ad1ee6b4b3c4754cf5885be6593c269419c19fea36760513397d92085e105de VMOD_DYNAMIC_VERSION=2.8.0
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 23:07:56 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 23:07:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 23:07:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 23:07:56 GMT
USER varnish
# Sat, 16 Mar 2024 23:07:56 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 23:07:57 GMT
CMD []
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fc0a6b4f05ea4ca23e76482563e821f3f0810f377876de06c5e6a3c5b183d6`  
		Last Modified: Sat, 16 Mar 2024 23:11:15 GMT  
		Size: 61.6 MB (61612967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ae77898131bdebf8ccce60090b516eb3aaa58e41639d5e20791e094ef328f6`  
		Last Modified: Sat, 16 Mar 2024 23:11:07 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.4`

```console
$ docker pull varnish@sha256:882224e47d7db63a17dce924bf9033b5181a2a3a0fedee09e9aa40c0207f9ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.4` - linux; amd64

```console
$ docker pull varnish@sha256:b8370ea0069c03b3b14ae335d01ac6fe9c1a2416cb58a04374c7a05f794f5696
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134784916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a18216991f6a1afd692fb5920e9d02abf542c16b6d2d673ee4dcd3b155a3d5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:17:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 14:20:43 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 14:20:43 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 14:20:43 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 14:20:43 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 14:20:43 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 14:20:43 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 14:20:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 14:20:44 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 14:20:44 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 14:20:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:26:17 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 14:26:18 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:26:18 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 14:26:18 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 14:26:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:26:18 GMT
USER varnish
# Tue, 14 May 2024 14:26:18 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:26:18 GMT
CMD []
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a16974ae153bf113b00ccc0fbf36aac224d2dc680479303298885c6dc18e369`  
		Last Modified: Tue, 14 May 2024 14:36:43 GMT  
		Size: 105.6 MB (105632491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5013aecdda5901d37096b63257c04c84531732b0b32bc00be4f8adb51cbd503`  
		Last Modified: Tue, 14 May 2024 14:36:29 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6d6e7a17e4ee13e1459b04a4a679c4d3ba359f49edf76e98919f4cbbab2b27`  
		Last Modified: Tue, 14 May 2024 14:36:29 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4` - linux; arm variant v7

```console
$ docker pull varnish@sha256:4583809dc8bdcc3a40334d41ed24522463163aaae73022d6f0c53e4f89ea0fc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105004879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68a526a0cb0674dac743036b5c1580beec513788e0155f2ef8a489808be285d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:29:26 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 09:32:20 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 09:32:21 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 09:32:21 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 09:32:21 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 09:32:21 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 09:32:21 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 09:32:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 09:32:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 09:32:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 09:32:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:34:47 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 09:34:48 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:34:48 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 09:34:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 09:34:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:34:49 GMT
USER varnish
# Tue, 14 May 2024 09:34:49 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:34:49 GMT
CMD []
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d2699d7174ee2e3ec604bfeb786dd77e9eedf5d0a48877a3273f650c5077c0`  
		Last Modified: Tue, 14 May 2024 09:44:56 GMT  
		Size: 80.3 MB (80262661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60f9712404c431a4fd8b84805e3a650f223a1422c848b02681e410bb739754`  
		Last Modified: Tue, 14 May 2024 09:44:44 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fa61b2a01fe31985e791b88be9e0288fd610dde76d73b68f1426b2887fecdc`  
		Last Modified: Tue, 14 May 2024 09:44:44 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:2ac2a3ad2e8ef37460b50bf8ae3afefbee38523eb0aaee01f7d6a5e2c3fdb3b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129270960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e44b842694bd08afb5258b5ecd852a0b2b78d9a72bca12ea1cda6a774488be5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:36:27 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 07:39:07 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 07:39:07 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 07:39:07 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 07:39:07 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 07:39:07 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 07:39:07 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 07:39:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 07:39:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 07:39:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 07:39:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:41:14 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 07:41:16 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:41:16 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 07:41:16 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 07:41:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:41:16 GMT
USER varnish
# Tue, 14 May 2024 07:41:16 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:41:16 GMT
CMD []
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048b118ca13512abdb6cfc328a5341657e791ccb3ab8790a8f2b12ac3c31d858`  
		Last Modified: Tue, 14 May 2024 07:50:14 GMT  
		Size: 100.1 MB (100089445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eebca74f010bc1af9b8dda398fbc899b6407212646e1cf52d00a5b8b55b03ab`  
		Last Modified: Tue, 14 May 2024 07:50:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0ff9860e00c9b930e05109dc282db9d300a0457af0d0c59351d49ec164ba61`  
		Last Modified: Tue, 14 May 2024 07:50:02 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4` - linux; 386

```console
$ docker pull varnish@sha256:1a9742bfb4ce30721c6ca2fb5520c15305d749e160ec5611cd50e8790eebc63e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131930287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bc76427f2017543e41070e746fc91d73dfb0c21a092175637a91b6bc9d2874`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:36:55 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 08:40:50 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 08:40:50 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 08:40:50 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 08:40:50 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 08:40:50 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 08:40:50 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 08:40:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 08:40:51 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 08:40:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 08:40:51 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:44:17 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 08:44:18 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:44:18 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 08:44:18 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 08:44:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:44:19 GMT
USER varnish
# Tue, 14 May 2024 08:44:19 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:44:19 GMT
CMD []
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc2369f33a43201c69e5e6ad92aeac3ded2c005a5c3706aeb78ba01830e5a63`  
		Last Modified: Tue, 14 May 2024 08:57:36 GMT  
		Size: 101.8 MB (101765638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bd0d0328766529f5a2016fa7b7ec510ffecc1ba0cab060ed4fef646c928e15`  
		Last Modified: Tue, 14 May 2024 08:57:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2f2768da2b8d37692d1c75568c404df85dc71979e9d7d8853eb282addf1d86`  
		Last Modified: Tue, 14 May 2024 08:57:14 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4` - linux; ppc64le

```console
$ docker pull varnish@sha256:3ab6c8b9e140978901343919b2cace41958092e19e671810122ebce933b12a76
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137714757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972cca6f54c3a511281a9ebc05c802367bd39316298842c4b6183435f736ff97`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:16:10 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:20:38 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 06:20:38 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 06:20:38 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 06:20:38 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 06:20:39 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:20:39 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 06:20:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 06:20:39 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:20:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:20:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:24:45 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:24:50 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:24:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:24:50 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:24:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:24:51 GMT
USER varnish
# Tue, 14 May 2024 06:24:51 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:24:51 GMT
CMD []
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426fac7e303070a52e77a623a26e18a04b9bc1ed6c91073683d85327b983ef85`  
		Last Modified: Tue, 14 May 2024 06:42:06 GMT  
		Size: 104.6 MB (104571587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320391667901aac1e14c6f05c8a445467f80196650c05b69b226e68c2c048887`  
		Last Modified: Tue, 14 May 2024 06:41:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b06fc6a3aab74a784600134ec69349d5cd9892a1c4fb30280e0e7c4f049882`  
		Last Modified: Tue, 14 May 2024 06:41:49 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4` - linux; s390x

```console
$ docker pull varnish@sha256:db3133a8388660ac154a58e136a49b0065223533421dd29486e98dc39ca9df22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112365129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7434c2abce66b312ebf0f4009a2e2d2111a9257362cefabd0f244b26fc9ab3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:30:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:33:31 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 06:33:31 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 06:33:31 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 06:33:31 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 06:33:31 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:33:32 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 06:33:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 06:33:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:33:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:33:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:35:41 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:35:44 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:35:44 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:35:45 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:35:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:35:45 GMT
USER varnish
# Tue, 14 May 2024 06:35:45 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:35:45 GMT
CMD []
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df8730d37f1330b10295cfd34b8376a58bc64bf2d8198e0b45334700003fbd6`  
		Last Modified: Tue, 14 May 2024 06:44:59 GMT  
		Size: 84.9 MB (84850723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f69700bb9b4d260724360cb436e12ef933d83342415b05dab002efb950930f`  
		Last Modified: Tue, 14 May 2024 06:44:47 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffb8a880c88bb62724629c502991052f5d79ccd0f05d405bc80a52b9c53e738`  
		Last Modified: Tue, 14 May 2024 06:44:47 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.4-alpine`

```console
$ docker pull varnish@sha256:2c6ab5471f574fd6cdb1b89da00b72ba870512959529d43c648fec5ff81a2322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.4-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:bad41538a520c7324ae66672afcd1843244ff3fd6a69dc186fffabb26e5e5b3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73111717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fcd1daa5a1fd515be57af3744ca44fd77a3aff504e0813f18881ba362df461`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:58:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 20:06:43 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 20:06:43 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 20:06:44 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 20:06:44 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 20:06:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 20:08:04 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 20:08:04 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 20:08:04 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 20:08:05 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 20:08:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 20:08:05 GMT
USER varnish
# Tue, 19 Mar 2024 20:08:05 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 20:08:05 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e88fbcf523fb9f70c926ce56e3d01391ed2c58556c7fed0504edee8f38f1599`  
		Last Modified: Tue, 19 Mar 2024 20:12:02 GMT  
		Size: 69.7 MB (69700966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73d56dea7353d1ce78b162cf126e47cb61ed2436148992e6973adba9df7a26f`  
		Last Modified: Tue, 19 Mar 2024 20:11:53 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d86a9601c89cd35fb0e08c0495b786d5c0fd08804adbc6cf16ceabede21ed6`  
		Last Modified: Tue, 19 Mar 2024 20:11:53 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d8d8d456b3b22b0a1717e09faa1a04161ca2b812536f9fcc981531f8ada51710
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57316383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31c572f46d3e2f829a48ec29edf234b8908aff261f843e8008c27792c881c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:04:36 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:25:16 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 19:25:16 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 19:25:17 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 19:25:17 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 19:25:18 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:25:18 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 19:25:18 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 19:25:19 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:25:19 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:25:19 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:27:54 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 19:27:55 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:27:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:27:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:27:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:27:57 GMT
USER varnish
# Tue, 19 Mar 2024 19:27:57 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:27:58 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb32a9d2bc9510faba817c92bfe1cf189ad3cfd884457c74f7933aed86df6eb`  
		Last Modified: Tue, 19 Mar 2024 19:33:10 GMT  
		Size: 54.4 MB (54395458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001be72dd77327edce535297b918c11d2092b608be216951ffe22e818dd361d1`  
		Last Modified: Tue, 19 Mar 2024 19:33:02 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02b8aa68970246d2ae92e63dd681f9788e02bb390ef1e86b69bd42087bca281`  
		Last Modified: Tue, 19 Mar 2024 19:33:02 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:479ea6daf1d1ddb36de834aa28c5e64c8a4883f743eed493192255ce9f795df1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69813716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be2438e6775bff4a85bde81ac5d9c06ac7d183b8d6ce2edea5db9b89655cc4c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:44:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 18:57:04 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 18:57:04 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:57:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 18:57:04 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 18:58:12 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 18:58:12 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 18:58:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 18:58:13 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 18:58:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 18:58:13 GMT
USER varnish
# Tue, 19 Mar 2024 18:58:13 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 18:58:13 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894a7285b926312b215684e50114187e34f58603947ba360a068c707e8c90cfd`  
		Last Modified: Tue, 19 Mar 2024 19:01:30 GMT  
		Size: 66.5 MB (66463974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf21108d62a7fd3c9304838a0e7d38d87a8b2aaea9be4002b48b0debcfb122a`  
		Last Modified: Tue, 19 Mar 2024 19:01:24 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b1b0f8e8b6fe88f280d6f8a38df3be1e85d89988fb2386fb5a8b6b171772d3`  
		Last Modified: Tue, 19 Mar 2024 19:01:24 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4-alpine` - linux; 386

```console
$ docker pull varnish@sha256:1fdf700b9bf5114292511d5f9b8410f030a420195edc7822ff168350517f134e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75135148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f375513ff93e5dcf88d1563c073de2cbed2e3d5b7d77236f1550cd1af8c6a4be`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:10:49 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:04:13 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 19:04:13 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 19:04:13 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 19:04:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 19:04:14 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:04:14 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 19:04:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 19:04:14 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:04:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:04:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:06:19 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 19:06:19 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:06:19 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:06:19 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:06:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:06:20 GMT
USER varnish
# Tue, 19 Mar 2024 19:06:20 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:06:20 GMT
CMD []
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a30e445c3604537fdf8df8c22a060202d20489b8eddfa77f4550fe4f911650`  
		Last Modified: Tue, 19 Mar 2024 19:11:11 GMT  
		Size: 71.9 MB (71889037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4152d250362e0e5bf5357d66457786d213f1d15255388a3bb7c01c3f2052d5`  
		Last Modified: Tue, 19 Mar 2024 19:10:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2737032c6f8bcdf0a71d104e82734a6b69555856e39ecff4ef201d8b391fd949`  
		Last Modified: Tue, 19 Mar 2024 19:10:57 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:cbcdf4a72047647d6e472f95a475d99778629b31fa07a868c0e8f6ee6c329013
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70642273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817de67047306f66d083abae50517fcfa5851ece50b2da689d6cbb59802870bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:04:51 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:44:28 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 19:44:29 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 19:44:29 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 19:44:29 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 19:44:30 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:44:30 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 19:44:30 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 19:44:30 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:44:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:44:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:45:51 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 19:45:54 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:45:54 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:45:54 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:45:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:45:55 GMT
USER varnish
# Tue, 19 Mar 2024 19:45:55 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743250632b3e83457d746dd80c83c1792da89dcac7861cfbe4e0ced8ff47f129`  
		Last Modified: Tue, 19 Mar 2024 19:51:43 GMT  
		Size: 67.3 MB (67281893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9d99e7af2f3afb5934553c41f70a80f5fa99509365d3f33bebb6089dcd9461`  
		Last Modified: Tue, 19 Mar 2024 19:51:33 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f77c02b1d17e9e7dcf8169ca83ef8b3325640b7d59994287907bad7312790`  
		Last Modified: Tue, 19 Mar 2024 19:51:33 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:1b30229155355ad2c6b66e8e72eddc263f19d9cd02ea6017fa667301d5a27b85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65011686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697ae126a2c8542caeb132c89923bbb9ac0034c03f83099f8fd649c1782a34a3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 23:02:20 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:29:26 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 19:29:27 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 19:29:27 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:29:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:29:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:30:52 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 19:30:54 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:30:54 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:30:55 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:30:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:30:55 GMT
USER varnish
# Tue, 19 Mar 2024 19:30:55 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:30:55 GMT
CMD []
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe38f977ea67683ee4420495875859583d5281a008b4d6aed6e1d588f2f0806`  
		Last Modified: Tue, 19 Mar 2024 19:35:51 GMT  
		Size: 61.8 MB (61767029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c60b2806d71370deb7439b9951f3eb3c198692c33e1f8286d755dc93bdbee9`  
		Last Modified: Tue, 19 Mar 2024 19:35:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d1a215e014825ed08ff1940cdbfc607d4163f6608a016f2cca535243352213`  
		Last Modified: Tue, 19 Mar 2024 19:35:44 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.4.2`

```console
$ docker pull varnish@sha256:2abda59b186a226d89d54f96da3f40f4a3a9fdb053bddebea0c7e85d2d729fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.4.2` - linux; amd64

```console
$ docker pull varnish@sha256:b78591423a0a9eb425f943d520c5000653106cd31da8c8ed8370b20ae953988c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134764332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332fad1a37eb7dc6a914582a75fe93ad09df715919811b015933bfac382f9a3d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:17:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 14:28:26 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 14 May 2024 14:28:26 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 14 May 2024 14:28:26 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 14:28:26 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 14:28:26 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 14:28:26 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 14:28:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 14:28:27 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 14:28:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 14:28:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:30:52 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 14:30:53 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:30:53 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 14:30:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:30:53 GMT
USER varnish
# Tue, 14 May 2024 14:30:53 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:30:53 GMT
CMD []
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ce11243eebf7ebabe057b685bb57522ec2c42910da33f99f6eb3d250d6de6f`  
		Last Modified: Tue, 14 May 2024 14:37:26 GMT  
		Size: 105.6 MB (105613429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6853fe6bda9010f381617fbab53cf6c172dbc197dd76a796fb1e404ca18d1a7`  
		Last Modified: Tue, 14 May 2024 14:37:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2` - linux; arm variant v7

```console
$ docker pull varnish@sha256:fc9f5713824dfb880badcf8e92978822b3b5fc22e459d76ab9a8e1423bfe6c51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105012771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9d2e0e3d501996e80593d2f095be5b35b21966a61891483ec3c56990525605`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:29:26 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 09:36:53 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 14 May 2024 09:36:53 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 14 May 2024 09:36:53 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 09:36:53 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 09:36:53 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 09:36:53 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 09:36:54 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 09:36:54 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 09:36:54 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 09:36:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:39:19 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 09:39:20 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:39:20 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 09:39:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:39:20 GMT
USER varnish
# Tue, 14 May 2024 09:39:20 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:39:20 GMT
CMD []
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06819d00b1552ddf548edb3f86d80a953db214a4230220c2fc6c84b9ce1fee9f`  
		Last Modified: Tue, 14 May 2024 09:45:34 GMT  
		Size: 80.3 MB (80272075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f234caa51cd40d82f1d9d1f81272bc7f28d5d82209f0382b03a79b5bc4ac7a`  
		Last Modified: Tue, 14 May 2024 09:45:23 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b96b3b3db213c1ce9fc2bb00b87aa64b2bade212daae7a49bae5bb7d4b1f94c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129252405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d95fbabcd324945b08a2c28fe3b7757c66c1d3b1d75682bba947bccb4bc8349`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:36:27 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 07:43:11 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 14 May 2024 07:43:11 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 14 May 2024 07:43:11 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 07:43:11 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 07:43:11 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 07:43:11 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 07:43:11 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 07:43:11 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 07:43:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 07:43:12 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:45:20 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 07:45:22 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:45:22 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 07:45:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:45:22 GMT
USER varnish
# Tue, 14 May 2024 07:45:22 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:45:22 GMT
CMD []
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094ccb1f8045f381a9a13315570ac37fbbb8c79b218068a8477832e6d03edb4`  
		Last Modified: Tue, 14 May 2024 07:50:53 GMT  
		Size: 100.1 MB (100072414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb10fb99095b1789ef09dc72e905666ddaf3c53fc8a78295b017273904531139`  
		Last Modified: Tue, 14 May 2024 07:50:41 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2` - linux; 386

```console
$ docker pull varnish@sha256:cb0cc77367e4829d3affd5551d9080a03c6b0fa078ff9b58e70e8ec5892629ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131914601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48974fd8b3cf8d44aca07431074dc8526bdc2e1fa992b4e9231813c0af64ccc3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:36:55 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 08:46:53 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 14 May 2024 08:46:53 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 14 May 2024 08:46:53 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 08:46:53 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 08:46:53 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 08:46:53 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 08:46:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 08:46:53 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 08:46:54 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 08:46:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:50:17 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 08:50:19 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:50:19 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 08:50:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:50:19 GMT
USER varnish
# Tue, 14 May 2024 08:50:20 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:50:20 GMT
CMD []
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49c5f1ef23ce91521118b6452b07c92b7d034bf779b107962704accbc42e672`  
		Last Modified: Tue, 14 May 2024 08:58:31 GMT  
		Size: 101.8 MB (101751472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394577e08ea5aedcbd0c0dbe3373663d7be20ba2d72d3067bacd60153464dd83`  
		Last Modified: Tue, 14 May 2024 08:58:09 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2` - linux; ppc64le

```console
$ docker pull varnish@sha256:acf5a63864a644f993bdb399f2c3845086bb636d0325e68ee06a97c300e5cac3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137684889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924b039455e93c7721e8b92827fe03de20a43df6ef37c11ed97016a5e211e3cc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:16:10 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:28:45 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 14 May 2024 06:28:45 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 14 May 2024 06:28:45 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 06:28:46 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 06:28:46 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:28:46 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 06:28:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 06:28:47 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 06:28:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:28:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:32:57 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 06:33:01 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:33:01 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:33:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:33:02 GMT
USER varnish
# Tue, 14 May 2024 06:33:02 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:33:03 GMT
CMD []
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0047bd90dbed67820b0837071d98b21fc851869b0e2a7f73c14ffa58ebf5018b`  
		Last Modified: Tue, 14 May 2024 06:42:55 GMT  
		Size: 104.5 MB (104543242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f13f5dbb9191c0810c871f4bc3c9746820d378fd439a5b802c1548fb224c27`  
		Last Modified: Tue, 14 May 2024 06:42:38 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2` - linux; s390x

```console
$ docker pull varnish@sha256:4a62a5a3ede583f0dc63c2f717e9bbca94769b6883891ce48b1a66dcc344e61d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112347776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1af3e20053c4f6ea6a5f28f8e1673404ea4921b4d05dd85d561b45f402353`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:30:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:37:40 GMT
ARG VARNISH_VERSION=7.4.2
# Tue, 14 May 2024 06:37:40 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Tue, 14 May 2024 06:37:41 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 06:37:41 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 06:37:41 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:37:41 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 06:37:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 06:37:41 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Tue, 14 May 2024 06:37:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:37:41 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:39:46 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout cfa8cb3724e4ca6398f60b09157715bcb99d189d;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.4.2.tgz -o $tmpdir/orig.tgz;     echo "acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 14 May 2024 06:39:50 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:39:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:39:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:39:50 GMT
USER varnish
# Tue, 14 May 2024 06:39:50 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:39:50 GMT
CMD []
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f581ab98d8fb29b6c716aa8440f67e67cc978bf9ad9037b21b338460a7c636c9`  
		Last Modified: Tue, 14 May 2024 06:45:31 GMT  
		Size: 84.8 MB (84834886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78a6fcb9cb428fbd0bc5c23b138fc0d42b1d373358deb7ff5cd9aef9e51b6e6`  
		Last Modified: Tue, 14 May 2024 06:45:19 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.4.2-alpine`

```console
$ docker pull varnish@sha256:05b9d1caacca1854f1bde5f2b41bf05e81b46cf9f6f81d3c154ea4c6e440e711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.4.2-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:5fbc1bc3e84cd3ac60979a9481a85f5f52ff1cc67faf8947829a7bd7b9b9754b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73097019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11907c4ede7c51a7cc8003a8ebe7e9a0609cfd2fada1ca510e2874ba75b7e1db`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:58:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 16 Mar 2024 08:58:03 GMT
ARG VARNISH_VERSION=7.4.2
# Sat, 16 Mar 2024 08:58:04 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Sat, 16 Mar 2024 08:58:04 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 08:58:04 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 08:58:04 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 16 Mar 2024 08:58:04 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Sat, 16 Mar 2024 08:58:04 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Sat, 16 Mar 2024 08:58:04 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 08:58:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 08:58:04 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 08:59:25 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 08:59:25 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 08:59:25 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 08:59:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 08:59:26 GMT
USER varnish
# Sat, 16 Mar 2024 08:59:26 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 08:59:26 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae58533547796615774c41bafb56460bad4877888565bfc9a1ec6c16f52f6b4`  
		Last Modified: Sat, 16 Mar 2024 09:01:31 GMT  
		Size: 69.7 MB (69687794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99819e92fc3b92e368ea5ea98755d4e3030786570497598bd4e522ba1ac33a56`  
		Last Modified: Sat, 16 Mar 2024 09:01:22 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:ae15d877b16a9eca5c1c41f757d89ed297cc8f443c69fa711759a93eb37ce6ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57294962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d2c8f3854f037f951775e00013e99cec1267081a8ec3dc3571de8417211882`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:04:36 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 16 Mar 2024 06:04:36 GMT
ARG VARNISH_VERSION=7.4.2
# Sat, 16 Mar 2024 06:04:36 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Sat, 16 Mar 2024 06:04:37 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 06:04:37 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 06:04:37 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 16 Mar 2024 06:04:37 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Sat, 16 Mar 2024 06:04:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Sat, 16 Mar 2024 06:04:37 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 06:04:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 06:04:37 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 06:06:12 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 06:06:12 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 06:06:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:06:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 06:06:13 GMT
USER varnish
# Sat, 16 Mar 2024 06:06:13 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 06:06:13 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ab5ecb2d1ed8f3c2aae1ab9bd751055e5d7650e89828ea44f142bfcac65fb`  
		Last Modified: Sat, 16 Mar 2024 06:08:44 GMT  
		Size: 54.4 MB (54375566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9005365c96e93c96392277b12692c41855b1ee092d79721e614ea7fa36110f`  
		Last Modified: Sat, 16 Mar 2024 06:08:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ced59af939b84abbbe5a45d2d7a5ad49e27421c533be3330b224db0df4bdd0d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69798957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27d5e54efc15e7c1862bfc721b43e2f0bdeac3c0e735b182f7cf9f4c6c0d4ec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:44:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 16 Mar 2024 02:44:35 GMT
ARG VARNISH_VERSION=7.4.2
# Sat, 16 Mar 2024 02:44:35 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Sat, 16 Mar 2024 02:44:35 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 02:44:35 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 02:44:35 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 16 Mar 2024 02:44:35 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Sat, 16 Mar 2024 02:44:35 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Sat, 16 Mar 2024 02:44:35 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 02:44:36 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 02:44:36 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 02:45:51 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 02:45:52 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 02:45:52 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 02:45:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 02:45:52 GMT
USER varnish
# Sat, 16 Mar 2024 02:45:52 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 02:45:52 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc6b87e2fecbc8a9b6a549447b8bef8755d09b37dc73504c7abc051c6c3406c`  
		Last Modified: Sat, 16 Mar 2024 02:47:41 GMT  
		Size: 66.5 MB (66450745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbd4bbee5b2f4c2b9555ad865e5eeb174cdd26745d22c72fe9f9e2a62f66797`  
		Last Modified: Sat, 16 Mar 2024 02:47:35 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2-alpine` - linux; 386

```console
$ docker pull varnish@sha256:3b929f5efbe11594b3643e94b0e246dc698b9af7d8fda80275faf291e499a888
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75119619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc308e5759522d6b64d75e29f341324082d4142e938021f6f3d4d8b77eb25f3f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:10:49 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 16 Mar 2024 05:10:49 GMT
ARG VARNISH_VERSION=7.4.2
# Sat, 16 Mar 2024 05:10:49 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Sat, 16 Mar 2024 05:10:49 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 05:10:50 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 05:10:50 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 16 Mar 2024 05:10:50 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Sat, 16 Mar 2024 05:10:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Sat, 16 Mar 2024 05:10:50 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 05:10:50 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 05:10:50 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 05:13:08 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 05:13:08 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 05:13:08 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:13:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 05:13:09 GMT
USER varnish
# Sat, 16 Mar 2024 05:13:09 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 05:13:09 GMT
CMD []
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e76080aaf74906dfe4b51837edcb9b80241208594c78ba88c76b0a9134944b6`  
		Last Modified: Sat, 16 Mar 2024 05:15:51 GMT  
		Size: 71.9 MB (71875033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dd51dd34630edb1257f7518c446ccb790b322755fd09dd2a1d381a206def97`  
		Last Modified: Sat, 16 Mar 2024 05:15:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:1ca80c297a6636bef9e676941eadbbd2ae4a9883046c66082eb9962960cccd9e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70612414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39f9f04fdcb24570df2135e595128bbf3a7367d913a0f5bb08e313ef5db2cd8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:04:51 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 16 Mar 2024 07:04:51 GMT
ARG VARNISH_VERSION=7.4.2
# Sat, 16 Mar 2024 07:04:51 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Sat, 16 Mar 2024 07:04:52 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 07:04:52 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 07:04:52 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 16 Mar 2024 07:04:53 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Sat, 16 Mar 2024 07:04:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Sat, 16 Mar 2024 07:04:54 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 07:04:54 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 07:04:54 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 07:06:30 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 07:06:32 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 07:06:33 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:06:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 07:06:34 GMT
USER varnish
# Sat, 16 Mar 2024 07:06:34 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 07:06:34 GMT
CMD []
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53da8af833a2063e7469eca5acf43f5089262962457c9e0c3fa2dd70a25e90e5`  
		Last Modified: Sat, 16 Mar 2024 07:08:52 GMT  
		Size: 67.3 MB (67253562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be6baa01e0aa1ca71e452b7d8f4fdb9481e761b24a79f0236c1162c333219c`  
		Last Modified: Sat, 16 Mar 2024 07:08:42 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.2-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:658c619e1c5888e359b4e6993de98b842e60f83a216e0e385524ceec95a8214c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64981125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c25a5086d9e97839e0738a7ab23141fdcc358c417980cbd7036347af18b3c0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 23:02:20 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 16 Mar 2024 23:02:20 GMT
ARG VARNISH_VERSION=7.4.2
# Sat, 16 Mar 2024 23:02:20 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Sat, 16 Mar 2024 23:02:20 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 23:02:20 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 23:02:21 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 16 Mar 2024 23:02:21 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Sat, 16 Mar 2024 23:02:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Sat, 16 Mar 2024 23:02:21 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 23:02:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 23:02:21 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 23:03:57 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 23:03:59 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 23:03:59 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 23:03:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 23:03:59 GMT
USER varnish
# Sat, 16 Mar 2024 23:03:59 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 23:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e0e3c7f56cc2089f64535150ddab85f53e7531b873d39685447626588bb835`  
		Last Modified: Sat, 16 Mar 2024 23:10:56 GMT  
		Size: 61.7 MB (61737992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa1f3451ac4491205f6e354cc93f52b906c40e9f65d8fe5944e999a5ac963`  
		Last Modified: Sat, 16 Mar 2024 23:10:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.4.3`

```console
$ docker pull varnish@sha256:882224e47d7db63a17dce924bf9033b5181a2a3a0fedee09e9aa40c0207f9ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.4.3` - linux; amd64

```console
$ docker pull varnish@sha256:b8370ea0069c03b3b14ae335d01ac6fe9c1a2416cb58a04374c7a05f794f5696
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134784916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a18216991f6a1afd692fb5920e9d02abf542c16b6d2d673ee4dcd3b155a3d5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:17:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 14:20:43 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 14:20:43 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 14:20:43 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 14:20:43 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 14:20:43 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 14:20:43 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 14:20:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 14:20:44 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 14:20:44 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 14:20:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:26:17 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 14:26:18 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:26:18 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 14:26:18 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 14:26:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:26:18 GMT
USER varnish
# Tue, 14 May 2024 14:26:18 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:26:18 GMT
CMD []
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a16974ae153bf113b00ccc0fbf36aac224d2dc680479303298885c6dc18e369`  
		Last Modified: Tue, 14 May 2024 14:36:43 GMT  
		Size: 105.6 MB (105632491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5013aecdda5901d37096b63257c04c84531732b0b32bc00be4f8adb51cbd503`  
		Last Modified: Tue, 14 May 2024 14:36:29 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6d6e7a17e4ee13e1459b04a4a679c4d3ba359f49edf76e98919f4cbbab2b27`  
		Last Modified: Tue, 14 May 2024 14:36:29 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3` - linux; arm variant v7

```console
$ docker pull varnish@sha256:4583809dc8bdcc3a40334d41ed24522463163aaae73022d6f0c53e4f89ea0fc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105004879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68a526a0cb0674dac743036b5c1580beec513788e0155f2ef8a489808be285d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:29:26 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 09:32:20 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 09:32:21 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 09:32:21 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 09:32:21 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 09:32:21 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 09:32:21 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 09:32:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 09:32:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 09:32:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 09:32:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:34:47 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 09:34:48 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:34:48 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 09:34:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 09:34:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:34:49 GMT
USER varnish
# Tue, 14 May 2024 09:34:49 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:34:49 GMT
CMD []
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d2699d7174ee2e3ec604bfeb786dd77e9eedf5d0a48877a3273f650c5077c0`  
		Last Modified: Tue, 14 May 2024 09:44:56 GMT  
		Size: 80.3 MB (80262661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60f9712404c431a4fd8b84805e3a650f223a1422c848b02681e410bb739754`  
		Last Modified: Tue, 14 May 2024 09:44:44 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fa61b2a01fe31985e791b88be9e0288fd610dde76d73b68f1426b2887fecdc`  
		Last Modified: Tue, 14 May 2024 09:44:44 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:2ac2a3ad2e8ef37460b50bf8ae3afefbee38523eb0aaee01f7d6a5e2c3fdb3b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129270960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e44b842694bd08afb5258b5ecd852a0b2b78d9a72bca12ea1cda6a774488be5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:36:27 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 07:39:07 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 07:39:07 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 07:39:07 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 07:39:07 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 07:39:07 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 07:39:07 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 07:39:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 07:39:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 07:39:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 07:39:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:41:14 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 07:41:16 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:41:16 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 07:41:16 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 07:41:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:41:16 GMT
USER varnish
# Tue, 14 May 2024 07:41:16 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:41:16 GMT
CMD []
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048b118ca13512abdb6cfc328a5341657e791ccb3ab8790a8f2b12ac3c31d858`  
		Last Modified: Tue, 14 May 2024 07:50:14 GMT  
		Size: 100.1 MB (100089445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eebca74f010bc1af9b8dda398fbc899b6407212646e1cf52d00a5b8b55b03ab`  
		Last Modified: Tue, 14 May 2024 07:50:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0ff9860e00c9b930e05109dc282db9d300a0457af0d0c59351d49ec164ba61`  
		Last Modified: Tue, 14 May 2024 07:50:02 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3` - linux; 386

```console
$ docker pull varnish@sha256:1a9742bfb4ce30721c6ca2fb5520c15305d749e160ec5611cd50e8790eebc63e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131930287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bc76427f2017543e41070e746fc91d73dfb0c21a092175637a91b6bc9d2874`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:36:55 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 08:40:50 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 08:40:50 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 08:40:50 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 08:40:50 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 08:40:50 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 08:40:50 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 08:40:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 08:40:51 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 08:40:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 08:40:51 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:44:17 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 08:44:18 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:44:18 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 08:44:18 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 08:44:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:44:19 GMT
USER varnish
# Tue, 14 May 2024 08:44:19 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:44:19 GMT
CMD []
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc2369f33a43201c69e5e6ad92aeac3ded2c005a5c3706aeb78ba01830e5a63`  
		Last Modified: Tue, 14 May 2024 08:57:36 GMT  
		Size: 101.8 MB (101765638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bd0d0328766529f5a2016fa7b7ec510ffecc1ba0cab060ed4fef646c928e15`  
		Last Modified: Tue, 14 May 2024 08:57:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2f2768da2b8d37692d1c75568c404df85dc71979e9d7d8853eb282addf1d86`  
		Last Modified: Tue, 14 May 2024 08:57:14 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3` - linux; ppc64le

```console
$ docker pull varnish@sha256:3ab6c8b9e140978901343919b2cace41958092e19e671810122ebce933b12a76
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137714757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972cca6f54c3a511281a9ebc05c802367bd39316298842c4b6183435f736ff97`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:16:10 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:20:38 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 06:20:38 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 06:20:38 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 06:20:38 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 06:20:39 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:20:39 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 06:20:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 06:20:39 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:20:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:20:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:24:45 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:24:50 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:24:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:24:50 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:24:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:24:51 GMT
USER varnish
# Tue, 14 May 2024 06:24:51 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:24:51 GMT
CMD []
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426fac7e303070a52e77a623a26e18a04b9bc1ed6c91073683d85327b983ef85`  
		Last Modified: Tue, 14 May 2024 06:42:06 GMT  
		Size: 104.6 MB (104571587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320391667901aac1e14c6f05c8a445467f80196650c05b69b226e68c2c048887`  
		Last Modified: Tue, 14 May 2024 06:41:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b06fc6a3aab74a784600134ec69349d5cd9892a1c4fb30280e0e7c4f049882`  
		Last Modified: Tue, 14 May 2024 06:41:49 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3` - linux; s390x

```console
$ docker pull varnish@sha256:db3133a8388660ac154a58e136a49b0065223533421dd29486e98dc39ca9df22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112365129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7434c2abce66b312ebf0f4009a2e2d2111a9257362cefabd0f244b26fc9ab3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:30:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:33:31 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 06:33:31 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 06:33:31 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 06:33:31 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 06:33:31 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:33:32 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 06:33:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 06:33:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:33:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:33:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:35:41 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:35:44 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:35:44 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:35:45 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:35:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:35:45 GMT
USER varnish
# Tue, 14 May 2024 06:35:45 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:35:45 GMT
CMD []
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df8730d37f1330b10295cfd34b8376a58bc64bf2d8198e0b45334700003fbd6`  
		Last Modified: Tue, 14 May 2024 06:44:59 GMT  
		Size: 84.9 MB (84850723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f69700bb9b4d260724360cb436e12ef933d83342415b05dab002efb950930f`  
		Last Modified: Tue, 14 May 2024 06:44:47 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffb8a880c88bb62724629c502991052f5d79ccd0f05d405bc80a52b9c53e738`  
		Last Modified: Tue, 14 May 2024 06:44:47 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.4.3-alpine`

```console
$ docker pull varnish@sha256:2c6ab5471f574fd6cdb1b89da00b72ba870512959529d43c648fec5ff81a2322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.4.3-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:bad41538a520c7324ae66672afcd1843244ff3fd6a69dc186fffabb26e5e5b3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73111717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fcd1daa5a1fd515be57af3744ca44fd77a3aff504e0813f18881ba362df461`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:58:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 20:06:43 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 20:06:43 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 20:06:44 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 20:06:44 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 20:06:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 20:08:04 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 20:08:04 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 20:08:04 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 20:08:05 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 20:08:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 20:08:05 GMT
USER varnish
# Tue, 19 Mar 2024 20:08:05 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 20:08:05 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e88fbcf523fb9f70c926ce56e3d01391ed2c58556c7fed0504edee8f38f1599`  
		Last Modified: Tue, 19 Mar 2024 20:12:02 GMT  
		Size: 69.7 MB (69700966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73d56dea7353d1ce78b162cf126e47cb61ed2436148992e6973adba9df7a26f`  
		Last Modified: Tue, 19 Mar 2024 20:11:53 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d86a9601c89cd35fb0e08c0495b786d5c0fd08804adbc6cf16ceabede21ed6`  
		Last Modified: Tue, 19 Mar 2024 20:11:53 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d8d8d456b3b22b0a1717e09faa1a04161ca2b812536f9fcc981531f8ada51710
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57316383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31c572f46d3e2f829a48ec29edf234b8908aff261f843e8008c27792c881c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:04:36 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:25:16 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 19:25:16 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 19:25:17 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 19:25:17 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 19:25:18 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:25:18 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 19:25:18 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 19:25:19 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:25:19 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:25:19 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:27:54 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 19:27:55 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:27:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:27:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:27:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:27:57 GMT
USER varnish
# Tue, 19 Mar 2024 19:27:57 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:27:58 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb32a9d2bc9510faba817c92bfe1cf189ad3cfd884457c74f7933aed86df6eb`  
		Last Modified: Tue, 19 Mar 2024 19:33:10 GMT  
		Size: 54.4 MB (54395458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001be72dd77327edce535297b918c11d2092b608be216951ffe22e818dd361d1`  
		Last Modified: Tue, 19 Mar 2024 19:33:02 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02b8aa68970246d2ae92e63dd681f9788e02bb390ef1e86b69bd42087bca281`  
		Last Modified: Tue, 19 Mar 2024 19:33:02 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:479ea6daf1d1ddb36de834aa28c5e64c8a4883f743eed493192255ce9f795df1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69813716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be2438e6775bff4a85bde81ac5d9c06ac7d183b8d6ce2edea5db9b89655cc4c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:44:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 18:57:04 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 18:57:04 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:57:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 18:57:04 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 18:58:12 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 18:58:12 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 18:58:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 18:58:13 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 18:58:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 18:58:13 GMT
USER varnish
# Tue, 19 Mar 2024 18:58:13 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 18:58:13 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894a7285b926312b215684e50114187e34f58603947ba360a068c707e8c90cfd`  
		Last Modified: Tue, 19 Mar 2024 19:01:30 GMT  
		Size: 66.5 MB (66463974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf21108d62a7fd3c9304838a0e7d38d87a8b2aaea9be4002b48b0debcfb122a`  
		Last Modified: Tue, 19 Mar 2024 19:01:24 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b1b0f8e8b6fe88f280d6f8a38df3be1e85d89988fb2386fb5a8b6b171772d3`  
		Last Modified: Tue, 19 Mar 2024 19:01:24 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3-alpine` - linux; 386

```console
$ docker pull varnish@sha256:1fdf700b9bf5114292511d5f9b8410f030a420195edc7822ff168350517f134e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75135148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f375513ff93e5dcf88d1563c073de2cbed2e3d5b7d77236f1550cd1af8c6a4be`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:10:49 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:04:13 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 19:04:13 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 19:04:13 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 19:04:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 19:04:14 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:04:14 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 19:04:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 19:04:14 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:04:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:04:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:06:19 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 19:06:19 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:06:19 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:06:19 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:06:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:06:20 GMT
USER varnish
# Tue, 19 Mar 2024 19:06:20 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:06:20 GMT
CMD []
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a30e445c3604537fdf8df8c22a060202d20489b8eddfa77f4550fe4f911650`  
		Last Modified: Tue, 19 Mar 2024 19:11:11 GMT  
		Size: 71.9 MB (71889037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4152d250362e0e5bf5357d66457786d213f1d15255388a3bb7c01c3f2052d5`  
		Last Modified: Tue, 19 Mar 2024 19:10:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2737032c6f8bcdf0a71d104e82734a6b69555856e39ecff4ef201d8b391fd949`  
		Last Modified: Tue, 19 Mar 2024 19:10:57 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:cbcdf4a72047647d6e472f95a475d99778629b31fa07a868c0e8f6ee6c329013
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70642273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817de67047306f66d083abae50517fcfa5851ece50b2da689d6cbb59802870bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:04:51 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:44:28 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 19:44:29 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 19:44:29 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 19:44:29 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 19:44:30 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:44:30 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 19:44:30 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 19:44:30 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:44:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:44:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:45:51 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 19:45:54 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:45:54 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:45:54 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:45:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:45:55 GMT
USER varnish
# Tue, 19 Mar 2024 19:45:55 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743250632b3e83457d746dd80c83c1792da89dcac7861cfbe4e0ced8ff47f129`  
		Last Modified: Tue, 19 Mar 2024 19:51:43 GMT  
		Size: 67.3 MB (67281893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9d99e7af2f3afb5934553c41f70a80f5fa99509365d3f33bebb6089dcd9461`  
		Last Modified: Tue, 19 Mar 2024 19:51:33 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f77c02b1d17e9e7dcf8169ca83ef8b3325640b7d59994287907bad7312790`  
		Last Modified: Tue, 19 Mar 2024 19:51:33 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.4.3-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:1b30229155355ad2c6b66e8e72eddc263f19d9cd02ea6017fa667301d5a27b85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65011686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697ae126a2c8542caeb132c89923bbb9ac0034c03f83099f8fd649c1782a34a3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 23:02:20 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:29:26 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 19:29:27 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 19:29:27 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:29:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:29:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:30:52 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 19:30:54 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:30:54 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:30:55 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:30:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:30:55 GMT
USER varnish
# Tue, 19 Mar 2024 19:30:55 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:30:55 GMT
CMD []
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe38f977ea67683ee4420495875859583d5281a008b4d6aed6e1d588f2f0806`  
		Last Modified: Tue, 19 Mar 2024 19:35:51 GMT  
		Size: 61.8 MB (61767029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c60b2806d71370deb7439b9951f3eb3c198692c33e1f8286d755dc93bdbee9`  
		Last Modified: Tue, 19 Mar 2024 19:35:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d1a215e014825ed08ff1940cdbfc607d4163f6608a016f2cca535243352213`  
		Last Modified: Tue, 19 Mar 2024 19:35:44 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5`

```console
$ docker pull varnish@sha256:b872f952fa3532d91627b46c9d7bd61ace423c916cd96e94b8d97530aeae1c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.5` - linux; amd64

```console
$ docker pull varnish@sha256:f72ebe3b392a696053248d7b8e7dfdabfa33791bd141ff47d852e48e18c93007
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134870706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cbd7438657ddb8bdb5f6b5f47755c40a03c0b3e348f6e8dd6d842d9c24076c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:17:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 14:17:47 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 14:17:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 14:17:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 14:17:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 14:17:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 14:17:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 14:17:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 14:17:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 14:17:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 14:17:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:20:30 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 14:20:31 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:20:31 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 14:20:31 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 14:20:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:20:31 GMT
USER varnish
# Tue, 14 May 2024 14:20:32 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:20:32 GMT
CMD []
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413e6b36d364286798878657af0dcccb36d94782a6d2419229eae08912d17455`  
		Last Modified: Tue, 14 May 2024 14:36:14 GMT  
		Size: 105.7 MB (105718284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e66dffca66663ec433a001fc5f077272a46180f57573f9b5ce1452a7a83f55`  
		Last Modified: Tue, 14 May 2024 14:36:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb59e22e9737d1d5781e464a404ade546d918bfa502cbbcc4517d65a7f680b`  
		Last Modified: Tue, 14 May 2024 14:36:00 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; arm variant v7

```console
$ docker pull varnish@sha256:085ff1723c4b074e79adbe248872143338473b731cd7490afef28adb3c4130b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105119153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db54e2c465642301fdacd6668d3395df8e3512f1e531fb8de36272cb117cb0fc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:29:26 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 09:29:26 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 09:29:26 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 09:29:26 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 09:29:26 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 09:29:26 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 09:29:26 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 09:29:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 09:29:27 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 09:29:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 09:29:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:32:07 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 09:32:08 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:32:08 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 09:32:08 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 09:32:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:32:08 GMT
USER varnish
# Tue, 14 May 2024 09:32:08 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:32:08 GMT
CMD []
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c650ad817ba02c0d4e4727081a89c1db1a6286d775da0f2f8fab196660899a55`  
		Last Modified: Tue, 14 May 2024 09:44:31 GMT  
		Size: 80.4 MB (80376936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c68ca8861c02f74b24369f7760ab0139906755818dd0a15e4418d2ada7ffa34`  
		Last Modified: Tue, 14 May 2024 09:44:19 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8f0aa28587e85f7e413f79324a49f39f5de701c02a9870d12d3f7d15703009`  
		Last Modified: Tue, 14 May 2024 09:44:19 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:29c577bfa369c579fcbee8cff6e41fe72263689f245b8f1671d27d6202599a8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129357190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50701c82e1132191d5f63d75d248438bbb5f29014b25fc5bec3f3e4c8c3e5eb4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:36:27 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 07:36:27 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 07:36:27 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 07:36:27 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 07:36:27 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 07:36:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 07:36:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 07:36:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 07:36:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 07:36:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 07:36:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:38:48 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 07:38:50 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:38:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 07:38:50 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 07:38:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:38:50 GMT
USER varnish
# Tue, 14 May 2024 07:38:50 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:38:50 GMT
CMD []
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb62cc8d96dea21946b78774c842df0094506ef45e41526b277f284fb97bb47c`  
		Last Modified: Tue, 14 May 2024 07:49:49 GMT  
		Size: 100.2 MB (100175675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3966f347840524811178eaad61a7e5340413786a2688888f743afe86e1a0a9b`  
		Last Modified: Tue, 14 May 2024 07:49:38 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cf5e226a79576e4a1dc03254d42b5b40fe89c8325674f07dd035f0714efbe7`  
		Last Modified: Tue, 14 May 2024 07:49:38 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; 386

```console
$ docker pull varnish@sha256:5c0f224d3030b7f84f4bfa6b54269d447cd15eee73980e887dc39a1d05fd1f8d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132039089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e293efa3f248ab5f50cc1921acfc2e8e469a0f81e12431f9cfcd98e08a3df6be`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:36:55 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 08:36:55 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 08:36:55 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 08:36:55 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 08:36:55 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 08:36:56 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 08:36:56 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 08:36:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 08:36:56 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 08:36:56 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 08:36:56 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:40:38 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 08:40:40 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:40:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 08:40:40 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 08:40:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:40:40 GMT
USER varnish
# Tue, 14 May 2024 08:40:40 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:40:40 GMT
CMD []
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b2a8d398f06f001e325035fa52a9e1f2559a0317771d7eed0dfc4f3ec041ca`  
		Last Modified: Tue, 14 May 2024 08:57:00 GMT  
		Size: 101.9 MB (101874440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbd51cfeb5a6e23f7f127eb571ff7791f604966eed44cb694c6a2dd97b4089e`  
		Last Modified: Tue, 14 May 2024 08:56:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699e57a7a26c2cdc5a62b03fb1ae3fdd471c1b324602902354dff65d33a8ea5e`  
		Last Modified: Tue, 14 May 2024 08:56:37 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; ppc64le

```console
$ docker pull varnish@sha256:0ae43991e3759b15eb00d277fc9dc7c4eb4ae56a6fa79dff7f719c508beb8484
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137799705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c772594d8919b834a3d73ad7fe9e9fffe8dc4ca2777cddef9f57a4dad00f9749`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:16:10 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:16:11 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 06:16:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 06:16:11 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 06:16:11 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 06:16:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:16:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 06:16:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 06:16:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:16:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:16:13 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:20:16 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:20:20 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:20:20 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:20:20 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:20:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:20:21 GMT
USER varnish
# Tue, 14 May 2024 06:20:21 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:20:21 GMT
CMD []
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403b56cebcc3656269beca052096c5e1c11f1672a301a9ee52ae464c2564a49c`  
		Last Modified: Tue, 14 May 2024 06:41:36 GMT  
		Size: 104.7 MB (104656534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada4372d38a4d23cb9c481bc8876c79897d109fb449f4136514ae7c48feb8251`  
		Last Modified: Tue, 14 May 2024 06:41:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18266cc4a11d4c00d9eaed8537bec3c1501f89485f7ff559aa1d02143fb05c5`  
		Last Modified: Tue, 14 May 2024 06:41:19 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; s390x

```console
$ docker pull varnish@sha256:742a183e8ee36555aed72fe43318eb161ed5f5d00fd37dd750de3469bca50c51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112463112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85bd636b03f65a70e70ca62abf48eebae6762e8efee6a75959c259861912f10`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:30:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:30:46 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 06:30:46 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 06:30:46 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 06:30:46 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 06:30:46 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:30:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 06:30:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 06:30:46 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:30:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:30:46 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:33:11 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:33:15 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:33:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:33:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:33:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:33:15 GMT
USER varnish
# Tue, 14 May 2024 06:33:15 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:33:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea2a5e5bd549feabbf3edf8165c5877667fd57501953641b82bb4cc396c4b56`  
		Last Modified: Tue, 14 May 2024 06:44:38 GMT  
		Size: 84.9 MB (84948702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f71635c9c126f4f48e53db27bdd0c2e05b81e3a215b4034716600191d01407a`  
		Last Modified: Tue, 14 May 2024 06:44:27 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0407e5e9f9bdb646351b73c58d732fb18751572de2233d8340f97c944573e2`  
		Last Modified: Tue, 14 May 2024 06:44:27 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5-alpine`

```console
$ docker pull varnish@sha256:3a4011e1cb36e5b070f6d134202e980d0f4878f0d03f26682c72a8c1508851e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.5-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:3faeff6620b5f7240ed712831ed6e7d2e1db892ea9b296b82de23d89fd591a99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73202083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd13adbcd80e61e6f3c26bda7e058d15009f0a20ae20131472a565226e574f7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:58:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 20:02:40 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 20:02:40 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 20:02:41 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 20:02:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 20:02:41 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 20:03:52 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 20:03:52 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 20:03:52 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 20:03:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 20:03:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 20:03:52 GMT
USER varnish
# Tue, 19 Mar 2024 20:03:53 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 20:03:53 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c176d45bcb975cba1b43c0c9e49ce65128387efdfdc17217145873f04a11e1`  
		Last Modified: Tue, 19 Mar 2024 20:11:16 GMT  
		Size: 69.8 MB (69791333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d913ae7181c4f5f8a43290c04e24020c8eb9184528c77eaf8703c38014f77`  
		Last Modified: Tue, 19 Mar 2024 20:11:08 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d41aa7153952f065906cfaf9d8f0422d186bce263716a52a9d7d934daed6a0b`  
		Last Modified: Tue, 19 Mar 2024 20:11:08 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:1c82d437e3fc46d648e4225b36a91481bd5f868c35e1702d7bcc1d9c20d18640
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57409560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266b9b4a0d680e0cd2ff6dced155f16bd284ee39b69e0483ec6103699359a002`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:04:36 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:18:13 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 19:18:14 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 19:18:14 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 19:18:14 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 19:18:15 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:18:15 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 19:18:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 19:18:16 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:18:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:18:17 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:20:43 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:20:43 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:20:44 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:20:45 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:20:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:20:46 GMT
USER varnish
# Tue, 19 Mar 2024 19:20:46 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:20:47 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f8adbcbac98e64fc449be303f6272d2738adb8525204c6901dff554f86fa66`  
		Last Modified: Tue, 19 Mar 2024 19:32:25 GMT  
		Size: 54.5 MB (54488635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3941fb8199245e2961065a39b72e24f8de8af71856809785011bf58a8387a3`  
		Last Modified: Tue, 19 Mar 2024 19:32:17 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79682f92088dfb803f52e91606c36c4f38d6cd5ddce57f483a9e2ef62920304`  
		Last Modified: Tue, 19 Mar 2024 19:32:23 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ec98b2eb6b8667b460891865e7efac5ff91a27f865fc4c36b6b1fd734bbc8cd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69908650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c1d1ec26a3258c847ab32434c2b7bde64ac4beeabc8748d1801080c01ab7dc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:44:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:53:31 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 18:53:31 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 18:53:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:53:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 18:53:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 18:54:32 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 18:54:33 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 18:54:33 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 18:54:33 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 18:54:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 18:54:33 GMT
USER varnish
# Tue, 19 Mar 2024 18:54:33 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 18:54:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d0b6d2fd6cff808b366da93f873d055ce0419948d3444a1bb58808ea47fb3f`  
		Last Modified: Tue, 19 Mar 2024 19:00:52 GMT  
		Size: 66.6 MB (66558909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44994d724b8545ce35ad86ea63237c741cdc823b438f0d6bd598c894642c8179`  
		Last Modified: Tue, 19 Mar 2024 19:00:45 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e930cce73c948215a5db7660fc238edfe4246ba4765a2962c4719e153abc60d`  
		Last Modified: Tue, 19 Mar 2024 19:00:46 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; 386

```console
$ docker pull varnish@sha256:271cfe5af6514984ccd097b3cce731d5a9c032bc99b52cc47110dbc556768d57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75228860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb431a34bb6cdb93a0f5f2e356b8c965ce3a1fc82f8161532b21fa9bd1145809`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:10:49 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 18:58:27 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:58:28 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 18:58:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 18:58:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:58:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 18:58:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:00:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:00:28 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:00:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:00:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:00:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:00:29 GMT
USER varnish
# Tue, 19 Mar 2024 19:00:29 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:00:29 GMT
CMD []
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113db18c4e7963ab8ca76533a0c77b2c708d3810e54641faa7945eca0c252dcf`  
		Last Modified: Tue, 19 Mar 2024 19:10:14 GMT  
		Size: 72.0 MB (71982747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e877b2d115d0c129cc6f97774e825110e4e6bd3931b8c5f04ce7182ffcba6`  
		Last Modified: Tue, 19 Mar 2024 19:10:00 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25f3f77beb119cded24ad4aab6c67e0513920007e46e9354bc1d57d452efdfb`  
		Last Modified: Tue, 19 Mar 2024 19:10:00 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:dd4d79b176782a5f57f40678bc6650e84e8c9a86073f29466b31fc0c51703082
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70737370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ea74155a1db4e763d97a0f632041aaed697fbd9ffd1648642f8e415d23690c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:04:51 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:38:24 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 19:38:24 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 19:38:24 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 19:38:25 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 19:38:25 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:38:25 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 19:38:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 19:38:26 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:38:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:38:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:39:41 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:39:43 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:39:43 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:39:44 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:39:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:39:44 GMT
USER varnish
# Tue, 19 Mar 2024 19:39:45 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:39:45 GMT
CMD []
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428f744b49685e322e0a893302c92068a1ede30c15fb29519256fe37a6aad148`  
		Last Modified: Tue, 19 Mar 2024 19:50:52 GMT  
		Size: 67.4 MB (67376994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb191424e69a8bb8a6be9f12d7e46c4b1369b37491fff6bd81eeccb9a712cc6`  
		Last Modified: Tue, 19 Mar 2024 19:50:41 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b37f7f2ebd35872c656f0820fc315ddc1c3d695c666ef09402005c4cc1852d`  
		Last Modified: Tue, 19 Mar 2024 19:50:41 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:a47e0d4cd725605df06b5bc1fcc8eb693a849c5ddd6337d65815300b329b22f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65112686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0da4d7f455db127e85ce04ed01f5c3e28cb4e1f11d7d716f95da5128336356a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 23:02:20 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 19:23:42 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 19:23:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 19:23:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:23:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:23:43 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:25:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:25:02 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:25:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:25:02 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:25:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:25:02 GMT
USER varnish
# Tue, 19 Mar 2024 19:25:03 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:25:03 GMT
CMD []
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef4ed0e0ad7feb66dd97a52a239ef0ef58422dcd40a031c39b4461500d8784`  
		Last Modified: Tue, 19 Mar 2024 19:35:15 GMT  
		Size: 61.9 MB (61868027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2140d3395b6c8cba74c81342c72ca2c18dc574495773600dcbb7d1704c51ba2`  
		Last Modified: Tue, 19 Mar 2024 19:35:08 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89279a57010ad629819355bee1cf98630a8c3743a4d658fe28695d5e586bc113`  
		Last Modified: Tue, 19 Mar 2024 19:35:08 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5.0`

```console
$ docker pull varnish@sha256:b872f952fa3532d91627b46c9d7bd61ace423c916cd96e94b8d97530aeae1c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.5.0` - linux; amd64

```console
$ docker pull varnish@sha256:f72ebe3b392a696053248d7b8e7dfdabfa33791bd141ff47d852e48e18c93007
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134870706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cbd7438657ddb8bdb5f6b5f47755c40a03c0b3e348f6e8dd6d842d9c24076c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:17:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 14:17:47 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 14:17:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 14:17:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 14:17:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 14:17:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 14:17:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 14:17:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 14:17:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 14:17:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 14:17:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:20:30 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 14:20:31 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:20:31 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 14:20:31 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 14:20:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:20:31 GMT
USER varnish
# Tue, 14 May 2024 14:20:32 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:20:32 GMT
CMD []
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413e6b36d364286798878657af0dcccb36d94782a6d2419229eae08912d17455`  
		Last Modified: Tue, 14 May 2024 14:36:14 GMT  
		Size: 105.7 MB (105718284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e66dffca66663ec433a001fc5f077272a46180f57573f9b5ce1452a7a83f55`  
		Last Modified: Tue, 14 May 2024 14:36:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb59e22e9737d1d5781e464a404ade546d918bfa502cbbcc4517d65a7f680b`  
		Last Modified: Tue, 14 May 2024 14:36:00 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:085ff1723c4b074e79adbe248872143338473b731cd7490afef28adb3c4130b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105119153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db54e2c465642301fdacd6668d3395df8e3512f1e531fb8de36272cb117cb0fc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:29:26 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 09:29:26 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 09:29:26 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 09:29:26 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 09:29:26 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 09:29:26 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 09:29:26 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 09:29:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 09:29:27 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 09:29:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 09:29:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:32:07 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 09:32:08 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:32:08 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 09:32:08 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 09:32:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:32:08 GMT
USER varnish
# Tue, 14 May 2024 09:32:08 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:32:08 GMT
CMD []
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c650ad817ba02c0d4e4727081a89c1db1a6286d775da0f2f8fab196660899a55`  
		Last Modified: Tue, 14 May 2024 09:44:31 GMT  
		Size: 80.4 MB (80376936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c68ca8861c02f74b24369f7760ab0139906755818dd0a15e4418d2ada7ffa34`  
		Last Modified: Tue, 14 May 2024 09:44:19 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8f0aa28587e85f7e413f79324a49f39f5de701c02a9870d12d3f7d15703009`  
		Last Modified: Tue, 14 May 2024 09:44:19 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:29c577bfa369c579fcbee8cff6e41fe72263689f245b8f1671d27d6202599a8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129357190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50701c82e1132191d5f63d75d248438bbb5f29014b25fc5bec3f3e4c8c3e5eb4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:36:27 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 07:36:27 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 07:36:27 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 07:36:27 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 07:36:27 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 07:36:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 07:36:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 07:36:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 07:36:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 07:36:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 07:36:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:38:48 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 07:38:50 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:38:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 07:38:50 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 07:38:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:38:50 GMT
USER varnish
# Tue, 14 May 2024 07:38:50 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:38:50 GMT
CMD []
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb62cc8d96dea21946b78774c842df0094506ef45e41526b277f284fb97bb47c`  
		Last Modified: Tue, 14 May 2024 07:49:49 GMT  
		Size: 100.2 MB (100175675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3966f347840524811178eaad61a7e5340413786a2688888f743afe86e1a0a9b`  
		Last Modified: Tue, 14 May 2024 07:49:38 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cf5e226a79576e4a1dc03254d42b5b40fe89c8325674f07dd035f0714efbe7`  
		Last Modified: Tue, 14 May 2024 07:49:38 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; 386

```console
$ docker pull varnish@sha256:5c0f224d3030b7f84f4bfa6b54269d447cd15eee73980e887dc39a1d05fd1f8d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132039089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e293efa3f248ab5f50cc1921acfc2e8e469a0f81e12431f9cfcd98e08a3df6be`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:36:55 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 08:36:55 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 08:36:55 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 08:36:55 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 08:36:55 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 08:36:56 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 08:36:56 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 08:36:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 08:36:56 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 08:36:56 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 08:36:56 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:40:38 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 08:40:40 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:40:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 08:40:40 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 08:40:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:40:40 GMT
USER varnish
# Tue, 14 May 2024 08:40:40 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:40:40 GMT
CMD []
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b2a8d398f06f001e325035fa52a9e1f2559a0317771d7eed0dfc4f3ec041ca`  
		Last Modified: Tue, 14 May 2024 08:57:00 GMT  
		Size: 101.9 MB (101874440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbd51cfeb5a6e23f7f127eb571ff7791f604966eed44cb694c6a2dd97b4089e`  
		Last Modified: Tue, 14 May 2024 08:56:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699e57a7a26c2cdc5a62b03fb1ae3fdd471c1b324602902354dff65d33a8ea5e`  
		Last Modified: Tue, 14 May 2024 08:56:37 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:0ae43991e3759b15eb00d277fc9dc7c4eb4ae56a6fa79dff7f719c508beb8484
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137799705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c772594d8919b834a3d73ad7fe9e9fffe8dc4ca2777cddef9f57a4dad00f9749`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:16:10 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:16:11 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 06:16:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 06:16:11 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 06:16:11 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 06:16:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:16:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 06:16:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 06:16:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:16:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:16:13 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:20:16 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:20:20 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:20:20 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:20:20 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:20:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:20:21 GMT
USER varnish
# Tue, 14 May 2024 06:20:21 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:20:21 GMT
CMD []
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403b56cebcc3656269beca052096c5e1c11f1672a301a9ee52ae464c2564a49c`  
		Last Modified: Tue, 14 May 2024 06:41:36 GMT  
		Size: 104.7 MB (104656534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada4372d38a4d23cb9c481bc8876c79897d109fb449f4136514ae7c48feb8251`  
		Last Modified: Tue, 14 May 2024 06:41:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18266cc4a11d4c00d9eaed8537bec3c1501f89485f7ff559aa1d02143fb05c5`  
		Last Modified: Tue, 14 May 2024 06:41:19 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; s390x

```console
$ docker pull varnish@sha256:742a183e8ee36555aed72fe43318eb161ed5f5d00fd37dd750de3469bca50c51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112463112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85bd636b03f65a70e70ca62abf48eebae6762e8efee6a75959c259861912f10`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:30:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:30:46 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 06:30:46 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 06:30:46 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 06:30:46 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 06:30:46 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:30:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 06:30:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 06:30:46 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:30:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:30:46 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:33:11 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:33:15 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:33:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:33:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:33:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:33:15 GMT
USER varnish
# Tue, 14 May 2024 06:33:15 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:33:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea2a5e5bd549feabbf3edf8165c5877667fd57501953641b82bb4cc396c4b56`  
		Last Modified: Tue, 14 May 2024 06:44:38 GMT  
		Size: 84.9 MB (84948702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f71635c9c126f4f48e53db27bdd0c2e05b81e3a215b4034716600191d01407a`  
		Last Modified: Tue, 14 May 2024 06:44:27 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0407e5e9f9bdb646351b73c58d732fb18751572de2233d8340f97c944573e2`  
		Last Modified: Tue, 14 May 2024 06:44:27 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5.0-alpine`

```console
$ docker pull varnish@sha256:3a4011e1cb36e5b070f6d134202e980d0f4878f0d03f26682c72a8c1508851e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.5.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:3faeff6620b5f7240ed712831ed6e7d2e1db892ea9b296b82de23d89fd591a99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73202083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd13adbcd80e61e6f3c26bda7e058d15009f0a20ae20131472a565226e574f7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:58:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 20:02:40 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 20:02:40 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 20:02:41 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 20:02:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 20:02:41 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 20:03:52 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 20:03:52 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 20:03:52 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 20:03:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 20:03:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 20:03:52 GMT
USER varnish
# Tue, 19 Mar 2024 20:03:53 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 20:03:53 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c176d45bcb975cba1b43c0c9e49ce65128387efdfdc17217145873f04a11e1`  
		Last Modified: Tue, 19 Mar 2024 20:11:16 GMT  
		Size: 69.8 MB (69791333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d913ae7181c4f5f8a43290c04e24020c8eb9184528c77eaf8703c38014f77`  
		Last Modified: Tue, 19 Mar 2024 20:11:08 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d41aa7153952f065906cfaf9d8f0422d186bce263716a52a9d7d934daed6a0b`  
		Last Modified: Tue, 19 Mar 2024 20:11:08 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:1c82d437e3fc46d648e4225b36a91481bd5f868c35e1702d7bcc1d9c20d18640
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57409560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266b9b4a0d680e0cd2ff6dced155f16bd284ee39b69e0483ec6103699359a002`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:04:36 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:18:13 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 19:18:14 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 19:18:14 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 19:18:14 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 19:18:15 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:18:15 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 19:18:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 19:18:16 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:18:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:18:17 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:20:43 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:20:43 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:20:44 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:20:45 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:20:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:20:46 GMT
USER varnish
# Tue, 19 Mar 2024 19:20:46 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:20:47 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f8adbcbac98e64fc449be303f6272d2738adb8525204c6901dff554f86fa66`  
		Last Modified: Tue, 19 Mar 2024 19:32:25 GMT  
		Size: 54.5 MB (54488635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3941fb8199245e2961065a39b72e24f8de8af71856809785011bf58a8387a3`  
		Last Modified: Tue, 19 Mar 2024 19:32:17 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79682f92088dfb803f52e91606c36c4f38d6cd5ddce57f483a9e2ef62920304`  
		Last Modified: Tue, 19 Mar 2024 19:32:23 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ec98b2eb6b8667b460891865e7efac5ff91a27f865fc4c36b6b1fd734bbc8cd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69908650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c1d1ec26a3258c847ab32434c2b7bde64ac4beeabc8748d1801080c01ab7dc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:44:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:53:31 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 18:53:31 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 18:53:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:53:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 18:53:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 18:54:32 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 18:54:33 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 18:54:33 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 18:54:33 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 18:54:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 18:54:33 GMT
USER varnish
# Tue, 19 Mar 2024 18:54:33 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 18:54:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d0b6d2fd6cff808b366da93f873d055ce0419948d3444a1bb58808ea47fb3f`  
		Last Modified: Tue, 19 Mar 2024 19:00:52 GMT  
		Size: 66.6 MB (66558909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44994d724b8545ce35ad86ea63237c741cdc823b438f0d6bd598c894642c8179`  
		Last Modified: Tue, 19 Mar 2024 19:00:45 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e930cce73c948215a5db7660fc238edfe4246ba4765a2962c4719e153abc60d`  
		Last Modified: Tue, 19 Mar 2024 19:00:46 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:271cfe5af6514984ccd097b3cce731d5a9c032bc99b52cc47110dbc556768d57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75228860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb431a34bb6cdb93a0f5f2e356b8c965ce3a1fc82f8161532b21fa9bd1145809`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:10:49 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 18:58:27 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:58:28 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 18:58:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 18:58:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:58:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 18:58:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:00:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:00:28 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:00:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:00:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:00:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:00:29 GMT
USER varnish
# Tue, 19 Mar 2024 19:00:29 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:00:29 GMT
CMD []
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113db18c4e7963ab8ca76533a0c77b2c708d3810e54641faa7945eca0c252dcf`  
		Last Modified: Tue, 19 Mar 2024 19:10:14 GMT  
		Size: 72.0 MB (71982747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e877b2d115d0c129cc6f97774e825110e4e6bd3931b8c5f04ce7182ffcba6`  
		Last Modified: Tue, 19 Mar 2024 19:10:00 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25f3f77beb119cded24ad4aab6c67e0513920007e46e9354bc1d57d452efdfb`  
		Last Modified: Tue, 19 Mar 2024 19:10:00 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:dd4d79b176782a5f57f40678bc6650e84e8c9a86073f29466b31fc0c51703082
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70737370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ea74155a1db4e763d97a0f632041aaed697fbd9ffd1648642f8e415d23690c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:04:51 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:38:24 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 19:38:24 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 19:38:24 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 19:38:25 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 19:38:25 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:38:25 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 19:38:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 19:38:26 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:38:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:38:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:39:41 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:39:43 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:39:43 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:39:44 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:39:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:39:44 GMT
USER varnish
# Tue, 19 Mar 2024 19:39:45 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:39:45 GMT
CMD []
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428f744b49685e322e0a893302c92068a1ede30c15fb29519256fe37a6aad148`  
		Last Modified: Tue, 19 Mar 2024 19:50:52 GMT  
		Size: 67.4 MB (67376994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb191424e69a8bb8a6be9f12d7e46c4b1369b37491fff6bd81eeccb9a712cc6`  
		Last Modified: Tue, 19 Mar 2024 19:50:41 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b37f7f2ebd35872c656f0820fc315ddc1c3d695c666ef09402005c4cc1852d`  
		Last Modified: Tue, 19 Mar 2024 19:50:41 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:a47e0d4cd725605df06b5bc1fcc8eb693a849c5ddd6337d65815300b329b22f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65112686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0da4d7f455db127e85ce04ed01f5c3e28cb4e1f11d7d716f95da5128336356a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 23:02:20 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 19:23:42 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 19:23:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 19:23:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:23:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:23:43 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:25:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:25:02 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:25:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:25:02 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:25:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:25:02 GMT
USER varnish
# Tue, 19 Mar 2024 19:25:03 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:25:03 GMT
CMD []
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef4ed0e0ad7feb66dd97a52a239ef0ef58422dcd40a031c39b4461500d8784`  
		Last Modified: Tue, 19 Mar 2024 19:35:15 GMT  
		Size: 61.9 MB (61868027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2140d3395b6c8cba74c81342c72ca2c18dc574495773600dcbb7d1704c51ba2`  
		Last Modified: Tue, 19 Mar 2024 19:35:08 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89279a57010ad629819355bee1cf98630a8c3743a4d658fe28695d5e586bc113`  
		Last Modified: Tue, 19 Mar 2024 19:35:08 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:alpine`

```console
$ docker pull varnish@sha256:3a4011e1cb36e5b070f6d134202e980d0f4878f0d03f26682c72a8c1508851e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:alpine` - linux; amd64

```console
$ docker pull varnish@sha256:3faeff6620b5f7240ed712831ed6e7d2e1db892ea9b296b82de23d89fd591a99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73202083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd13adbcd80e61e6f3c26bda7e058d15009f0a20ae20131472a565226e574f7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:58:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 20:02:40 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 20:02:40 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 20:02:41 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 20:02:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 20:02:41 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 20:03:52 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 20:03:52 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 20:03:52 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 20:03:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 20:03:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 20:03:52 GMT
USER varnish
# Tue, 19 Mar 2024 20:03:53 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 20:03:53 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c176d45bcb975cba1b43c0c9e49ce65128387efdfdc17217145873f04a11e1`  
		Last Modified: Tue, 19 Mar 2024 20:11:16 GMT  
		Size: 69.8 MB (69791333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d913ae7181c4f5f8a43290c04e24020c8eb9184528c77eaf8703c38014f77`  
		Last Modified: Tue, 19 Mar 2024 20:11:08 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d41aa7153952f065906cfaf9d8f0422d186bce263716a52a9d7d934daed6a0b`  
		Last Modified: Tue, 19 Mar 2024 20:11:08 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:1c82d437e3fc46d648e4225b36a91481bd5f868c35e1702d7bcc1d9c20d18640
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57409560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266b9b4a0d680e0cd2ff6dced155f16bd284ee39b69e0483ec6103699359a002`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:04:36 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:18:13 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 19:18:14 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 19:18:14 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 19:18:14 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 19:18:15 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:18:15 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 19:18:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 19:18:16 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:18:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:18:17 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:20:43 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:20:43 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:20:44 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:20:45 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:20:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:20:46 GMT
USER varnish
# Tue, 19 Mar 2024 19:20:46 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:20:47 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f8adbcbac98e64fc449be303f6272d2738adb8525204c6901dff554f86fa66`  
		Last Modified: Tue, 19 Mar 2024 19:32:25 GMT  
		Size: 54.5 MB (54488635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3941fb8199245e2961065a39b72e24f8de8af71856809785011bf58a8387a3`  
		Last Modified: Tue, 19 Mar 2024 19:32:17 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79682f92088dfb803f52e91606c36c4f38d6cd5ddce57f483a9e2ef62920304`  
		Last Modified: Tue, 19 Mar 2024 19:32:23 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ec98b2eb6b8667b460891865e7efac5ff91a27f865fc4c36b6b1fd734bbc8cd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69908650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c1d1ec26a3258c847ab32434c2b7bde64ac4beeabc8748d1801080c01ab7dc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:44:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:53:31 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 18:53:31 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 18:53:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:53:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 18:53:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 18:54:32 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 18:54:33 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 18:54:33 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 18:54:33 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 18:54:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 18:54:33 GMT
USER varnish
# Tue, 19 Mar 2024 18:54:33 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 18:54:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d0b6d2fd6cff808b366da93f873d055ce0419948d3444a1bb58808ea47fb3f`  
		Last Modified: Tue, 19 Mar 2024 19:00:52 GMT  
		Size: 66.6 MB (66558909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44994d724b8545ce35ad86ea63237c741cdc823b438f0d6bd598c894642c8179`  
		Last Modified: Tue, 19 Mar 2024 19:00:45 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e930cce73c948215a5db7660fc238edfe4246ba4765a2962c4719e153abc60d`  
		Last Modified: Tue, 19 Mar 2024 19:00:46 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:271cfe5af6514984ccd097b3cce731d5a9c032bc99b52cc47110dbc556768d57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75228860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb431a34bb6cdb93a0f5f2e356b8c965ce3a1fc82f8161532b21fa9bd1145809`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:10:49 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 18:58:27 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:58:28 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 18:58:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 18:58:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:58:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 18:58:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:00:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:00:28 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:00:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:00:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:00:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:00:29 GMT
USER varnish
# Tue, 19 Mar 2024 19:00:29 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:00:29 GMT
CMD []
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113db18c4e7963ab8ca76533a0c77b2c708d3810e54641faa7945eca0c252dcf`  
		Last Modified: Tue, 19 Mar 2024 19:10:14 GMT  
		Size: 72.0 MB (71982747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e877b2d115d0c129cc6f97774e825110e4e6bd3931b8c5f04ce7182ffcba6`  
		Last Modified: Tue, 19 Mar 2024 19:10:00 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25f3f77beb119cded24ad4aab6c67e0513920007e46e9354bc1d57d452efdfb`  
		Last Modified: Tue, 19 Mar 2024 19:10:00 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:dd4d79b176782a5f57f40678bc6650e84e8c9a86073f29466b31fc0c51703082
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70737370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ea74155a1db4e763d97a0f632041aaed697fbd9ffd1648642f8e415d23690c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:04:51 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:38:24 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 19:38:24 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 19:38:24 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 19:38:25 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 19:38:25 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:38:25 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 19:38:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 19:38:26 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:38:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:38:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:39:41 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:39:43 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:39:43 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:39:44 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:39:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:39:44 GMT
USER varnish
# Tue, 19 Mar 2024 19:39:45 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:39:45 GMT
CMD []
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428f744b49685e322e0a893302c92068a1ede30c15fb29519256fe37a6aad148`  
		Last Modified: Tue, 19 Mar 2024 19:50:52 GMT  
		Size: 67.4 MB (67376994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb191424e69a8bb8a6be9f12d7e46c4b1369b37491fff6bd81eeccb9a712cc6`  
		Last Modified: Tue, 19 Mar 2024 19:50:41 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b37f7f2ebd35872c656f0820fc315ddc1c3d695c666ef09402005c4cc1852d`  
		Last Modified: Tue, 19 Mar 2024 19:50:41 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:a47e0d4cd725605df06b5bc1fcc8eb693a849c5ddd6337d65815300b329b22f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65112686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0da4d7f455db127e85ce04ed01f5c3e28cb4e1f11d7d716f95da5128336356a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 23:02:20 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 19:23:42 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 19:23:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 19:23:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:23:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:23:43 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:25:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:25:02 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:25:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:25:02 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:25:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:25:02 GMT
USER varnish
# Tue, 19 Mar 2024 19:25:03 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:25:03 GMT
CMD []
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef4ed0e0ad7feb66dd97a52a239ef0ef58422dcd40a031c39b4461500d8784`  
		Last Modified: Tue, 19 Mar 2024 19:35:15 GMT  
		Size: 61.9 MB (61868027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2140d3395b6c8cba74c81342c72ca2c18dc574495773600dcbb7d1704c51ba2`  
		Last Modified: Tue, 19 Mar 2024 19:35:08 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89279a57010ad629819355bee1cf98630a8c3743a4d658fe28695d5e586bc113`  
		Last Modified: Tue, 19 Mar 2024 19:35:08 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:b872f952fa3532d91627b46c9d7bd61ace423c916cd96e94b8d97530aeae1c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:f72ebe3b392a696053248d7b8e7dfdabfa33791bd141ff47d852e48e18c93007
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134870706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cbd7438657ddb8bdb5f6b5f47755c40a03c0b3e348f6e8dd6d842d9c24076c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:17:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 14:17:47 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 14:17:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 14:17:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 14:17:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 14:17:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 14:17:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 14:17:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 14:17:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 14:17:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 14:17:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:20:30 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 14:20:31 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:20:31 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 14:20:31 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 14:20:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:20:31 GMT
USER varnish
# Tue, 14 May 2024 14:20:32 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:20:32 GMT
CMD []
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413e6b36d364286798878657af0dcccb36d94782a6d2419229eae08912d17455`  
		Last Modified: Tue, 14 May 2024 14:36:14 GMT  
		Size: 105.7 MB (105718284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e66dffca66663ec433a001fc5f077272a46180f57573f9b5ce1452a7a83f55`  
		Last Modified: Tue, 14 May 2024 14:36:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb59e22e9737d1d5781e464a404ade546d918bfa502cbbcc4517d65a7f680b`  
		Last Modified: Tue, 14 May 2024 14:36:00 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:085ff1723c4b074e79adbe248872143338473b731cd7490afef28adb3c4130b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105119153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db54e2c465642301fdacd6668d3395df8e3512f1e531fb8de36272cb117cb0fc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:29:26 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 09:29:26 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 09:29:26 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 09:29:26 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 09:29:26 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 09:29:26 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 09:29:26 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 09:29:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 09:29:27 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 09:29:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 09:29:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:32:07 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 09:32:08 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:32:08 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 09:32:08 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 09:32:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:32:08 GMT
USER varnish
# Tue, 14 May 2024 09:32:08 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:32:08 GMT
CMD []
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c650ad817ba02c0d4e4727081a89c1db1a6286d775da0f2f8fab196660899a55`  
		Last Modified: Tue, 14 May 2024 09:44:31 GMT  
		Size: 80.4 MB (80376936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c68ca8861c02f74b24369f7760ab0139906755818dd0a15e4418d2ada7ffa34`  
		Last Modified: Tue, 14 May 2024 09:44:19 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8f0aa28587e85f7e413f79324a49f39f5de701c02a9870d12d3f7d15703009`  
		Last Modified: Tue, 14 May 2024 09:44:19 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:29c577bfa369c579fcbee8cff6e41fe72263689f245b8f1671d27d6202599a8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129357190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50701c82e1132191d5f63d75d248438bbb5f29014b25fc5bec3f3e4c8c3e5eb4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:36:27 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 07:36:27 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 07:36:27 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 07:36:27 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 07:36:27 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 07:36:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 07:36:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 07:36:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 07:36:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 07:36:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 07:36:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:38:48 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 07:38:50 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:38:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 07:38:50 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 07:38:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:38:50 GMT
USER varnish
# Tue, 14 May 2024 07:38:50 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:38:50 GMT
CMD []
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb62cc8d96dea21946b78774c842df0094506ef45e41526b277f284fb97bb47c`  
		Last Modified: Tue, 14 May 2024 07:49:49 GMT  
		Size: 100.2 MB (100175675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3966f347840524811178eaad61a7e5340413786a2688888f743afe86e1a0a9b`  
		Last Modified: Tue, 14 May 2024 07:49:38 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cf5e226a79576e4a1dc03254d42b5b40fe89c8325674f07dd035f0714efbe7`  
		Last Modified: Tue, 14 May 2024 07:49:38 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:5c0f224d3030b7f84f4bfa6b54269d447cd15eee73980e887dc39a1d05fd1f8d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132039089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e293efa3f248ab5f50cc1921acfc2e8e469a0f81e12431f9cfcd98e08a3df6be`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:36:55 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 08:36:55 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 08:36:55 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 08:36:55 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 08:36:55 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 08:36:56 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 08:36:56 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 08:36:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 08:36:56 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 08:36:56 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 08:36:56 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:40:38 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 08:40:40 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:40:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 08:40:40 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 08:40:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:40:40 GMT
USER varnish
# Tue, 14 May 2024 08:40:40 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:40:40 GMT
CMD []
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b2a8d398f06f001e325035fa52a9e1f2559a0317771d7eed0dfc4f3ec041ca`  
		Last Modified: Tue, 14 May 2024 08:57:00 GMT  
		Size: 101.9 MB (101874440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbd51cfeb5a6e23f7f127eb571ff7791f604966eed44cb694c6a2dd97b4089e`  
		Last Modified: Tue, 14 May 2024 08:56:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699e57a7a26c2cdc5a62b03fb1ae3fdd471c1b324602902354dff65d33a8ea5e`  
		Last Modified: Tue, 14 May 2024 08:56:37 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:0ae43991e3759b15eb00d277fc9dc7c4eb4ae56a6fa79dff7f719c508beb8484
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137799705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c772594d8919b834a3d73ad7fe9e9fffe8dc4ca2777cddef9f57a4dad00f9749`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:16:10 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:16:11 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 06:16:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 06:16:11 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 06:16:11 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 06:16:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:16:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 06:16:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 06:16:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:16:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:16:13 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:20:16 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:20:20 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:20:20 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:20:20 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:20:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:20:21 GMT
USER varnish
# Tue, 14 May 2024 06:20:21 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:20:21 GMT
CMD []
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403b56cebcc3656269beca052096c5e1c11f1672a301a9ee52ae464c2564a49c`  
		Last Modified: Tue, 14 May 2024 06:41:36 GMT  
		Size: 104.7 MB (104656534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada4372d38a4d23cb9c481bc8876c79897d109fb449f4136514ae7c48feb8251`  
		Last Modified: Tue, 14 May 2024 06:41:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18266cc4a11d4c00d9eaed8537bec3c1501f89485f7ff559aa1d02143fb05c5`  
		Last Modified: Tue, 14 May 2024 06:41:19 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:742a183e8ee36555aed72fe43318eb161ed5f5d00fd37dd750de3469bca50c51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112463112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85bd636b03f65a70e70ca62abf48eebae6762e8efee6a75959c259861912f10`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:30:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:30:46 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 06:30:46 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 06:30:46 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 06:30:46 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 06:30:46 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:30:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 06:30:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 06:30:46 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:30:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:30:46 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:33:11 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:33:15 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:33:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:33:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:33:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:33:15 GMT
USER varnish
# Tue, 14 May 2024 06:33:15 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:33:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea2a5e5bd549feabbf3edf8165c5877667fd57501953641b82bb4cc396c4b56`  
		Last Modified: Tue, 14 May 2024 06:44:38 GMT  
		Size: 84.9 MB (84948702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f71635c9c126f4f48e53db27bdd0c2e05b81e3a215b4034716600191d01407a`  
		Last Modified: Tue, 14 May 2024 06:44:27 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0407e5e9f9bdb646351b73c58d732fb18751572de2233d8340f97c944573e2`  
		Last Modified: Tue, 14 May 2024 06:44:27 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:3a4011e1cb36e5b070f6d134202e980d0f4878f0d03f26682c72a8c1508851e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:fresh-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:3faeff6620b5f7240ed712831ed6e7d2e1db892ea9b296b82de23d89fd591a99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73202083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd13adbcd80e61e6f3c26bda7e058d15009f0a20ae20131472a565226e574f7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:58:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 20:02:40 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 20:02:40 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 20:02:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 20:02:41 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 20:02:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 20:02:41 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 20:03:52 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 20:03:52 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 20:03:52 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 20:03:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 20:03:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 20:03:52 GMT
USER varnish
# Tue, 19 Mar 2024 20:03:53 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 20:03:53 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c176d45bcb975cba1b43c0c9e49ce65128387efdfdc17217145873f04a11e1`  
		Last Modified: Tue, 19 Mar 2024 20:11:16 GMT  
		Size: 69.8 MB (69791333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d913ae7181c4f5f8a43290c04e24020c8eb9184528c77eaf8703c38014f77`  
		Last Modified: Tue, 19 Mar 2024 20:11:08 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d41aa7153952f065906cfaf9d8f0422d186bce263716a52a9d7d934daed6a0b`  
		Last Modified: Tue, 19 Mar 2024 20:11:08 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:1c82d437e3fc46d648e4225b36a91481bd5f868c35e1702d7bcc1d9c20d18640
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57409560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266b9b4a0d680e0cd2ff6dced155f16bd284ee39b69e0483ec6103699359a002`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:04:36 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:18:13 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 19:18:14 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 19:18:14 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 19:18:14 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 19:18:15 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:18:15 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 19:18:15 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 19:18:16 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:18:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:18:17 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:20:43 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:20:43 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:20:44 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:20:45 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:20:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:20:46 GMT
USER varnish
# Tue, 19 Mar 2024 19:20:46 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:20:47 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f8adbcbac98e64fc449be303f6272d2738adb8525204c6901dff554f86fa66`  
		Last Modified: Tue, 19 Mar 2024 19:32:25 GMT  
		Size: 54.5 MB (54488635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3941fb8199245e2961065a39b72e24f8de8af71856809785011bf58a8387a3`  
		Last Modified: Tue, 19 Mar 2024 19:32:17 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79682f92088dfb803f52e91606c36c4f38d6cd5ddce57f483a9e2ef62920304`  
		Last Modified: Tue, 19 Mar 2024 19:32:23 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ec98b2eb6b8667b460891865e7efac5ff91a27f865fc4c36b6b1fd734bbc8cd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69908650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c1d1ec26a3258c847ab32434c2b7bde64ac4beeabc8748d1801080c01ab7dc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:44:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:53:31 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 18:53:31 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 18:53:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:53:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 18:53:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 18:54:32 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 18:54:33 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 18:54:33 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 18:54:33 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 18:54:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 18:54:33 GMT
USER varnish
# Tue, 19 Mar 2024 18:54:33 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 18:54:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d0b6d2fd6cff808b366da93f873d055ce0419948d3444a1bb58808ea47fb3f`  
		Last Modified: Tue, 19 Mar 2024 19:00:52 GMT  
		Size: 66.6 MB (66558909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44994d724b8545ce35ad86ea63237c741cdc823b438f0d6bd598c894642c8179`  
		Last Modified: Tue, 19 Mar 2024 19:00:45 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e930cce73c948215a5db7660fc238edfe4246ba4765a2962c4719e153abc60d`  
		Last Modified: Tue, 19 Mar 2024 19:00:46 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:271cfe5af6514984ccd097b3cce731d5a9c032bc99b52cc47110dbc556768d57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75228860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb431a34bb6cdb93a0f5f2e356b8c965ce3a1fc82f8161532b21fa9bd1145809`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:10:49 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 18:58:27 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:58:28 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 18:58:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 18:58:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:58:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 18:58:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:00:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:00:28 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:00:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:00:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:00:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:00:29 GMT
USER varnish
# Tue, 19 Mar 2024 19:00:29 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:00:29 GMT
CMD []
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113db18c4e7963ab8ca76533a0c77b2c708d3810e54641faa7945eca0c252dcf`  
		Last Modified: Tue, 19 Mar 2024 19:10:14 GMT  
		Size: 72.0 MB (71982747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e877b2d115d0c129cc6f97774e825110e4e6bd3931b8c5f04ce7182ffcba6`  
		Last Modified: Tue, 19 Mar 2024 19:10:00 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25f3f77beb119cded24ad4aab6c67e0513920007e46e9354bc1d57d452efdfb`  
		Last Modified: Tue, 19 Mar 2024 19:10:00 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:dd4d79b176782a5f57f40678bc6650e84e8c9a86073f29466b31fc0c51703082
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70737370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ea74155a1db4e763d97a0f632041aaed697fbd9ffd1648642f8e415d23690c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:04:51 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:38:24 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 19:38:24 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 19:38:24 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 19:38:25 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 19:38:25 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:38:25 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 19:38:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 19:38:26 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:38:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:38:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:39:41 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:39:43 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:39:43 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:39:44 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:39:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:39:44 GMT
USER varnish
# Tue, 19 Mar 2024 19:39:45 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:39:45 GMT
CMD []
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428f744b49685e322e0a893302c92068a1ede30c15fb29519256fe37a6aad148`  
		Last Modified: Tue, 19 Mar 2024 19:50:52 GMT  
		Size: 67.4 MB (67376994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb191424e69a8bb8a6be9f12d7e46c4b1369b37491fff6bd81eeccb9a712cc6`  
		Last Modified: Tue, 19 Mar 2024 19:50:41 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b37f7f2ebd35872c656f0820fc315ddc1c3d695c666ef09402005c4cc1852d`  
		Last Modified: Tue, 19 Mar 2024 19:50:41 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:a47e0d4cd725605df06b5bc1fcc8eb693a849c5ddd6337d65815300b329b22f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65112686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0da4d7f455db127e85ce04ed01f5c3e28cb4e1f11d7d716f95da5128336356a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 23:02:20 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 19:23:42 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:23:42 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 19:23:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 19:23:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:23:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:23:43 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:25:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:25:02 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:25:02 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:25:02 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:25:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:25:02 GMT
USER varnish
# Tue, 19 Mar 2024 19:25:03 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:25:03 GMT
CMD []
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cef4ed0e0ad7feb66dd97a52a239ef0ef58422dcd40a031c39b4461500d8784`  
		Last Modified: Tue, 19 Mar 2024 19:35:15 GMT  
		Size: 61.9 MB (61868027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2140d3395b6c8cba74c81342c72ca2c18dc574495773600dcbb7d1704c51ba2`  
		Last Modified: Tue, 19 Mar 2024 19:35:08 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89279a57010ad629819355bee1cf98630a8c3743a4d658fe28695d5e586bc113`  
		Last Modified: Tue, 19 Mar 2024 19:35:08 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:b872f952fa3532d91627b46c9d7bd61ace423c916cd96e94b8d97530aeae1c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:f72ebe3b392a696053248d7b8e7dfdabfa33791bd141ff47d852e48e18c93007
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134870706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cbd7438657ddb8bdb5f6b5f47755c40a03c0b3e348f6e8dd6d842d9c24076c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:17:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 14:17:47 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 14:17:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 14:17:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 14:17:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 14:17:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 14:17:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 14:17:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 14:17:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 14:17:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 14:17:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:20:30 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 14:20:31 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:20:31 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 14:20:31 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 14:20:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:20:31 GMT
USER varnish
# Tue, 14 May 2024 14:20:32 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:20:32 GMT
CMD []
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413e6b36d364286798878657af0dcccb36d94782a6d2419229eae08912d17455`  
		Last Modified: Tue, 14 May 2024 14:36:14 GMT  
		Size: 105.7 MB (105718284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e66dffca66663ec433a001fc5f077272a46180f57573f9b5ce1452a7a83f55`  
		Last Modified: Tue, 14 May 2024 14:36:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb59e22e9737d1d5781e464a404ade546d918bfa502cbbcc4517d65a7f680b`  
		Last Modified: Tue, 14 May 2024 14:36:00 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:085ff1723c4b074e79adbe248872143338473b731cd7490afef28adb3c4130b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105119153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db54e2c465642301fdacd6668d3395df8e3512f1e531fb8de36272cb117cb0fc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:29:26 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 09:29:26 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 09:29:26 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 09:29:26 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 09:29:26 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 09:29:26 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 09:29:26 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 09:29:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 09:29:27 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 09:29:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 09:29:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:32:07 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 09:32:08 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:32:08 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 09:32:08 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 09:32:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:32:08 GMT
USER varnish
# Tue, 14 May 2024 09:32:08 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:32:08 GMT
CMD []
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c650ad817ba02c0d4e4727081a89c1db1a6286d775da0f2f8fab196660899a55`  
		Last Modified: Tue, 14 May 2024 09:44:31 GMT  
		Size: 80.4 MB (80376936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c68ca8861c02f74b24369f7760ab0139906755818dd0a15e4418d2ada7ffa34`  
		Last Modified: Tue, 14 May 2024 09:44:19 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8f0aa28587e85f7e413f79324a49f39f5de701c02a9870d12d3f7d15703009`  
		Last Modified: Tue, 14 May 2024 09:44:19 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:29c577bfa369c579fcbee8cff6e41fe72263689f245b8f1671d27d6202599a8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129357190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50701c82e1132191d5f63d75d248438bbb5f29014b25fc5bec3f3e4c8c3e5eb4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:36:27 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 07:36:27 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 07:36:27 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 07:36:27 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 07:36:27 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 07:36:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 07:36:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 07:36:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 07:36:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 07:36:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 07:36:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:38:48 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 07:38:50 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:38:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 07:38:50 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 07:38:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:38:50 GMT
USER varnish
# Tue, 14 May 2024 07:38:50 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:38:50 GMT
CMD []
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb62cc8d96dea21946b78774c842df0094506ef45e41526b277f284fb97bb47c`  
		Last Modified: Tue, 14 May 2024 07:49:49 GMT  
		Size: 100.2 MB (100175675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3966f347840524811178eaad61a7e5340413786a2688888f743afe86e1a0a9b`  
		Last Modified: Tue, 14 May 2024 07:49:38 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cf5e226a79576e4a1dc03254d42b5b40fe89c8325674f07dd035f0714efbe7`  
		Last Modified: Tue, 14 May 2024 07:49:38 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:5c0f224d3030b7f84f4bfa6b54269d447cd15eee73980e887dc39a1d05fd1f8d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132039089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e293efa3f248ab5f50cc1921acfc2e8e469a0f81e12431f9cfcd98e08a3df6be`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:36:55 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 08:36:55 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 08:36:55 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 08:36:55 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 08:36:55 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 08:36:56 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 08:36:56 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 08:36:56 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 08:36:56 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 08:36:56 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 08:36:56 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:40:38 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 08:40:40 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:40:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 08:40:40 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 08:40:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:40:40 GMT
USER varnish
# Tue, 14 May 2024 08:40:40 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:40:40 GMT
CMD []
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b2a8d398f06f001e325035fa52a9e1f2559a0317771d7eed0dfc4f3ec041ca`  
		Last Modified: Tue, 14 May 2024 08:57:00 GMT  
		Size: 101.9 MB (101874440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbd51cfeb5a6e23f7f127eb571ff7791f604966eed44cb694c6a2dd97b4089e`  
		Last Modified: Tue, 14 May 2024 08:56:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699e57a7a26c2cdc5a62b03fb1ae3fdd471c1b324602902354dff65d33a8ea5e`  
		Last Modified: Tue, 14 May 2024 08:56:37 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:0ae43991e3759b15eb00d277fc9dc7c4eb4ae56a6fa79dff7f719c508beb8484
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137799705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c772594d8919b834a3d73ad7fe9e9fffe8dc4ca2777cddef9f57a4dad00f9749`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:16:10 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:16:11 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 06:16:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 06:16:11 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 06:16:11 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 06:16:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:16:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 06:16:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 06:16:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:16:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:16:13 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:20:16 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:20:20 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:20:20 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:20:20 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:20:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:20:21 GMT
USER varnish
# Tue, 14 May 2024 06:20:21 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:20:21 GMT
CMD []
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403b56cebcc3656269beca052096c5e1c11f1672a301a9ee52ae464c2564a49c`  
		Last Modified: Tue, 14 May 2024 06:41:36 GMT  
		Size: 104.7 MB (104656534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada4372d38a4d23cb9c481bc8876c79897d109fb449f4136514ae7c48feb8251`  
		Last Modified: Tue, 14 May 2024 06:41:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18266cc4a11d4c00d9eaed8537bec3c1501f89485f7ff559aa1d02143fb05c5`  
		Last Modified: Tue, 14 May 2024 06:41:19 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:742a183e8ee36555aed72fe43318eb161ed5f5d00fd37dd750de3469bca50c51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112463112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85bd636b03f65a70e70ca62abf48eebae6762e8efee6a75959c259861912f10`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:30:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:30:46 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 14 May 2024 06:30:46 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 14 May 2024 06:30:46 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 14 May 2024 06:30:46 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 14 May 2024 06:30:46 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:30:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 14 May 2024 06:30:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 14 May 2024 06:30:46 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:30:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:30:46 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:33:11 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:33:15 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:33:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:33:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:33:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:33:15 GMT
USER varnish
# Tue, 14 May 2024 06:33:15 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:33:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea2a5e5bd549feabbf3edf8165c5877667fd57501953641b82bb4cc396c4b56`  
		Last Modified: Tue, 14 May 2024 06:44:38 GMT  
		Size: 84.9 MB (84948702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f71635c9c126f4f48e53db27bdd0c2e05b81e3a215b4034716600191d01407a`  
		Last Modified: Tue, 14 May 2024 06:44:27 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0407e5e9f9bdb646351b73c58d732fb18751572de2233d8340f97c944573e2`  
		Last Modified: Tue, 14 May 2024 06:44:27 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old`

```console
$ docker pull varnish@sha256:882224e47d7db63a17dce924bf9033b5181a2a3a0fedee09e9aa40c0207f9ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:b8370ea0069c03b3b14ae335d01ac6fe9c1a2416cb58a04374c7a05f794f5696
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134784916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a18216991f6a1afd692fb5920e9d02abf542c16b6d2d673ee4dcd3b155a3d5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:17:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 14:20:43 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 14:20:43 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 14:20:43 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 14:20:43 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 14:20:43 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 14:20:43 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 14:20:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 14:20:44 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 14:20:44 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 14:20:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:26:17 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 14:26:18 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:26:18 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 14:26:18 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 14:26:18 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:26:18 GMT
USER varnish
# Tue, 14 May 2024 14:26:18 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:26:18 GMT
CMD []
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a16974ae153bf113b00ccc0fbf36aac224d2dc680479303298885c6dc18e369`  
		Last Modified: Tue, 14 May 2024 14:36:43 GMT  
		Size: 105.6 MB (105632491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5013aecdda5901d37096b63257c04c84531732b0b32bc00be4f8adb51cbd503`  
		Last Modified: Tue, 14 May 2024 14:36:29 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6d6e7a17e4ee13e1459b04a4a679c4d3ba359f49edf76e98919f4cbbab2b27`  
		Last Modified: Tue, 14 May 2024 14:36:29 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:4583809dc8bdcc3a40334d41ed24522463163aaae73022d6f0c53e4f89ea0fc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105004879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68a526a0cb0674dac743036b5c1580beec513788e0155f2ef8a489808be285d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:29:26 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 09:32:20 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 09:32:21 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 09:32:21 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 09:32:21 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 09:32:21 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 09:32:21 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 09:32:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 09:32:21 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 09:32:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 09:32:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:34:47 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 09:34:48 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:34:48 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 09:34:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 09:34:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:34:49 GMT
USER varnish
# Tue, 14 May 2024 09:34:49 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:34:49 GMT
CMD []
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d2699d7174ee2e3ec604bfeb786dd77e9eedf5d0a48877a3273f650c5077c0`  
		Last Modified: Tue, 14 May 2024 09:44:56 GMT  
		Size: 80.3 MB (80262661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60f9712404c431a4fd8b84805e3a650f223a1422c848b02681e410bb739754`  
		Last Modified: Tue, 14 May 2024 09:44:44 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fa61b2a01fe31985e791b88be9e0288fd610dde76d73b68f1426b2887fecdc`  
		Last Modified: Tue, 14 May 2024 09:44:44 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:2ac2a3ad2e8ef37460b50bf8ae3afefbee38523eb0aaee01f7d6a5e2c3fdb3b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129270960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e44b842694bd08afb5258b5ecd852a0b2b78d9a72bca12ea1cda6a774488be5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:36:27 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 07:39:07 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 07:39:07 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 07:39:07 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 07:39:07 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 07:39:07 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 07:39:07 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 07:39:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 07:39:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 07:39:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 07:39:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:41:14 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 07:41:16 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:41:16 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 07:41:16 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 07:41:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:41:16 GMT
USER varnish
# Tue, 14 May 2024 07:41:16 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:41:16 GMT
CMD []
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048b118ca13512abdb6cfc328a5341657e791ccb3ab8790a8f2b12ac3c31d858`  
		Last Modified: Tue, 14 May 2024 07:50:14 GMT  
		Size: 100.1 MB (100089445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eebca74f010bc1af9b8dda398fbc899b6407212646e1cf52d00a5b8b55b03ab`  
		Last Modified: Tue, 14 May 2024 07:50:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0ff9860e00c9b930e05109dc282db9d300a0457af0d0c59351d49ec164ba61`  
		Last Modified: Tue, 14 May 2024 07:50:02 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:1a9742bfb4ce30721c6ca2fb5520c15305d749e160ec5611cd50e8790eebc63e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131930287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bc76427f2017543e41070e746fc91d73dfb0c21a092175637a91b6bc9d2874`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:36:55 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 08:40:50 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 08:40:50 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 08:40:50 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 08:40:50 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 08:40:50 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 08:40:50 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 08:40:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 08:40:51 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 08:40:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 08:40:51 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:44:17 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 08:44:18 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:44:18 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 08:44:18 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 08:44:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:44:19 GMT
USER varnish
# Tue, 14 May 2024 08:44:19 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:44:19 GMT
CMD []
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc2369f33a43201c69e5e6ad92aeac3ded2c005a5c3706aeb78ba01830e5a63`  
		Last Modified: Tue, 14 May 2024 08:57:36 GMT  
		Size: 101.8 MB (101765638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bd0d0328766529f5a2016fa7b7ec510ffecc1ba0cab060ed4fef646c928e15`  
		Last Modified: Tue, 14 May 2024 08:57:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2f2768da2b8d37692d1c75568c404df85dc71979e9d7d8853eb282addf1d86`  
		Last Modified: Tue, 14 May 2024 08:57:14 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:3ab6c8b9e140978901343919b2cace41958092e19e671810122ebce933b12a76
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137714757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972cca6f54c3a511281a9ebc05c802367bd39316298842c4b6183435f736ff97`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:16:10 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:20:38 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 06:20:38 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 06:20:38 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 06:20:38 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 06:20:39 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:20:39 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 06:20:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 06:20:39 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:20:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:20:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:24:45 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:24:50 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:24:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:24:50 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:24:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:24:51 GMT
USER varnish
# Tue, 14 May 2024 06:24:51 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:24:51 GMT
CMD []
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426fac7e303070a52e77a623a26e18a04b9bc1ed6c91073683d85327b983ef85`  
		Last Modified: Tue, 14 May 2024 06:42:06 GMT  
		Size: 104.6 MB (104571587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320391667901aac1e14c6f05c8a445467f80196650c05b69b226e68c2c048887`  
		Last Modified: Tue, 14 May 2024 06:41:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b06fc6a3aab74a784600134ec69349d5cd9892a1c4fb30280e0e7c4f049882`  
		Last Modified: Tue, 14 May 2024 06:41:49 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:db3133a8388660ac154a58e136a49b0065223533421dd29486e98dc39ca9df22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112365129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7434c2abce66b312ebf0f4009a2e2d2111a9257362cefabd0f244b26fc9ab3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:30:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 14 May 2024 06:33:31 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 14 May 2024 06:33:31 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 14 May 2024 06:33:31 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 14 May 2024 06:33:31 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 14 May 2024 06:33:31 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 14 May 2024 06:33:32 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 14 May 2024 06:33:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 14 May 2024 06:33:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 14 May 2024 06:33:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 14 May 2024 06:33:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:35:41 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 14 May 2024 06:35:44 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:35:44 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 14 May 2024 06:35:45 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 14 May 2024 06:35:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:35:45 GMT
USER varnish
# Tue, 14 May 2024 06:35:45 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:35:45 GMT
CMD []
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df8730d37f1330b10295cfd34b8376a58bc64bf2d8198e0b45334700003fbd6`  
		Last Modified: Tue, 14 May 2024 06:44:59 GMT  
		Size: 84.9 MB (84850723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f69700bb9b4d260724360cb436e12ef933d83342415b05dab002efb950930f`  
		Last Modified: Tue, 14 May 2024 06:44:47 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffb8a880c88bb62724629c502991052f5d79ccd0f05d405bc80a52b9c53e738`  
		Last Modified: Tue, 14 May 2024 06:44:47 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:2c6ab5471f574fd6cdb1b89da00b72ba870512959529d43c648fec5ff81a2322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:bad41538a520c7324ae66672afcd1843244ff3fd6a69dc186fffabb26e5e5b3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73111717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fcd1daa5a1fd515be57af3744ca44fd77a3aff504e0813f18881ba362df461`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:58:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 20:06:43 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 20:06:43 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 20:06:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 20:06:44 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 20:06:44 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 20:06:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 20:08:04 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 20:08:04 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 20:08:04 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 20:08:05 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 20:08:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 20:08:05 GMT
USER varnish
# Tue, 19 Mar 2024 20:08:05 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 20:08:05 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e88fbcf523fb9f70c926ce56e3d01391ed2c58556c7fed0504edee8f38f1599`  
		Last Modified: Tue, 19 Mar 2024 20:12:02 GMT  
		Size: 69.7 MB (69700966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73d56dea7353d1ce78b162cf126e47cb61ed2436148992e6973adba9df7a26f`  
		Last Modified: Tue, 19 Mar 2024 20:11:53 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d86a9601c89cd35fb0e08c0495b786d5c0fd08804adbc6cf16ceabede21ed6`  
		Last Modified: Tue, 19 Mar 2024 20:11:53 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:d8d8d456b3b22b0a1717e09faa1a04161ca2b812536f9fcc981531f8ada51710
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57316383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31c572f46d3e2f829a48ec29edf234b8908aff261f843e8008c27792c881c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:04:36 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:25:16 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 19:25:16 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 19:25:17 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 19:25:17 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 19:25:18 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:25:18 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 19:25:18 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 19:25:19 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:25:19 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:25:19 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:27:54 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 19:27:55 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:27:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:27:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:27:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:27:57 GMT
USER varnish
# Tue, 19 Mar 2024 19:27:57 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:27:58 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb32a9d2bc9510faba817c92bfe1cf189ad3cfd884457c74f7933aed86df6eb`  
		Last Modified: Tue, 19 Mar 2024 19:33:10 GMT  
		Size: 54.4 MB (54395458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001be72dd77327edce535297b918c11d2092b608be216951ffe22e818dd361d1`  
		Last Modified: Tue, 19 Mar 2024 19:33:02 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02b8aa68970246d2ae92e63dd681f9788e02bb390ef1e86b69bd42087bca281`  
		Last Modified: Tue, 19 Mar 2024 19:33:02 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:479ea6daf1d1ddb36de834aa28c5e64c8a4883f743eed493192255ce9f795df1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69813716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be2438e6775bff4a85bde81ac5d9c06ac7d183b8d6ce2edea5db9b89655cc4c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:44:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 18:57:04 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 18:57:04 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 18:57:04 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:57:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 18:57:04 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 18:58:12 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 18:58:12 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 18:58:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 18:58:13 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 18:58:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 18:58:13 GMT
USER varnish
# Tue, 19 Mar 2024 18:58:13 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 18:58:13 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894a7285b926312b215684e50114187e34f58603947ba360a068c707e8c90cfd`  
		Last Modified: Tue, 19 Mar 2024 19:01:30 GMT  
		Size: 66.5 MB (66463974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf21108d62a7fd3c9304838a0e7d38d87a8b2aaea9be4002b48b0debcfb122a`  
		Last Modified: Tue, 19 Mar 2024 19:01:24 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b1b0f8e8b6fe88f280d6f8a38df3be1e85d89988fb2386fb5a8b6b171772d3`  
		Last Modified: Tue, 19 Mar 2024 19:01:24 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:1fdf700b9bf5114292511d5f9b8410f030a420195edc7822ff168350517f134e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75135148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f375513ff93e5dcf88d1563c073de2cbed2e3d5b7d77236f1550cd1af8c6a4be`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:10:49 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:04:13 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 19:04:13 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 19:04:13 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 19:04:14 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 19:04:14 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:04:14 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 19:04:14 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 19:04:14 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:04:14 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:04:14 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:06:19 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 19:06:19 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:06:19 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:06:19 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:06:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:06:20 GMT
USER varnish
# Tue, 19 Mar 2024 19:06:20 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:06:20 GMT
CMD []
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a30e445c3604537fdf8df8c22a060202d20489b8eddfa77f4550fe4f911650`  
		Last Modified: Tue, 19 Mar 2024 19:11:11 GMT  
		Size: 71.9 MB (71889037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4152d250362e0e5bf5357d66457786d213f1d15255388a3bb7c01c3f2052d5`  
		Last Modified: Tue, 19 Mar 2024 19:10:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2737032c6f8bcdf0a71d104e82734a6b69555856e39ecff4ef201d8b391fd949`  
		Last Modified: Tue, 19 Mar 2024 19:10:57 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:cbcdf4a72047647d6e472f95a475d99778629b31fa07a868c0e8f6ee6c329013
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70642273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817de67047306f66d083abae50517fcfa5851ece50b2da689d6cbb59802870bd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:04:51 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:44:28 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 19:44:29 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 19:44:29 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 19:44:29 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 19:44:30 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:44:30 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 19:44:30 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 19:44:30 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:44:31 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:44:31 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:45:51 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 19:45:54 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:45:54 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:45:54 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:45:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:45:55 GMT
USER varnish
# Tue, 19 Mar 2024 19:45:55 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:45:55 GMT
CMD []
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743250632b3e83457d746dd80c83c1792da89dcac7861cfbe4e0ced8ff47f129`  
		Last Modified: Tue, 19 Mar 2024 19:51:43 GMT  
		Size: 67.3 MB (67281893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9d99e7af2f3afb5934553c41f70a80f5fa99509365d3f33bebb6089dcd9461`  
		Last Modified: Tue, 19 Mar 2024 19:51:33 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f77c02b1d17e9e7dcf8169ca83ef8b3325640b7d59994287907bad7312790`  
		Last Modified: Tue, 19 Mar 2024 19:51:33 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:1b30229155355ad2c6b66e8e72eddc263f19d9cd02ea6017fa667301d5a27b85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65011686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697ae126a2c8542caeb132c89923bbb9ac0034c03f83099f8fd649c1782a34a3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 23:02:20 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 19:29:26 GMT
ARG VARNISH_VERSION=7.4.3
# Tue, 19 Mar 2024 19:29:27 GMT
ARG DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Tue, 19 Mar 2024 19:29:27 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Tue, 19 Mar 2024 19:29:27 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 19:29:27 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 19:29:27 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:30:52 GMT
# ARGS: DIST_SHA512=2530e913abc34b4afbfaf22a562e596141f855ed6af9c58c211ff5b76c12a0df6d7101af02994ff8b3c031be35e3fade3963dfec44ddd7d270e0d8535e4360f2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.3 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Tue, 19 Mar 2024 19:30:54 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:30:54 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:30:55 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:30:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:30:55 GMT
USER varnish
# Tue, 19 Mar 2024 19:30:55 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:30:55 GMT
CMD []
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe38f977ea67683ee4420495875859583d5281a008b4d6aed6e1d588f2f0806`  
		Last Modified: Tue, 19 Mar 2024 19:35:51 GMT  
		Size: 61.8 MB (61767029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c60b2806d71370deb7439b9951f3eb3c198692c33e1f8286d755dc93bdbee9`  
		Last Modified: Tue, 19 Mar 2024 19:35:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d1a215e014825ed08ff1940cdbfc607d4163f6608a016f2cca535243352213`  
		Last Modified: Tue, 19 Mar 2024 19:35:44 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:eb5b5923785da107b84db2f896cc90d654c14ed335123c16fbbf8d8fa17dacc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:3be84605f51934b662a1fd32c03d982f9235468fdb8427f2d20fa1c8429dc4a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95874783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9aa8a59b93ff62a0d1e53b9cbd4026c35668b03c79c4969bf8746954b5a9fbe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 14:26:32 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 14:26:32 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 14:26:32 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 14:26:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 14:28:21 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 14:28:21 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 14:28:21 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 14:28:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 14:28:21 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 14:28:22 GMT
CMD []
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359f8f3a4792f96c1720dfd7f4dd952889d4ab9344eb0fe9413ffffc2229b61a`  
		Last Modified: Tue, 14 May 2024 14:37:03 GMT  
		Size: 64.4 MB (64440136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0385c17efd750567c8ab5fce43768872bc80277f323daa30421423f5c8f598a`  
		Last Modified: Tue, 14 May 2024 14:36:54 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:56f3662203529fca4d1f77533683ba3d50392d0a8e33a7b17d00def46c101b65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72870716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7b9d0eb1054b63a01be7fe1c035340bf0a4ad3c10879eb62f9e0358c60f7fb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:35:00 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 09:35:00 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 09:35:00 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 09:35:00 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 09:36:47 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 09:36:47 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 09:36:48 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 09:36:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 09:36:48 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 09:36:48 GMT
CMD []
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f106de5cb49a4793119ff373fe3b357fc2eed6a8825ca5516e4b0f113a9271`  
		Last Modified: Tue, 14 May 2024 09:45:13 GMT  
		Size: 46.3 MB (46275509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4360686e3bc89571cb56e34c207bf1c03b274f41f9f0efc016795bf2ee8e822`  
		Last Modified: Tue, 14 May 2024 09:45:07 GMT  
		Size: 714.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a21d622cce0cfc37c7923b5405f569e8d5dd5434cc40583cfd5c6ed71544bd85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89977458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3d300d8903dff396e57d3e6e86b7f065db5cb2c7c0dbbd5e11e34adb97ca23`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:41:33 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 07:41:33 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 07:41:33 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 07:41:33 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 07:43:01 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 07:43:01 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 07:43:01 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 07:43:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 07:43:01 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 07:43:02 GMT
CMD []
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e142232f2ce3e867f9128875cf61777e5e40c82eb952700a7896f5a16901a0`  
		Last Modified: Tue, 14 May 2024 07:50:31 GMT  
		Size: 59.9 MB (59889832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c0ecccf7b958b1578b188ef2833a7365f17b5a62ba9227b337f41e137076e7`  
		Last Modified: Tue, 14 May 2024 07:50:25 GMT  
		Size: 718.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:fae67428c9fbfac1d3bafbb56d810446a2dc60497ac3341f640cfd4a24fd7aeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97146491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1d4b8a8f9c33f0bb44f64d7ad8166752b52f58da7a88086e0cac799831c38`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:47:34 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 14 May 2024 00:47:34 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:44:30 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 08:44:30 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 08:44:30 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 08:44:30 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 08:46:47 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 08:46:48 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 08:46:48 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 08:46:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 08:46:49 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 08:46:49 GMT
CMD []
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f907ff471f0851875703285eb6d0ef438811d491aadb5aba748aa312476aeda`  
		Last Modified: Tue, 14 May 2024 08:57:59 GMT  
		Size: 64.7 MB (64721732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18e6804a4d99f5cc0febeea741d31d1ed3388b1f166485bba629841e4a9fc6f`  
		Last Modified: Tue, 14 May 2024 08:57:47 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:cdc5925f33e2f3d2766f8f221d3f3dd8ce814a4387b8ce60bbde786d9ba097bc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94661580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98390a649c51397783ed4d8fe780ca0f05dc4f989c8d00aef9ac970fabff2136`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:25:05 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 06:25:05 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 06:25:06 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 06:25:06 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:28:35 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 06:28:38 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:28:38 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 06:28:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:28:38 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:28:39 GMT
CMD []
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dfefba4fba615398a7eab3e3342d67dcf7df7f8e6cac0f28d30001ab1684e5`  
		Last Modified: Tue, 14 May 2024 06:42:28 GMT  
		Size: 59.3 MB (59349704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f01dbfb3e2cfaa17b94584fd9fcb792d0ee168bcb7891a67a3d3d2feae19f5`  
		Last Modified: Tue, 14 May 2024 06:42:18 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:c9887b4336fa3addcaa27879c77b53e03af001a369ad6a8abff832e56c356b56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deacee544cdd187a45643da0b7bc6eeedf17ba7641ea2f1e758deeda3adbd530`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 14 May 2024 00:43:11 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Tue, 14 May 2024 00:43:13 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:36:02 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 14 May 2024 06:36:02 GMT
ARG VARNISH_VERSION=6.0.13
# Tue, 14 May 2024 06:36:02 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Tue, 14 May 2024 06:36:03 GMT
ENV VARNISH_SIZE=100M
# Tue, 14 May 2024 06:37:27 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Tue, 14 May 2024 06:37:29 GMT
WORKDIR /etc/varnish
# Tue, 14 May 2024 06:37:29 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Tue, 14 May 2024 06:37:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 14 May 2024 06:37:30 GMT
EXPOSE 80 8443
# Tue, 14 May 2024 06:37:30 GMT
CMD []
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a4866f0e934710827a963ac4a2533e21008525af1ba9fdb2b354138060dd70`  
		Last Modified: Tue, 14 May 2024 06:45:13 GMT  
		Size: 46.6 MB (46596547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8339ee670ce12c69916f24743f49512e75d61dc5c928b10db3b0442836475`  
		Last Modified: Tue, 14 May 2024 06:45:07 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
