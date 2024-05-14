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
