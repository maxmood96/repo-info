<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.13`](#varnish6013)
-	[`varnish:7`](#varnish7)
-	[`varnish:7-alpine`](#varnish7-alpine)
-	[`varnish:7.5`](#varnish75)
-	[`varnish:7.5-alpine`](#varnish75-alpine)
-	[`varnish:7.5.0`](#varnish750)
-	[`varnish:7.5.0-alpine`](#varnish750-alpine)
-	[`varnish:7.6`](#varnish76)
-	[`varnish:7.6-alpine`](#varnish76-alpine)
-	[`varnish:7.6.0`](#varnish760)
-	[`varnish:7.6.0-alpine`](#varnish760-alpine)
-	[`varnish:alpine`](#varnishalpine)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:fresh-alpine`](#varnishfresh-alpine)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:bfd6cf3bc107200b6feac23071cce59ce28e910805e58f97b67280721e062c0c
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
$ docker pull varnish@sha256:672b71e5883cefd983bab2dbf3634f2cc5ee0ef341bfb33050446e5dfd4f8595
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95867078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6057c46accf738b2d68e68f5803b049689957714857a4e3270b7965b2ee098c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:56:53 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 27 Sep 2024 07:56:53 GMT
ARG VARNISH_VERSION=6.0.13
# Fri, 27 Sep 2024 07:56:54 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Fri, 27 Sep 2024 07:56:54 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:58:40 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Fri, 27 Sep 2024 07:58:40 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:58:40 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:58:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:58:40 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:58:40 GMT
CMD []
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b6651c40c47f71c9486af005d55471e17d8a90aa852ed051a7e4ba1a3348ed`  
		Last Modified: Fri, 27 Sep 2024 07:59:56 GMT  
		Size: 64.4 MB (64437764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c046b9fb8849d1f1d68eedb3fc15fdb5469610f06a54ba908d173d8e396feb1`  
		Last Modified: Fri, 27 Sep 2024 07:59:48 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c0e75a091223dc30da50c78da9b32dfb6ebf8a61a7fde62ac08d72c8b9e4f86e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72864140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc154e7c6bb5593ea4e110cdf1869c0059bf606d05dbeb397be19e9f36296758`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 05:14:05 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
# Fri, 27 Sep 2024 05:14:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:26:26 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 27 Sep 2024 07:26:27 GMT
ARG VARNISH_VERSION=6.0.13
# Fri, 27 Sep 2024 07:26:27 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Fri, 27 Sep 2024 07:26:27 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:28:28 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Fri, 27 Sep 2024 07:28:28 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:28:28 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:28:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:28:29 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:28:29 GMT
CMD []
```

-	Layers:
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7d4933da79ac1087836dc24bfb8ba8ae3e80cede005988a89d4e7d8feaf874`  
		Last Modified: Fri, 27 Sep 2024 07:29:38 GMT  
		Size: 46.3 MB (46274112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e705e915ccaa6302ee24bc00b349bdb9403be35b7a813145cbaeda347828b49a`  
		Last Modified: Fri, 27 Sep 2024 07:29:32 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f5f81da76f5e69e98006b3733a4f9082952033d459558e9fa56c8ed915c752db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89961577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d6730b0996d43d67c19836bd61d7fbebe76ff38bb1fafb246e2ea97e9e695c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:32:04 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 27 Sep 2024 07:32:04 GMT
ARG VARNISH_VERSION=6.0.13
# Fri, 27 Sep 2024 07:32:04 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Fri, 27 Sep 2024 07:32:04 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:33:35 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Fri, 27 Sep 2024 07:33:36 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:33:36 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:33:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:33:36 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:33:36 GMT
CMD []
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c11049a7bb44f1c287f63d0c337404483102a7055f33124aea5fe489ca9589`  
		Last Modified: Fri, 27 Sep 2024 07:34:46 GMT  
		Size: 59.9 MB (59885703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b81c9012312de01b188f659e443f50952e138bac1371b03dc84558f10849b7`  
		Last Modified: Fri, 27 Sep 2024 07:34:39 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; 386

```console
$ docker pull varnish@sha256:173b1de36a4d17ea1799e1bb74537b5f2fcb43312e8cbfa78dfe515479d8ab66
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97132611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4177ce3a56a71e449c2a875605082cf5ccb475126d7ebbf33fd937f9ac9e6abc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 07:23:23 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
# Fri, 27 Sep 2024 07:23:24 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:54:25 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 27 Sep 2024 07:54:25 GMT
ARG VARNISH_VERSION=6.0.13
# Fri, 27 Sep 2024 07:54:26 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Fri, 27 Sep 2024 07:54:26 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:56:46 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Fri, 27 Sep 2024 07:56:46 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:56:46 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:56:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:56:47 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:56:47 GMT
CMD []
```

-	Layers:
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de14ddae1aa0ebd1b4b6f365a428f18241ed79c7eca15ad87985885fea17625c`  
		Last Modified: Fri, 27 Sep 2024 07:58:29 GMT  
		Size: 64.7 MB (64718399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389ed122f33c9b42cd54aa8e4e994ff51e0787b7e1daa8a74d1393654a944fa0`  
		Last Modified: Fri, 27 Sep 2024 07:58:17 GMT  
		Size: 713.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:053579a9edb1c0ecd98f26ada06d72fcfeb69ed1e49940c05e60e25ff5f25371
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94647026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fd07f2ef42ca87942053c400a4785380dce3bb54e606fb1d63097a8cfe068f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 04 Sep 2024 22:26:18 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Wed, 04 Sep 2024 22:26:20 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:27:32 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Wed, 04 Sep 2024 23:27:33 GMT
ARG VARNISH_VERSION=6.0.13
# Wed, 04 Sep 2024 23:27:34 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Wed, 04 Sep 2024 23:27:34 GMT
ENV VARNISH_SIZE=100M
# Wed, 04 Sep 2024 23:30:49 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 04 Sep 2024 23:30:51 GMT
WORKDIR /etc/varnish
# Wed, 04 Sep 2024 23:30:52 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Wed, 04 Sep 2024 23:30:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 04 Sep 2024 23:30:52 GMT
EXPOSE 80 8443
# Wed, 04 Sep 2024 23:30:53 GMT
CMD []
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ad53399901533b0371d62560f54aaa95448a92fa2cc0e637b23440ebec222b`  
		Last Modified: Wed, 04 Sep 2024 23:44:07 GMT  
		Size: 59.3 MB (59347035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4eb9dcfc226e07bc3c4fa4ab30656eda5ab65803c658f6082bccdd1e5edfac`  
		Last Modified: Wed, 04 Sep 2024 23:43:57 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0` - linux; s390x

```console
$ docker pull varnish@sha256:32841bc0f7503dfd6c456ad94c8f78007b3100045965cadbe18f456099ac8abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76258728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded5fdd03ff15a069138878b85906a9196b3fc3ba8c26fafc22d244e44a35304`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 04 Sep 2024 21:43:26 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Wed, 04 Sep 2024 21:43:27 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:09:00 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Thu, 05 Sep 2024 00:09:00 GMT
ARG VARNISH_VERSION=6.0.13
# Thu, 05 Sep 2024 00:09:01 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Thu, 05 Sep 2024 00:09:01 GMT
ENV VARNISH_SIZE=100M
# Thu, 05 Sep 2024 00:10:22 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 05 Sep 2024 00:10:23 GMT
WORKDIR /etc/varnish
# Thu, 05 Sep 2024 00:10:23 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Thu, 05 Sep 2024 00:10:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 05 Sep 2024 00:10:23 GMT
EXPOSE 80 8443
# Thu, 05 Sep 2024 00:10:23 GMT
CMD []
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea184e408ee8a3bda0cdce477eb9806a10f7582bd36e0d18c1a36e645d4a8524`  
		Last Modified: Thu, 05 Sep 2024 00:17:59 GMT  
		Size: 46.6 MB (46594565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce81c8f7a8af9c632886d9382a8489c48b529c3a16f50cd485b6cd0cc3a2a19`  
		Last Modified: Thu, 05 Sep 2024 00:17:53 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.13`

```console
$ docker pull varnish@sha256:bfd6cf3bc107200b6feac23071cce59ce28e910805e58f97b67280721e062c0c
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
$ docker pull varnish@sha256:672b71e5883cefd983bab2dbf3634f2cc5ee0ef341bfb33050446e5dfd4f8595
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95867078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6057c46accf738b2d68e68f5803b049689957714857a4e3270b7965b2ee098c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:56:53 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 27 Sep 2024 07:56:53 GMT
ARG VARNISH_VERSION=6.0.13
# Fri, 27 Sep 2024 07:56:54 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Fri, 27 Sep 2024 07:56:54 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:58:40 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Fri, 27 Sep 2024 07:58:40 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:58:40 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:58:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:58:40 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:58:40 GMT
CMD []
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b6651c40c47f71c9486af005d55471e17d8a90aa852ed051a7e4ba1a3348ed`  
		Last Modified: Fri, 27 Sep 2024 07:59:56 GMT  
		Size: 64.4 MB (64437764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c046b9fb8849d1f1d68eedb3fc15fdb5469610f06a54ba908d173d8e396feb1`  
		Last Modified: Fri, 27 Sep 2024 07:59:48 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c0e75a091223dc30da50c78da9b32dfb6ebf8a61a7fde62ac08d72c8b9e4f86e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72864140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc154e7c6bb5593ea4e110cdf1869c0059bf606d05dbeb397be19e9f36296758`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 05:14:05 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
# Fri, 27 Sep 2024 05:14:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:26:26 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 27 Sep 2024 07:26:27 GMT
ARG VARNISH_VERSION=6.0.13
# Fri, 27 Sep 2024 07:26:27 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Fri, 27 Sep 2024 07:26:27 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:28:28 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Fri, 27 Sep 2024 07:28:28 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:28:28 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:28:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:28:29 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:28:29 GMT
CMD []
```

-	Layers:
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7d4933da79ac1087836dc24bfb8ba8ae3e80cede005988a89d4e7d8feaf874`  
		Last Modified: Fri, 27 Sep 2024 07:29:38 GMT  
		Size: 46.3 MB (46274112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e705e915ccaa6302ee24bc00b349bdb9403be35b7a813145cbaeda347828b49a`  
		Last Modified: Fri, 27 Sep 2024 07:29:32 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f5f81da76f5e69e98006b3733a4f9082952033d459558e9fa56c8ed915c752db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89961577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d6730b0996d43d67c19836bd61d7fbebe76ff38bb1fafb246e2ea97e9e695c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:32:04 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 27 Sep 2024 07:32:04 GMT
ARG VARNISH_VERSION=6.0.13
# Fri, 27 Sep 2024 07:32:04 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Fri, 27 Sep 2024 07:32:04 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:33:35 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Fri, 27 Sep 2024 07:33:36 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:33:36 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:33:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:33:36 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:33:36 GMT
CMD []
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c11049a7bb44f1c287f63d0c337404483102a7055f33124aea5fe489ca9589`  
		Last Modified: Fri, 27 Sep 2024 07:34:46 GMT  
		Size: 59.9 MB (59885703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b81c9012312de01b188f659e443f50952e138bac1371b03dc84558f10849b7`  
		Last Modified: Fri, 27 Sep 2024 07:34:39 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; 386

```console
$ docker pull varnish@sha256:173b1de36a4d17ea1799e1bb74537b5f2fcb43312e8cbfa78dfe515479d8ab66
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97132611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4177ce3a56a71e449c2a875605082cf5ccb475126d7ebbf33fd937f9ac9e6abc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 07:23:23 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
# Fri, 27 Sep 2024 07:23:24 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:54:25 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 27 Sep 2024 07:54:25 GMT
ARG VARNISH_VERSION=6.0.13
# Fri, 27 Sep 2024 07:54:26 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Fri, 27 Sep 2024 07:54:26 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:56:46 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Fri, 27 Sep 2024 07:56:46 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:56:46 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:56:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:56:47 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:56:47 GMT
CMD []
```

-	Layers:
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de14ddae1aa0ebd1b4b6f365a428f18241ed79c7eca15ad87985885fea17625c`  
		Last Modified: Fri, 27 Sep 2024 07:58:29 GMT  
		Size: 64.7 MB (64718399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389ed122f33c9b42cd54aa8e4e994ff51e0787b7e1daa8a74d1393654a944fa0`  
		Last Modified: Fri, 27 Sep 2024 07:58:17 GMT  
		Size: 713.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; ppc64le

```console
$ docker pull varnish@sha256:053579a9edb1c0ecd98f26ada06d72fcfeb69ed1e49940c05e60e25ff5f25371
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94647026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fd07f2ef42ca87942053c400a4785380dce3bb54e606fb1d63097a8cfe068f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 04 Sep 2024 22:26:18 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Wed, 04 Sep 2024 22:26:20 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:27:32 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Wed, 04 Sep 2024 23:27:33 GMT
ARG VARNISH_VERSION=6.0.13
# Wed, 04 Sep 2024 23:27:34 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Wed, 04 Sep 2024 23:27:34 GMT
ENV VARNISH_SIZE=100M
# Wed, 04 Sep 2024 23:30:49 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 04 Sep 2024 23:30:51 GMT
WORKDIR /etc/varnish
# Wed, 04 Sep 2024 23:30:52 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Wed, 04 Sep 2024 23:30:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 04 Sep 2024 23:30:52 GMT
EXPOSE 80 8443
# Wed, 04 Sep 2024 23:30:53 GMT
CMD []
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ad53399901533b0371d62560f54aaa95448a92fa2cc0e637b23440ebec222b`  
		Last Modified: Wed, 04 Sep 2024 23:44:07 GMT  
		Size: 59.3 MB (59347035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4eb9dcfc226e07bc3c4fa4ab30656eda5ab65803c658f6082bccdd1e5edfac`  
		Last Modified: Wed, 04 Sep 2024 23:43:57 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:6.0.13` - linux; s390x

```console
$ docker pull varnish@sha256:32841bc0f7503dfd6c456ad94c8f78007b3100045965cadbe18f456099ac8abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76258728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded5fdd03ff15a069138878b85906a9196b3fc3ba8c26fafc22d244e44a35304`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 04 Sep 2024 21:43:26 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Wed, 04 Sep 2024 21:43:27 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:09:00 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Thu, 05 Sep 2024 00:09:00 GMT
ARG VARNISH_VERSION=6.0.13
# Thu, 05 Sep 2024 00:09:01 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Thu, 05 Sep 2024 00:09:01 GMT
ENV VARNISH_SIZE=100M
# Thu, 05 Sep 2024 00:10:22 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 05 Sep 2024 00:10:23 GMT
WORKDIR /etc/varnish
# Thu, 05 Sep 2024 00:10:23 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Thu, 05 Sep 2024 00:10:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 05 Sep 2024 00:10:23 GMT
EXPOSE 80 8443
# Thu, 05 Sep 2024 00:10:23 GMT
CMD []
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea184e408ee8a3bda0cdce477eb9806a10f7582bd36e0d18c1a36e645d4a8524`  
		Last Modified: Thu, 05 Sep 2024 00:17:59 GMT  
		Size: 46.6 MB (46594565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce81c8f7a8af9c632886d9382a8489c48b529c3a16f50cd485b6cd0cc3a2a19`  
		Last Modified: Thu, 05 Sep 2024 00:17:53 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7`

```console
$ docker pull varnish@sha256:8e7ba64d6a432b97fb4efb1f3c120eaf911ed1c1235b18c864da6ca7406e9eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7` - linux; amd64

```console
$ docker pull varnish@sha256:a71cc6138225f2c8ba371927b994d4b5b2a6a437da8c6f81304742aa55dda57a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134982695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da37273f07e7bd9db9bb7acf5407271f4ccde6c61ccf590606567146dd885a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:51:16 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:51:16 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:51:16 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:51:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:51:17 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:51:17 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:53:55 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:53:55 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:53:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:53:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:53:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:53:56 GMT
USER varnish
# Fri, 27 Sep 2024 07:53:56 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:53:56 GMT
CMD []
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e2ce7afa100adb46c4acd2bef025c6577d68309b7153939833a5dda1b2a41b`  
		Last Modified: Fri, 27 Sep 2024 07:59:11 GMT  
		Size: 105.9 MB (105854407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea900cdc6f004e86ef8f4598a43dfb4e3c5862053f08217ae4830988bfcc3d2`  
		Last Modified: Fri, 27 Sep 2024 07:58:57 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e148ca457c952ede82841502cd9a8e3c09ddfdeb54657568fb5ae4f68b66cc1`  
		Last Modified: Fri, 27 Sep 2024 07:58:57 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5d8fe47f340d1e44020396650466bca61c29308cceb5f3dff5bf801952d10602
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105217189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0d15f054bdacd8b3c0f3733600948c003090d4aab5c967936625bf8be1864c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:20:10 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:20:10 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:20:11 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:20:11 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:23:14 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:23:15 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:23:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:23:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:23:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:23:16 GMT
USER varnish
# Fri, 27 Sep 2024 07:23:16 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:23:16 GMT
CMD []
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249c0ac843e40f12a2d525b9f3588886ab80624823564d77bae9fae28efdb2cb`  
		Last Modified: Fri, 27 Sep 2024 07:28:57 GMT  
		Size: 80.5 MB (80497030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e386ba271d5aaa8a17c7e57c779d2e1cba144fa9f086db55531c646ee89c6c`  
		Last Modified: Fri, 27 Sep 2024 07:28:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27dd9b2764bda28a7a10c33b6f50bbdf0d449f88f4345b712f716db4d88e370`  
		Last Modified: Fri, 27 Sep 2024 07:28:46 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:d42b3f4d2ac6e535a81651d29a299b117bdea7ed501a719a057938012f0b1d98
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129473676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf723ffc2300d885c7c66bd502fddf9c6e5d550b2af9e5b3a50fcbfa6202dfd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:27:00 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:27:00 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:27:01 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:27:01 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:29:23 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:29:24 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:29:24 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:29:25 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:29:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:29:25 GMT
USER varnish
# Fri, 27 Sep 2024 07:29:25 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:29:25 GMT
CMD []
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87e627a5d1611ff2d926a726f860cdcb063db55917cb3d67bcf3158f4654231`  
		Last Modified: Fri, 27 Sep 2024 07:34:04 GMT  
		Size: 100.3 MB (100315298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a171ed1f7c6532b689162145429fd4b0a586055a9c5064c19c8c4f56491223f`  
		Last Modified: Fri, 27 Sep 2024 07:33:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cf47690e5def09375fd3669ff3e10ee60d1e6d2a2004922f6902da80882891`  
		Last Modified: Fri, 27 Sep 2024 07:33:53 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7` - linux; 386

```console
$ docker pull varnish@sha256:5eb9001f3912d1f7729a7abb79dc3868203c11bb88043ddbc2bff44dcf470b0f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132117398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3db10a2b743e999aa53ac989a7ec3a42e3c366ecbddfb4cd9859934a1f83fe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:46:51 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:46:51 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:46:52 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:46:52 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:50:27 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:50:29 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:50:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:50:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:50:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:50:29 GMT
USER varnish
# Fri, 27 Sep 2024 07:50:29 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:50:30 GMT
CMD []
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d7b3e36bdc8fcd710d5baa19bb03c0f9dfe8095f7ef92d0cd277770bb19892`  
		Last Modified: Fri, 27 Sep 2024 07:57:33 GMT  
		Size: 102.0 MB (101971168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6701de376e37e68d6582481d3b7f9385834d64242b2859270dc372347f47fa`  
		Last Modified: Fri, 27 Sep 2024 07:57:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86034acb950f872f20bce5e55d03c73a7ad387133b563f1f491d31cd9b324d03`  
		Last Modified: Fri, 27 Sep 2024 07:57:13 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7` - linux; ppc64le

```console
$ docker pull varnish@sha256:80ad420fb59b56e2d5be3a6ccf99314f2cd3dbff2b6d81a37b49cba3c0251168
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137921174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86941e432a392b77ff8595ced407099ae34752c235d5a41b2a245770d7d1d42f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:21:04 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:21:04 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:21:05 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:21:05 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:21:05 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:21:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:24:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:24:51 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:24:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:24:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:24:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:24:52 GMT
USER varnish
# Thu, 17 Oct 2024 03:24:52 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:24:52 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84d4766d611be78854d8bfad7378b9072ecbe3ade1457862137470ce22557a`  
		Last Modified: Thu, 17 Oct 2024 03:29:28 GMT  
		Size: 104.8 MB (104796961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826c5b5ed72493c005e765ea9fe73a61c14e57cb1ca901e9caafd0a4010793c9`  
		Last Modified: Thu, 17 Oct 2024 03:29:10 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f551de2aa30e84f97b1573542aa0647fcecd2da21329b0ce70cb86cffcdd2de`  
		Last Modified: Thu, 17 Oct 2024 03:29:10 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7` - linux; s390x

```console
$ docker pull varnish@sha256:a6ec5d891316fa5d9a7de24ce870da964ef4c2fa4ee44b395f7d67170fde681d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112580334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236aaceab22f4762ec0de9bbfcef5865a636024ce50e501f67041974f02a6dc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:52:07 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:52:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:52:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:54:39 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:54:42 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:54:42 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:54:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:54:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:54:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:54:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:54:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40600a7c357ca6c02d49abca4f445d2a67e0f817e8924a4bbc3dbc0ab1c07a8c`  
		Last Modified: Thu, 17 Oct 2024 03:58:35 GMT  
		Size: 85.1 MB (85088239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9308896b060d89adc522b31775c270cc70aed098d14753b9f0d1d1adf9b33b`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715abd33b2fc67e17eeb2b082afb3c4d1233b5432aac4c5f07735d030f32a7cc`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7-alpine`

```console
$ docker pull varnish@sha256:062c4ab1b637b9e9a5d9250ce8508ee167cc45f370f4d2d1f1d1b7991ce845c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:a3574e3b2bd944073722b876c29cf09702b6375036db42f908e4650bf23dbd0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73337749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bacdaeae6793680cab791ebe1361728b7eb083a1facf2a497f7a1ea4cf18d4f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:23:25 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:23:25 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:23:25 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:23:25 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:23:26 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:24:40 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:24:40 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:24:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:24:40 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:24:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:24:41 GMT
USER varnish
# Tue, 17 Sep 2024 21:24:41 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:24:41 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e644d68d0bbf715e3aaf103a5de4694aabfd642ca037acec5cd9747bbd9db1e`  
		Last Modified: Tue, 17 Sep 2024 21:25:45 GMT  
		Size: 69.9 MB (69916017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce8bff1fbb90cba56a245cd68096d687f98a03b64a2b1b2681cb21b58ad0035`  
		Last Modified: Tue, 17 Sep 2024 21:25:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6388e5f21c3b90a3870f1d6f8d66c507911dd575681cde25bc1a04550effb8`  
		Last Modified: Tue, 17 Sep 2024 21:25:37 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:354deab8a503dc8e31a8850bef8b20fa344a9b0a15d14933ae7b5094d4a8c4ec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57533950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a17a406fb78972e5809fdbe52daa99b4e69883753a1179b956a1132227c941`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 22:00:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 22:00:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 22:00:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 22:02:14 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 22:02:14 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 22:02:14 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 22:02:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 22:02:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 22:02:14 GMT
USER varnish
# Tue, 17 Sep 2024 22:02:14 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 22:02:15 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8813ea3938ff81df50007e31b76067340c1758667bdfd7179d32551ad0bcfa2d`  
		Last Modified: Tue, 17 Sep 2024 22:03:10 GMT  
		Size: 54.6 MB (54604264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b05417369d263b7c8d8b315666096d9bab56febfc2a86595bd211969ebe18ad`  
		Last Modified: Tue, 17 Sep 2024 22:03:04 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ba7ded2285f89b8b64eb163a5f0ed74aaeec188161b3bf7fd0aaccae6788a1`  
		Last Modified: Tue, 17 Sep 2024 22:03:04 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfe1aee4c184e7663ae040322c0c31b35cd0b8d728f3865de30a67122a3b6f0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70044444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21780c1110170fc966cb4748ff00e2f7a188c43db1b48811bfecc073ecb4c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:43:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:43:49 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:43:49 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:43:49 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:43:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:43:49 GMT
USER varnish
# Tue, 17 Sep 2024 21:43:49 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:43:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28ba5a4402255fdab74468444d26ba5a450bb3bf85308c8bfa037ff0d2e4481`  
		Last Modified: Tue, 17 Sep 2024 21:44:39 GMT  
		Size: 66.7 MB (66683314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c872d5a9b252a340d0656fdcf4b6e90d931d11f137f0b44b4444ff273873a2`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2c1c538a2d3a1c5c004361f6a4b125a2483e3a3dc1816c7ea8775f6c7c7f9`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:3da50e3f81938d063b7849dd4d8f83dc09552bc13b68a0788b2bdaeb5e8966be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75354425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30579799344622ba130f6df5e174e986f75c31937b2056a74c7c6fb36422fccb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:44:36 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:44:37 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:44:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:44:37 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:44:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:44:37 GMT
USER varnish
# Tue, 17 Sep 2024 21:44:37 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:44:37 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cf3a67921019e12988f9ad85476068512edd6a81f7f1f8ff550e83621a3d5b`  
		Last Modified: Tue, 17 Sep 2024 21:45:52 GMT  
		Size: 72.1 MB (72098793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084453347407e41595c52dccc0c96066e579395b163b8855f44de0467535b488`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f056ae9a1c7699ea5fdc01d3dc561774699e1aa2129eb8e22bbd0390ccb475`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b33c3bf2263e07743fc34db1e1fd476bca5279d0e472948dcb4caa483dd3e079
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70852146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf71f4aa39c3d3f9cc25e091e2c80279768b5bd3188357306804ada74fe4555`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:21:40 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:21:41 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:21:41 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:21:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:21:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:21:44 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:21:44 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:21:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:21:45 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:23:09 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:23:11 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:23:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:23:12 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:23:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:23:13 GMT
USER varnish
# Tue, 17 Sep 2024 21:23:13 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:23:13 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08064ec4ae5f41f092978faf6983b834979aee5a429e973da86446bcdcfc102a`  
		Last Modified: Tue, 17 Sep 2024 21:24:27 GMT  
		Size: 67.5 MB (67485653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b5dc4a106ffaa87b00a0f8fe0dd74ee249a01a15d621662d178fe13c079e71`  
		Last Modified: Tue, 17 Sep 2024 21:24:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e905a8c021e2e7c34ba3ca625b2f1f36542c7334dfb60820e908c40d94b5678`  
		Last Modified: Tue, 17 Sep 2024 21:24:16 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:db93041e4e4775e3d4159fa1b5b7c65545a3c0dbdc12de978cded0fc36515740
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65242016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af743e848584bd94e6cf9c19729927521a094bfc5207e0be3a21a8aef0830a4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:46:31 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:46:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:46:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:47:54 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:47:56 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:47:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:47:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:47:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:47:57 GMT
USER varnish
# Tue, 17 Sep 2024 21:47:57 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:47:57 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6d1365d833d5e91a3423b89a361a19152c440c149cd7d12c26e57e64b3069`  
		Last Modified: Tue, 17 Sep 2024 21:49:17 GMT  
		Size: 62.0 MB (61986636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75daf6d5dfbb1c97cf59aa4a63c806056b36c721839e21899802891464a067a6`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85307912e9b6db6d28beb66a825b1bbaaafe821d0bc5b7156ff36f607b7b94c2`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5`

```console
$ docker pull varnish@sha256:6d19633286d18b65c951f0a6d9502585f8a571e76793972be397863dc12cae49
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
$ docker pull varnish@sha256:11453f7b435794761ad123289f68f13370b0e8f89a4bb3ba69ac3bf5c75e143a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134863533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aee31c556044c78e0318034656db8ed1fcfbc6f9ea30938ca8b1b26e0dbda34`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:54:12 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 27 Sep 2024 07:54:12 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 27 Sep 2024 07:54:12 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 27 Sep 2024 07:54:12 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 27 Sep 2024 07:54:12 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 27 Sep 2024 07:54:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 27 Sep 2024 07:54:13 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 27 Sep 2024 07:54:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 27 Sep 2024 07:54:13 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:54:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:54:13 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:56:44 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:56:45 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:56:45 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:56:45 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:56:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:56:45 GMT
USER varnish
# Fri, 27 Sep 2024 07:56:45 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:56:45 GMT
CMD []
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02a4e7c021f6492d9c50acb1c2f4f452e153374cfd1e6af5c5505d5d6988c53`  
		Last Modified: Fri, 27 Sep 2024 07:59:38 GMT  
		Size: 105.7 MB (105735245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19e64bf76c53681a32ce126ba90e08e913ca9bf5ec55b5cb8c2e33e951a4186`  
		Last Modified: Fri, 27 Sep 2024 07:59:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4ca367263950790d54ff31a9c62fc9d4afa281d7aa62662a0ead97e4fd4b0f`  
		Last Modified: Fri, 27 Sep 2024 07:59:24 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a956b30e5790720816bd60aecd9f624a288de8f0b240396b6265555be223691f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105118345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f611b80cb071073c0af049ffebf1e69145dcac306b44a17d879a8d96406bba60`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:23:32 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 27 Sep 2024 07:23:32 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 27 Sep 2024 07:23:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:23:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:23:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:26:12 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:26:13 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:26:14 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:26:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:26:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:26:14 GMT
USER varnish
# Fri, 27 Sep 2024 07:26:14 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:26:14 GMT
CMD []
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997f1e272111508113a00d5375b210295e4f7ffc5540ba58877e2f84ea1fa05f`  
		Last Modified: Fri, 27 Sep 2024 07:29:22 GMT  
		Size: 80.4 MB (80398188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3184f278cd4c69faaef01f839fd9d45a09ff0e4dc90f10f1d518b31666dfbe5`  
		Last Modified: Fri, 27 Sep 2024 07:29:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36719d9cb8521abf6cec05d65249ca84d1ba590fea19238a6ce546061e6ba388`  
		Last Modified: Fri, 27 Sep 2024 07:29:10 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:fdec206ee6f9a0b3ab4f073474ca2f66c008afbd16909d4c09c091f7e6ddbee2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129343816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0465fb994d6a0f03c44728072de7276389b58b0c63cae0748e0d28504256e464`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:29:40 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 27 Sep 2024 07:29:40 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 27 Sep 2024 07:29:40 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:29:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:29:40 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:31:51 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:31:53 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:31:53 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:31:53 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:31:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:31:53 GMT
USER varnish
# Fri, 27 Sep 2024 07:31:53 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:31:53 GMT
CMD []
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4e9f24eccb113f41ee75df838c443bf4f4b20a16d03f89cb3f993781bbd294`  
		Last Modified: Fri, 27 Sep 2024 07:34:29 GMT  
		Size: 100.2 MB (100185439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1890beea66eda00eba833c026dc74a50c86c0abf0b85b7b28a05301e2890717`  
		Last Modified: Fri, 27 Sep 2024 07:34:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd464ee94b50fed23a996381ae7b0ddd14eb6363e51c7b70bcb59183ac13e24`  
		Last Modified: Fri, 27 Sep 2024 07:34:18 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; 386

```console
$ docker pull varnish@sha256:90c2ce9f591d2345b6e9d96b2c99e91543e4c3941ca67a2ac8db491266cd0633
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132016871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24721978345a739069bc49d0ffd58faf7873c26fbc5b923cfeecfc5f20f5cc61`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:50:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 27 Sep 2024 07:50:46 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 27 Sep 2024 07:50:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:50:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:50:47 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:54:08 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:54:10 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:54:10 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:54:10 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:54:10 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:54:10 GMT
USER varnish
# Fri, 27 Sep 2024 07:54:11 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:54:11 GMT
CMD []
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a237cbfcdd9567204336e4c4dccaed9ed3876d0420b7e0f2ea642a142175a0`  
		Last Modified: Fri, 27 Sep 2024 07:58:07 GMT  
		Size: 101.9 MB (101870642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2176053ccdf02a07e6016241368fd1c8b6b762549bb78a9571e56845c13a3c5`  
		Last Modified: Fri, 27 Sep 2024 07:57:47 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d19b56512f6b50ddd6f596875309ba1ac75d6a2a83932f928a96ebdddc0aec`  
		Last Modified: Fri, 27 Sep 2024 07:57:47 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; ppc64le

```console
$ docker pull varnish@sha256:9da2339b7c4f5fbc3df9e284868c821c81d77f309b54db2bbc764e534516ca4d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137797884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc79a1b5a152d76ce01bae93f78e6d7ae09ac0a63dbb45ac5ce6d4eb9c825a5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:25:01 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 03:25:02 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 03:25:03 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 03:25:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 03:25:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:25:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:25:03 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:28:37 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:28:40 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:28:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:28:41 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:28:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:28:41 GMT
USER varnish
# Thu, 17 Oct 2024 03:28:41 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:28:42 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991d76c211cf2a830615bad768d92d195caf1d6e2619b51c8eb761e653788f31`  
		Last Modified: Thu, 17 Oct 2024 03:29:58 GMT  
		Size: 104.7 MB (104673673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0aca5c509ba6f97231d47b9babaa090d823353b46b4a935003063b5ba0c3ea`  
		Last Modified: Thu, 17 Oct 2024 03:29:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9936b87d11cac7008368bb672920d65fc0b57fa32deee7ea18bc08d46e3ca0`  
		Last Modified: Thu, 17 Oct 2024 03:29:41 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5` - linux; s390x

```console
$ docker pull varnish@sha256:3b34914b870a2edcd4dd9a97188bbb81856632bab5c2a8995edde96f1cc02223
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112468709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507d02e4180de236b10a91c68373d0cc6e694c2846cd995591b7b9fb14990a5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:55:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 03:55:11 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 03:55:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 03:55:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:55:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:55:12 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:57:38 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:57:41 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:57:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:57:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:57:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:57:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:57:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:57:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd94e8d5ab3de910e95edb78fdde0ea66df13e7ad9bf916690b28bafe248b6d`  
		Last Modified: Thu, 17 Oct 2024 03:58:58 GMT  
		Size: 85.0 MB (84976615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d9b29663f7a9f46b498ff8d0ec7cc98b7dbbc8fc084607283f531c314bd3ec`  
		Last Modified: Thu, 17 Oct 2024 03:58:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de3b12e1922df954d52eb1e54ca2ac9a195a03b65fc0169437b9deebc0ce263`  
		Last Modified: Thu, 17 Oct 2024 03:58:45 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5-alpine`

```console
$ docker pull varnish@sha256:d92362a83ce30bfd76c14777917466e76ce02e5ae154d08097435d28aed181be
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
$ docker pull varnish@sha256:59c3a09fc5abfcf1e68bd38d438688b7d0c83569e0a65c816969f83c90c13273
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73215829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f0db10e5790bfe29bd8386463af42eb77b410cb236646e6cd7360a0a9cd1d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:46:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 02:46:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 02:46:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 02:46:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 02:46:48 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:48:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:48:01 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:48:01 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:48:01 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:48:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:48:01 GMT
USER varnish
# Sat, 07 Sep 2024 02:48:02 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:48:02 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d285cdda36ba02e39fb5db5899ec835cee363b7ad2b87db63f3466c8e3527e`  
		Last Modified: Sat, 07 Sep 2024 02:53:41 GMT  
		Size: 69.8 MB (69794098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c3d3db1cd5550aceec91aca8a9a5acc85970f5d33b92957a32cb32b8653f63`  
		Last Modified: Sat, 07 Sep 2024 02:53:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babcaa75a49952cbb065a2d7ac35803afdabcc27c20e4167bee80ebe34d7d2b4`  
		Last Modified: Sat, 07 Sep 2024 02:53:33 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7fa07b0786b863dc266f351943439c8aafe5c3f1b93a8ac717ba1b00c802e9c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57421050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e86e2caef22106bf8ecd12f84c635b831a9666146b0dd59490107dad72d475a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:53:17 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 06 Sep 2024 23:53:17 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 06 Sep 2024 23:53:18 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 06 Sep 2024 23:53:18 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 06 Sep 2024 23:53:18 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 06 Sep 2024 23:53:18 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 06 Sep 2024 23:53:18 GMT
ENV VARNISH_SIZE=100M
# Fri, 06 Sep 2024 23:54:36 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 06 Sep 2024 23:54:37 GMT
WORKDIR /etc/varnish
# Fri, 06 Sep 2024 23:54:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:54:38 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 06 Sep 2024 23:54:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 06 Sep 2024 23:54:38 GMT
USER varnish
# Fri, 06 Sep 2024 23:54:38 GMT
EXPOSE 80 8443
# Fri, 06 Sep 2024 23:54:38 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41154e939d991f21ae1b190b52d812049226a428aa6bed870d4e144e9496d9c7`  
		Last Modified: Sat, 07 Sep 2024 00:00:34 GMT  
		Size: 54.5 MB (54491364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6660d44e064182554dc06b729533de25fcc0f86a3b8274bc4f1f15100ea84`  
		Last Modified: Sat, 07 Sep 2024 00:00:28 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf5f2ac481a3f8c6a07650a539c5e858231e5eff291d331151f75229b0d6216`  
		Last Modified: Sat, 07 Sep 2024 00:00:28 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a6ea3915acfc6f2cff98f8e6397b051c2f1486e0b1abffc2a9b5f4b6fcf44726
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69922870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6fa80545d0146358c54e3b460875cbe64c34292c8ec0e2a5ee4d89825e37d8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:32:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 02:32:42 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 02:32:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 02:32:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 02:32:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 02:32:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 02:32:43 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:33:48 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:33:48 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:33:48 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:33:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:33:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:33:48 GMT
USER varnish
# Sat, 07 Sep 2024 02:33:49 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:33:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7c041f1a08d6904c5fc431550f1b46f386b1e8a0a15f60420d3f1c3f8e4956`  
		Last Modified: Sat, 07 Sep 2024 02:38:29 GMT  
		Size: 66.6 MB (66561743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13493d62ebb9230283c31f2c29616815b7261d8ea5ce1fef5cee06eca895d48a`  
		Last Modified: Sat, 07 Sep 2024 02:38:23 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b528f8eb0911d23806e92337fc161ee9f7ffd889a3fc47faac4df88c1ff84d`  
		Last Modified: Sat, 07 Sep 2024 02:38:23 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; 386

```console
$ docker pull varnish@sha256:055811aff351b9a4185b26939c7b779ba64ef187e21b5c1ab3ebfae72c5dd2b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75241120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b353d90e6191bdd87206bdce7c566b1a283c71ab91f523afb89549543eb7c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:57:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 01:57:46 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 01:57:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 01:57:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 01:57:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 01:57:47 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 01:59:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 01:59:50 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 01:59:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 01:59:51 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 01:59:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 01:59:51 GMT
USER varnish
# Sat, 07 Sep 2024 01:59:51 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 01:59:51 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60754c4db0c99b69e16cf7a780fe7598d9436a865cac09ee645434b131389f24`  
		Last Modified: Sat, 07 Sep 2024 02:06:53 GMT  
		Size: 72.0 MB (71985490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f0f44ea3af290ddd37e769969c21b165b3cefc3b2b6b6f2987ffe285c643c3`  
		Last Modified: Sat, 07 Sep 2024 02:06:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ecb4e83c13f39bf24e6f0249ae24efc4a9b03f78fb80807592920214edf0d3`  
		Last Modified: Sat, 07 Sep 2024 02:06:41 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:aa76e10acc20b1fb7084f61677fc684cfed97b7af8517311b64343a792ef2ce4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70745749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288e480738fe2b36328c2abf2943fa9a47d7ca87a45ccd079f4024dc985cad78`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:59:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 01:59:43 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 01:59:43 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 01:59:43 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 01:59:44 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 01:59:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 01:59:45 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 01:59:45 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 01:59:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 01:59:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 01:59:46 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:01:10 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:01:13 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:01:13 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:01:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:01:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:01:14 GMT
USER varnish
# Sat, 07 Sep 2024 02:01:15 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:01:15 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3498df33b2a1081026de1cfb84850fe2c222aab212e52e98eab4ff6476b50b3b`  
		Last Modified: Sat, 07 Sep 2024 02:06:57 GMT  
		Size: 67.4 MB (67379260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff4a12d0055dfaf864b93acd92e976c57dd6f419497e874f975fb708b18d9f2`  
		Last Modified: Sat, 07 Sep 2024 02:06:47 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a34c42ae7729aeb3a5fdb84562bf98b976005e144797c0774ee4dde3c9ba29`  
		Last Modified: Sat, 07 Sep 2024 02:06:47 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ebc3c7d1e6ec9e99118c774dbc40e74cbee9596bcd758b9ef0d883e5b8221676
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65126002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd6b7c87f2e0740249182cd21889878ccfc7e1ebcd9b00a210f3f696b98373a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:10:28 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 06 Sep 2024 23:10:29 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 06 Sep 2024 23:10:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 06 Sep 2024 23:10:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 06 Sep 2024 23:10:29 GMT
ENV VARNISH_SIZE=100M
# Fri, 06 Sep 2024 23:11:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 06 Sep 2024 23:11:51 GMT
WORKDIR /etc/varnish
# Fri, 06 Sep 2024 23:11:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:11:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 06 Sep 2024 23:11:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 06 Sep 2024 23:11:52 GMT
USER varnish
# Fri, 06 Sep 2024 23:11:52 GMT
EXPOSE 80 8443
# Fri, 06 Sep 2024 23:11:52 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118bc1dbba5c82d06fdfed695d8e80e8044a23b2970f2be0b57056e8cf88c48`  
		Last Modified: Fri, 06 Sep 2024 23:17:56 GMT  
		Size: 61.9 MB (61870619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d03fb424bdb1471e62681e8eceff4cd027a748ea17df08c21c4e3e4fb13763`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72312bc2baecd766ef19ab42b9999881f9ac906a0aa00b1897913ade4e9af474`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5.0`

```console
$ docker pull varnish@sha256:6d19633286d18b65c951f0a6d9502585f8a571e76793972be397863dc12cae49
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
$ docker pull varnish@sha256:11453f7b435794761ad123289f68f13370b0e8f89a4bb3ba69ac3bf5c75e143a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134863533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aee31c556044c78e0318034656db8ed1fcfbc6f9ea30938ca8b1b26e0dbda34`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:54:12 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 27 Sep 2024 07:54:12 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 27 Sep 2024 07:54:12 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 27 Sep 2024 07:54:12 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 27 Sep 2024 07:54:12 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 27 Sep 2024 07:54:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 27 Sep 2024 07:54:13 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 27 Sep 2024 07:54:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 27 Sep 2024 07:54:13 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:54:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:54:13 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:56:44 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:56:45 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:56:45 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:56:45 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:56:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:56:45 GMT
USER varnish
# Fri, 27 Sep 2024 07:56:45 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:56:45 GMT
CMD []
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02a4e7c021f6492d9c50acb1c2f4f452e153374cfd1e6af5c5505d5d6988c53`  
		Last Modified: Fri, 27 Sep 2024 07:59:38 GMT  
		Size: 105.7 MB (105735245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19e64bf76c53681a32ce126ba90e08e913ca9bf5ec55b5cb8c2e33e951a4186`  
		Last Modified: Fri, 27 Sep 2024 07:59:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4ca367263950790d54ff31a9c62fc9d4afa281d7aa62662a0ead97e4fd4b0f`  
		Last Modified: Fri, 27 Sep 2024 07:59:24 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a956b30e5790720816bd60aecd9f624a288de8f0b240396b6265555be223691f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105118345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f611b80cb071073c0af049ffebf1e69145dcac306b44a17d879a8d96406bba60`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:23:32 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 27 Sep 2024 07:23:32 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 27 Sep 2024 07:23:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:23:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:23:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:26:12 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:26:13 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:26:14 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:26:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:26:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:26:14 GMT
USER varnish
# Fri, 27 Sep 2024 07:26:14 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:26:14 GMT
CMD []
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997f1e272111508113a00d5375b210295e4f7ffc5540ba58877e2f84ea1fa05f`  
		Last Modified: Fri, 27 Sep 2024 07:29:22 GMT  
		Size: 80.4 MB (80398188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3184f278cd4c69faaef01f839fd9d45a09ff0e4dc90f10f1d518b31666dfbe5`  
		Last Modified: Fri, 27 Sep 2024 07:29:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36719d9cb8521abf6cec05d65249ca84d1ba590fea19238a6ce546061e6ba388`  
		Last Modified: Fri, 27 Sep 2024 07:29:10 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:fdec206ee6f9a0b3ab4f073474ca2f66c008afbd16909d4c09c091f7e6ddbee2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129343816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0465fb994d6a0f03c44728072de7276389b58b0c63cae0748e0d28504256e464`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:29:40 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 27 Sep 2024 07:29:40 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 27 Sep 2024 07:29:40 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:29:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:29:40 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:31:51 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:31:53 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:31:53 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:31:53 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:31:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:31:53 GMT
USER varnish
# Fri, 27 Sep 2024 07:31:53 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:31:53 GMT
CMD []
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4e9f24eccb113f41ee75df838c443bf4f4b20a16d03f89cb3f993781bbd294`  
		Last Modified: Fri, 27 Sep 2024 07:34:29 GMT  
		Size: 100.2 MB (100185439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1890beea66eda00eba833c026dc74a50c86c0abf0b85b7b28a05301e2890717`  
		Last Modified: Fri, 27 Sep 2024 07:34:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd464ee94b50fed23a996381ae7b0ddd14eb6363e51c7b70bcb59183ac13e24`  
		Last Modified: Fri, 27 Sep 2024 07:34:18 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; 386

```console
$ docker pull varnish@sha256:90c2ce9f591d2345b6e9d96b2c99e91543e4c3941ca67a2ac8db491266cd0633
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132016871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24721978345a739069bc49d0ffd58faf7873c26fbc5b923cfeecfc5f20f5cc61`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:50:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 27 Sep 2024 07:50:46 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 27 Sep 2024 07:50:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:50:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:50:47 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:54:08 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:54:10 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:54:10 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:54:10 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:54:10 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:54:10 GMT
USER varnish
# Fri, 27 Sep 2024 07:54:11 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:54:11 GMT
CMD []
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a237cbfcdd9567204336e4c4dccaed9ed3876d0420b7e0f2ea642a142175a0`  
		Last Modified: Fri, 27 Sep 2024 07:58:07 GMT  
		Size: 101.9 MB (101870642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2176053ccdf02a07e6016241368fd1c8b6b762549bb78a9571e56845c13a3c5`  
		Last Modified: Fri, 27 Sep 2024 07:57:47 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d19b56512f6b50ddd6f596875309ba1ac75d6a2a83932f928a96ebdddc0aec`  
		Last Modified: Fri, 27 Sep 2024 07:57:47 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:9da2339b7c4f5fbc3df9e284868c821c81d77f309b54db2bbc764e534516ca4d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137797884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc79a1b5a152d76ce01bae93f78e6d7ae09ac0a63dbb45ac5ce6d4eb9c825a5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:25:01 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 03:25:02 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 03:25:03 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 03:25:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 03:25:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:25:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:25:03 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:28:37 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:28:40 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:28:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:28:41 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:28:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:28:41 GMT
USER varnish
# Thu, 17 Oct 2024 03:28:41 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:28:42 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991d76c211cf2a830615bad768d92d195caf1d6e2619b51c8eb761e653788f31`  
		Last Modified: Thu, 17 Oct 2024 03:29:58 GMT  
		Size: 104.7 MB (104673673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0aca5c509ba6f97231d47b9babaa090d823353b46b4a935003063b5ba0c3ea`  
		Last Modified: Thu, 17 Oct 2024 03:29:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9936b87d11cac7008368bb672920d65fc0b57fa32deee7ea18bc08d46e3ca0`  
		Last Modified: Thu, 17 Oct 2024 03:29:41 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0` - linux; s390x

```console
$ docker pull varnish@sha256:3b34914b870a2edcd4dd9a97188bbb81856632bab5c2a8995edde96f1cc02223
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112468709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507d02e4180de236b10a91c68373d0cc6e694c2846cd995591b7b9fb14990a5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:55:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 03:55:11 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 03:55:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 03:55:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:55:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:55:12 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:57:38 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:57:41 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:57:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:57:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:57:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:57:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:57:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:57:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd94e8d5ab3de910e95edb78fdde0ea66df13e7ad9bf916690b28bafe248b6d`  
		Last Modified: Thu, 17 Oct 2024 03:58:58 GMT  
		Size: 85.0 MB (84976615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d9b29663f7a9f46b498ff8d0ec7cc98b7dbbc8fc084607283f531c314bd3ec`  
		Last Modified: Thu, 17 Oct 2024 03:58:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de3b12e1922df954d52eb1e54ca2ac9a195a03b65fc0169437b9deebc0ce263`  
		Last Modified: Thu, 17 Oct 2024 03:58:45 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.5.0-alpine`

```console
$ docker pull varnish@sha256:d92362a83ce30bfd76c14777917466e76ce02e5ae154d08097435d28aed181be
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
$ docker pull varnish@sha256:59c3a09fc5abfcf1e68bd38d438688b7d0c83569e0a65c816969f83c90c13273
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73215829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f0db10e5790bfe29bd8386463af42eb77b410cb236646e6cd7360a0a9cd1d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:46:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 02:46:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 02:46:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 02:46:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 02:46:48 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:48:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:48:01 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:48:01 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:48:01 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:48:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:48:01 GMT
USER varnish
# Sat, 07 Sep 2024 02:48:02 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:48:02 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d285cdda36ba02e39fb5db5899ec835cee363b7ad2b87db63f3466c8e3527e`  
		Last Modified: Sat, 07 Sep 2024 02:53:41 GMT  
		Size: 69.8 MB (69794098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c3d3db1cd5550aceec91aca8a9a5acc85970f5d33b92957a32cb32b8653f63`  
		Last Modified: Sat, 07 Sep 2024 02:53:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babcaa75a49952cbb065a2d7ac35803afdabcc27c20e4167bee80ebe34d7d2b4`  
		Last Modified: Sat, 07 Sep 2024 02:53:33 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7fa07b0786b863dc266f351943439c8aafe5c3f1b93a8ac717ba1b00c802e9c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57421050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e86e2caef22106bf8ecd12f84c635b831a9666146b0dd59490107dad72d475a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:53:17 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 06 Sep 2024 23:53:17 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 06 Sep 2024 23:53:18 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 06 Sep 2024 23:53:18 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 06 Sep 2024 23:53:18 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 06 Sep 2024 23:53:18 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 06 Sep 2024 23:53:18 GMT
ENV VARNISH_SIZE=100M
# Fri, 06 Sep 2024 23:54:36 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 06 Sep 2024 23:54:37 GMT
WORKDIR /etc/varnish
# Fri, 06 Sep 2024 23:54:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:54:38 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 06 Sep 2024 23:54:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 06 Sep 2024 23:54:38 GMT
USER varnish
# Fri, 06 Sep 2024 23:54:38 GMT
EXPOSE 80 8443
# Fri, 06 Sep 2024 23:54:38 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41154e939d991f21ae1b190b52d812049226a428aa6bed870d4e144e9496d9c7`  
		Last Modified: Sat, 07 Sep 2024 00:00:34 GMT  
		Size: 54.5 MB (54491364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6660d44e064182554dc06b729533de25fcc0f86a3b8274bc4f1f15100ea84`  
		Last Modified: Sat, 07 Sep 2024 00:00:28 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf5f2ac481a3f8c6a07650a539c5e858231e5eff291d331151f75229b0d6216`  
		Last Modified: Sat, 07 Sep 2024 00:00:28 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a6ea3915acfc6f2cff98f8e6397b051c2f1486e0b1abffc2a9b5f4b6fcf44726
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69922870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6fa80545d0146358c54e3b460875cbe64c34292c8ec0e2a5ee4d89825e37d8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:32:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 02:32:42 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 02:32:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 02:32:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 02:32:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 02:32:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 02:32:43 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:33:48 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:33:48 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:33:48 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:33:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:33:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:33:48 GMT
USER varnish
# Sat, 07 Sep 2024 02:33:49 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:33:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7c041f1a08d6904c5fc431550f1b46f386b1e8a0a15f60420d3f1c3f8e4956`  
		Last Modified: Sat, 07 Sep 2024 02:38:29 GMT  
		Size: 66.6 MB (66561743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13493d62ebb9230283c31f2c29616815b7261d8ea5ce1fef5cee06eca895d48a`  
		Last Modified: Sat, 07 Sep 2024 02:38:23 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b528f8eb0911d23806e92337fc161ee9f7ffd889a3fc47faac4df88c1ff84d`  
		Last Modified: Sat, 07 Sep 2024 02:38:23 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:055811aff351b9a4185b26939c7b779ba64ef187e21b5c1ab3ebfae72c5dd2b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75241120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b353d90e6191bdd87206bdce7c566b1a283c71ab91f523afb89549543eb7c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:57:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 01:57:46 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 01:57:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 01:57:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 01:57:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 01:57:47 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 01:59:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 01:59:50 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 01:59:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 01:59:51 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 01:59:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 01:59:51 GMT
USER varnish
# Sat, 07 Sep 2024 01:59:51 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 01:59:51 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60754c4db0c99b69e16cf7a780fe7598d9436a865cac09ee645434b131389f24`  
		Last Modified: Sat, 07 Sep 2024 02:06:53 GMT  
		Size: 72.0 MB (71985490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f0f44ea3af290ddd37e769969c21b165b3cefc3b2b6b6f2987ffe285c643c3`  
		Last Modified: Sat, 07 Sep 2024 02:06:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ecb4e83c13f39bf24e6f0249ae24efc4a9b03f78fb80807592920214edf0d3`  
		Last Modified: Sat, 07 Sep 2024 02:06:41 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:aa76e10acc20b1fb7084f61677fc684cfed97b7af8517311b64343a792ef2ce4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70745749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288e480738fe2b36328c2abf2943fa9a47d7ca87a45ccd079f4024dc985cad78`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:59:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 01:59:43 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 01:59:43 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 01:59:43 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 01:59:44 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 01:59:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 01:59:45 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 01:59:45 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 01:59:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 01:59:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 01:59:46 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:01:10 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:01:13 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:01:13 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:01:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:01:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:01:14 GMT
USER varnish
# Sat, 07 Sep 2024 02:01:15 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:01:15 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3498df33b2a1081026de1cfb84850fe2c222aab212e52e98eab4ff6476b50b3b`  
		Last Modified: Sat, 07 Sep 2024 02:06:57 GMT  
		Size: 67.4 MB (67379260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff4a12d0055dfaf864b93acd92e976c57dd6f419497e874f975fb708b18d9f2`  
		Last Modified: Sat, 07 Sep 2024 02:06:47 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a34c42ae7729aeb3a5fdb84562bf98b976005e144797c0774ee4dde3c9ba29`  
		Last Modified: Sat, 07 Sep 2024 02:06:47 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.5.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ebc3c7d1e6ec9e99118c774dbc40e74cbee9596bcd758b9ef0d883e5b8221676
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65126002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd6b7c87f2e0740249182cd21889878ccfc7e1ebcd9b00a210f3f696b98373a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:10:28 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 06 Sep 2024 23:10:29 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 06 Sep 2024 23:10:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 06 Sep 2024 23:10:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 06 Sep 2024 23:10:29 GMT
ENV VARNISH_SIZE=100M
# Fri, 06 Sep 2024 23:11:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 06 Sep 2024 23:11:51 GMT
WORKDIR /etc/varnish
# Fri, 06 Sep 2024 23:11:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:11:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 06 Sep 2024 23:11:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 06 Sep 2024 23:11:52 GMT
USER varnish
# Fri, 06 Sep 2024 23:11:52 GMT
EXPOSE 80 8443
# Fri, 06 Sep 2024 23:11:52 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118bc1dbba5c82d06fdfed695d8e80e8044a23b2970f2be0b57056e8cf88c48`  
		Last Modified: Fri, 06 Sep 2024 23:17:56 GMT  
		Size: 61.9 MB (61870619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d03fb424bdb1471e62681e8eceff4cd027a748ea17df08c21c4e3e4fb13763`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72312bc2baecd766ef19ab42b9999881f9ac906a0aa00b1897913ade4e9af474`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.6`

```console
$ docker pull varnish@sha256:8e7ba64d6a432b97fb4efb1f3c120eaf911ed1c1235b18c864da6ca7406e9eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.6` - linux; amd64

```console
$ docker pull varnish@sha256:a71cc6138225f2c8ba371927b994d4b5b2a6a437da8c6f81304742aa55dda57a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134982695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da37273f07e7bd9db9bb7acf5407271f4ccde6c61ccf590606567146dd885a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:51:16 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:51:16 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:51:16 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:51:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:51:17 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:51:17 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:53:55 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:53:55 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:53:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:53:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:53:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:53:56 GMT
USER varnish
# Fri, 27 Sep 2024 07:53:56 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:53:56 GMT
CMD []
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e2ce7afa100adb46c4acd2bef025c6577d68309b7153939833a5dda1b2a41b`  
		Last Modified: Fri, 27 Sep 2024 07:59:11 GMT  
		Size: 105.9 MB (105854407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea900cdc6f004e86ef8f4598a43dfb4e3c5862053f08217ae4830988bfcc3d2`  
		Last Modified: Fri, 27 Sep 2024 07:58:57 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e148ca457c952ede82841502cd9a8e3c09ddfdeb54657568fb5ae4f68b66cc1`  
		Last Modified: Fri, 27 Sep 2024 07:58:57 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5d8fe47f340d1e44020396650466bca61c29308cceb5f3dff5bf801952d10602
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105217189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0d15f054bdacd8b3c0f3733600948c003090d4aab5c967936625bf8be1864c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:20:10 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:20:10 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:20:11 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:20:11 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:23:14 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:23:15 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:23:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:23:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:23:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:23:16 GMT
USER varnish
# Fri, 27 Sep 2024 07:23:16 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:23:16 GMT
CMD []
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249c0ac843e40f12a2d525b9f3588886ab80624823564d77bae9fae28efdb2cb`  
		Last Modified: Fri, 27 Sep 2024 07:28:57 GMT  
		Size: 80.5 MB (80497030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e386ba271d5aaa8a17c7e57c779d2e1cba144fa9f086db55531c646ee89c6c`  
		Last Modified: Fri, 27 Sep 2024 07:28:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27dd9b2764bda28a7a10c33b6f50bbdf0d449f88f4345b712f716db4d88e370`  
		Last Modified: Fri, 27 Sep 2024 07:28:46 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:d42b3f4d2ac6e535a81651d29a299b117bdea7ed501a719a057938012f0b1d98
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129473676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf723ffc2300d885c7c66bd502fddf9c6e5d550b2af9e5b3a50fcbfa6202dfd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:27:00 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:27:00 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:27:01 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:27:01 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:29:23 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:29:24 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:29:24 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:29:25 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:29:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:29:25 GMT
USER varnish
# Fri, 27 Sep 2024 07:29:25 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:29:25 GMT
CMD []
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87e627a5d1611ff2d926a726f860cdcb063db55917cb3d67bcf3158f4654231`  
		Last Modified: Fri, 27 Sep 2024 07:34:04 GMT  
		Size: 100.3 MB (100315298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a171ed1f7c6532b689162145429fd4b0a586055a9c5064c19c8c4f56491223f`  
		Last Modified: Fri, 27 Sep 2024 07:33:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cf47690e5def09375fd3669ff3e10ee60d1e6d2a2004922f6902da80882891`  
		Last Modified: Fri, 27 Sep 2024 07:33:53 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6` - linux; 386

```console
$ docker pull varnish@sha256:5eb9001f3912d1f7729a7abb79dc3868203c11bb88043ddbc2bff44dcf470b0f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132117398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3db10a2b743e999aa53ac989a7ec3a42e3c366ecbddfb4cd9859934a1f83fe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:46:51 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:46:51 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:46:52 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:46:52 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:50:27 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:50:29 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:50:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:50:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:50:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:50:29 GMT
USER varnish
# Fri, 27 Sep 2024 07:50:29 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:50:30 GMT
CMD []
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d7b3e36bdc8fcd710d5baa19bb03c0f9dfe8095f7ef92d0cd277770bb19892`  
		Last Modified: Fri, 27 Sep 2024 07:57:33 GMT  
		Size: 102.0 MB (101971168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6701de376e37e68d6582481d3b7f9385834d64242b2859270dc372347f47fa`  
		Last Modified: Fri, 27 Sep 2024 07:57:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86034acb950f872f20bce5e55d03c73a7ad387133b563f1f491d31cd9b324d03`  
		Last Modified: Fri, 27 Sep 2024 07:57:13 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6` - linux; ppc64le

```console
$ docker pull varnish@sha256:80ad420fb59b56e2d5be3a6ccf99314f2cd3dbff2b6d81a37b49cba3c0251168
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137921174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86941e432a392b77ff8595ced407099ae34752c235d5a41b2a245770d7d1d42f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:21:04 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:21:04 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:21:05 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:21:05 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:21:05 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:21:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:24:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:24:51 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:24:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:24:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:24:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:24:52 GMT
USER varnish
# Thu, 17 Oct 2024 03:24:52 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:24:52 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84d4766d611be78854d8bfad7378b9072ecbe3ade1457862137470ce22557a`  
		Last Modified: Thu, 17 Oct 2024 03:29:28 GMT  
		Size: 104.8 MB (104796961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826c5b5ed72493c005e765ea9fe73a61c14e57cb1ca901e9caafd0a4010793c9`  
		Last Modified: Thu, 17 Oct 2024 03:29:10 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f551de2aa30e84f97b1573542aa0647fcecd2da21329b0ce70cb86cffcdd2de`  
		Last Modified: Thu, 17 Oct 2024 03:29:10 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6` - linux; s390x

```console
$ docker pull varnish@sha256:a6ec5d891316fa5d9a7de24ce870da964ef4c2fa4ee44b395f7d67170fde681d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112580334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236aaceab22f4762ec0de9bbfcef5865a636024ce50e501f67041974f02a6dc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:52:07 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:52:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:52:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:54:39 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:54:42 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:54:42 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:54:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:54:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:54:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:54:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:54:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40600a7c357ca6c02d49abca4f445d2a67e0f817e8924a4bbc3dbc0ab1c07a8c`  
		Last Modified: Thu, 17 Oct 2024 03:58:35 GMT  
		Size: 85.1 MB (85088239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9308896b060d89adc522b31775c270cc70aed098d14753b9f0d1d1adf9b33b`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715abd33b2fc67e17eeb2b082afb3c4d1233b5432aac4c5f07735d030f32a7cc`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.6-alpine`

```console
$ docker pull varnish@sha256:062c4ab1b637b9e9a5d9250ce8508ee167cc45f370f4d2d1f1d1b7991ce845c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.6-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:a3574e3b2bd944073722b876c29cf09702b6375036db42f908e4650bf23dbd0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73337749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bacdaeae6793680cab791ebe1361728b7eb083a1facf2a497f7a1ea4cf18d4f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:23:25 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:23:25 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:23:25 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:23:25 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:23:26 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:24:40 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:24:40 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:24:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:24:40 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:24:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:24:41 GMT
USER varnish
# Tue, 17 Sep 2024 21:24:41 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:24:41 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e644d68d0bbf715e3aaf103a5de4694aabfd642ca037acec5cd9747bbd9db1e`  
		Last Modified: Tue, 17 Sep 2024 21:25:45 GMT  
		Size: 69.9 MB (69916017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce8bff1fbb90cba56a245cd68096d687f98a03b64a2b1b2681cb21b58ad0035`  
		Last Modified: Tue, 17 Sep 2024 21:25:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6388e5f21c3b90a3870f1d6f8d66c507911dd575681cde25bc1a04550effb8`  
		Last Modified: Tue, 17 Sep 2024 21:25:37 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:354deab8a503dc8e31a8850bef8b20fa344a9b0a15d14933ae7b5094d4a8c4ec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57533950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a17a406fb78972e5809fdbe52daa99b4e69883753a1179b956a1132227c941`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 22:00:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 22:00:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 22:00:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 22:02:14 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 22:02:14 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 22:02:14 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 22:02:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 22:02:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 22:02:14 GMT
USER varnish
# Tue, 17 Sep 2024 22:02:14 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 22:02:15 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8813ea3938ff81df50007e31b76067340c1758667bdfd7179d32551ad0bcfa2d`  
		Last Modified: Tue, 17 Sep 2024 22:03:10 GMT  
		Size: 54.6 MB (54604264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b05417369d263b7c8d8b315666096d9bab56febfc2a86595bd211969ebe18ad`  
		Last Modified: Tue, 17 Sep 2024 22:03:04 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ba7ded2285f89b8b64eb163a5f0ed74aaeec188161b3bf7fd0aaccae6788a1`  
		Last Modified: Tue, 17 Sep 2024 22:03:04 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfe1aee4c184e7663ae040322c0c31b35cd0b8d728f3865de30a67122a3b6f0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70044444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21780c1110170fc966cb4748ff00e2f7a188c43db1b48811bfecc073ecb4c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:43:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:43:49 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:43:49 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:43:49 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:43:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:43:49 GMT
USER varnish
# Tue, 17 Sep 2024 21:43:49 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:43:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28ba5a4402255fdab74468444d26ba5a450bb3bf85308c8bfa037ff0d2e4481`  
		Last Modified: Tue, 17 Sep 2024 21:44:39 GMT  
		Size: 66.7 MB (66683314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c872d5a9b252a340d0656fdcf4b6e90d931d11f137f0b44b4444ff273873a2`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2c1c538a2d3a1c5c004361f6a4b125a2483e3a3dc1816c7ea8775f6c7c7f9`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6-alpine` - linux; 386

```console
$ docker pull varnish@sha256:3da50e3f81938d063b7849dd4d8f83dc09552bc13b68a0788b2bdaeb5e8966be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75354425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30579799344622ba130f6df5e174e986f75c31937b2056a74c7c6fb36422fccb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:44:36 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:44:37 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:44:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:44:37 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:44:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:44:37 GMT
USER varnish
# Tue, 17 Sep 2024 21:44:37 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:44:37 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cf3a67921019e12988f9ad85476068512edd6a81f7f1f8ff550e83621a3d5b`  
		Last Modified: Tue, 17 Sep 2024 21:45:52 GMT  
		Size: 72.1 MB (72098793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084453347407e41595c52dccc0c96066e579395b163b8855f44de0467535b488`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f056ae9a1c7699ea5fdc01d3dc561774699e1aa2129eb8e22bbd0390ccb475`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b33c3bf2263e07743fc34db1e1fd476bca5279d0e472948dcb4caa483dd3e079
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70852146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf71f4aa39c3d3f9cc25e091e2c80279768b5bd3188357306804ada74fe4555`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:21:40 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:21:41 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:21:41 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:21:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:21:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:21:44 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:21:44 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:21:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:21:45 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:23:09 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:23:11 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:23:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:23:12 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:23:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:23:13 GMT
USER varnish
# Tue, 17 Sep 2024 21:23:13 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:23:13 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08064ec4ae5f41f092978faf6983b834979aee5a429e973da86446bcdcfc102a`  
		Last Modified: Tue, 17 Sep 2024 21:24:27 GMT  
		Size: 67.5 MB (67485653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b5dc4a106ffaa87b00a0f8fe0dd74ee249a01a15d621662d178fe13c079e71`  
		Last Modified: Tue, 17 Sep 2024 21:24:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e905a8c021e2e7c34ba3ca625b2f1f36542c7334dfb60820e908c40d94b5678`  
		Last Modified: Tue, 17 Sep 2024 21:24:16 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:db93041e4e4775e3d4159fa1b5b7c65545a3c0dbdc12de978cded0fc36515740
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65242016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af743e848584bd94e6cf9c19729927521a094bfc5207e0be3a21a8aef0830a4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:46:31 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:46:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:46:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:47:54 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:47:56 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:47:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:47:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:47:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:47:57 GMT
USER varnish
# Tue, 17 Sep 2024 21:47:57 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:47:57 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6d1365d833d5e91a3423b89a361a19152c440c149cd7d12c26e57e64b3069`  
		Last Modified: Tue, 17 Sep 2024 21:49:17 GMT  
		Size: 62.0 MB (61986636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75daf6d5dfbb1c97cf59aa4a63c806056b36c721839e21899802891464a067a6`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85307912e9b6db6d28beb66a825b1bbaaafe821d0bc5b7156ff36f607b7b94c2`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.6.0`

```console
$ docker pull varnish@sha256:8e7ba64d6a432b97fb4efb1f3c120eaf911ed1c1235b18c864da6ca7406e9eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.6.0` - linux; amd64

```console
$ docker pull varnish@sha256:a71cc6138225f2c8ba371927b994d4b5b2a6a437da8c6f81304742aa55dda57a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134982695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da37273f07e7bd9db9bb7acf5407271f4ccde6c61ccf590606567146dd885a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:51:16 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:51:16 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:51:16 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:51:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:51:17 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:51:17 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:53:55 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:53:55 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:53:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:53:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:53:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:53:56 GMT
USER varnish
# Fri, 27 Sep 2024 07:53:56 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:53:56 GMT
CMD []
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e2ce7afa100adb46c4acd2bef025c6577d68309b7153939833a5dda1b2a41b`  
		Last Modified: Fri, 27 Sep 2024 07:59:11 GMT  
		Size: 105.9 MB (105854407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea900cdc6f004e86ef8f4598a43dfb4e3c5862053f08217ae4830988bfcc3d2`  
		Last Modified: Fri, 27 Sep 2024 07:58:57 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e148ca457c952ede82841502cd9a8e3c09ddfdeb54657568fb5ae4f68b66cc1`  
		Last Modified: Fri, 27 Sep 2024 07:58:57 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.0` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5d8fe47f340d1e44020396650466bca61c29308cceb5f3dff5bf801952d10602
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105217189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0d15f054bdacd8b3c0f3733600948c003090d4aab5c967936625bf8be1864c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:20:10 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:20:10 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:20:11 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:20:11 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:23:14 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:23:15 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:23:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:23:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:23:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:23:16 GMT
USER varnish
# Fri, 27 Sep 2024 07:23:16 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:23:16 GMT
CMD []
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249c0ac843e40f12a2d525b9f3588886ab80624823564d77bae9fae28efdb2cb`  
		Last Modified: Fri, 27 Sep 2024 07:28:57 GMT  
		Size: 80.5 MB (80497030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e386ba271d5aaa8a17c7e57c779d2e1cba144fa9f086db55531c646ee89c6c`  
		Last Modified: Fri, 27 Sep 2024 07:28:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27dd9b2764bda28a7a10c33b6f50bbdf0d449f88f4345b712f716db4d88e370`  
		Last Modified: Fri, 27 Sep 2024 07:28:46 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:d42b3f4d2ac6e535a81651d29a299b117bdea7ed501a719a057938012f0b1d98
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129473676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf723ffc2300d885c7c66bd502fddf9c6e5d550b2af9e5b3a50fcbfa6202dfd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:27:00 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:27:00 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:27:01 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:27:01 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:29:23 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:29:24 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:29:24 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:29:25 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:29:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:29:25 GMT
USER varnish
# Fri, 27 Sep 2024 07:29:25 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:29:25 GMT
CMD []
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87e627a5d1611ff2d926a726f860cdcb063db55917cb3d67bcf3158f4654231`  
		Last Modified: Fri, 27 Sep 2024 07:34:04 GMT  
		Size: 100.3 MB (100315298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a171ed1f7c6532b689162145429fd4b0a586055a9c5064c19c8c4f56491223f`  
		Last Modified: Fri, 27 Sep 2024 07:33:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cf47690e5def09375fd3669ff3e10ee60d1e6d2a2004922f6902da80882891`  
		Last Modified: Fri, 27 Sep 2024 07:33:53 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.0` - linux; 386

```console
$ docker pull varnish@sha256:5eb9001f3912d1f7729a7abb79dc3868203c11bb88043ddbc2bff44dcf470b0f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132117398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3db10a2b743e999aa53ac989a7ec3a42e3c366ecbddfb4cd9859934a1f83fe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:46:51 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:46:51 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:46:52 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:46:52 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:50:27 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:50:29 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:50:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:50:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:50:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:50:29 GMT
USER varnish
# Fri, 27 Sep 2024 07:50:29 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:50:30 GMT
CMD []
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d7b3e36bdc8fcd710d5baa19bb03c0f9dfe8095f7ef92d0cd277770bb19892`  
		Last Modified: Fri, 27 Sep 2024 07:57:33 GMT  
		Size: 102.0 MB (101971168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6701de376e37e68d6582481d3b7f9385834d64242b2859270dc372347f47fa`  
		Last Modified: Fri, 27 Sep 2024 07:57:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86034acb950f872f20bce5e55d03c73a7ad387133b563f1f491d31cd9b324d03`  
		Last Modified: Fri, 27 Sep 2024 07:57:13 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.0` - linux; ppc64le

```console
$ docker pull varnish@sha256:80ad420fb59b56e2d5be3a6ccf99314f2cd3dbff2b6d81a37b49cba3c0251168
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137921174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86941e432a392b77ff8595ced407099ae34752c235d5a41b2a245770d7d1d42f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:21:04 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:21:04 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:21:05 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:21:05 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:21:05 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:21:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:24:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:24:51 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:24:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:24:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:24:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:24:52 GMT
USER varnish
# Thu, 17 Oct 2024 03:24:52 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:24:52 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84d4766d611be78854d8bfad7378b9072ecbe3ade1457862137470ce22557a`  
		Last Modified: Thu, 17 Oct 2024 03:29:28 GMT  
		Size: 104.8 MB (104796961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826c5b5ed72493c005e765ea9fe73a61c14e57cb1ca901e9caafd0a4010793c9`  
		Last Modified: Thu, 17 Oct 2024 03:29:10 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f551de2aa30e84f97b1573542aa0647fcecd2da21329b0ce70cb86cffcdd2de`  
		Last Modified: Thu, 17 Oct 2024 03:29:10 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.0` - linux; s390x

```console
$ docker pull varnish@sha256:a6ec5d891316fa5d9a7de24ce870da964ef4c2fa4ee44b395f7d67170fde681d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112580334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236aaceab22f4762ec0de9bbfcef5865a636024ce50e501f67041974f02a6dc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:52:07 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:52:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:52:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:54:39 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:54:42 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:54:42 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:54:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:54:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:54:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:54:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:54:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40600a7c357ca6c02d49abca4f445d2a67e0f817e8924a4bbc3dbc0ab1c07a8c`  
		Last Modified: Thu, 17 Oct 2024 03:58:35 GMT  
		Size: 85.1 MB (85088239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9308896b060d89adc522b31775c270cc70aed098d14753b9f0d1d1adf9b33b`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715abd33b2fc67e17eeb2b082afb3c4d1233b5432aac4c5f07735d030f32a7cc`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:7.6.0-alpine`

```console
$ docker pull varnish@sha256:062c4ab1b637b9e9a5d9250ce8508ee167cc45f370f4d2d1f1d1b7991ce845c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:7.6.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:a3574e3b2bd944073722b876c29cf09702b6375036db42f908e4650bf23dbd0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73337749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bacdaeae6793680cab791ebe1361728b7eb083a1facf2a497f7a1ea4cf18d4f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:23:25 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:23:25 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:23:25 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:23:25 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:23:26 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:24:40 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:24:40 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:24:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:24:40 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:24:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:24:41 GMT
USER varnish
# Tue, 17 Sep 2024 21:24:41 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:24:41 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e644d68d0bbf715e3aaf103a5de4694aabfd642ca037acec5cd9747bbd9db1e`  
		Last Modified: Tue, 17 Sep 2024 21:25:45 GMT  
		Size: 69.9 MB (69916017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce8bff1fbb90cba56a245cd68096d687f98a03b64a2b1b2681cb21b58ad0035`  
		Last Modified: Tue, 17 Sep 2024 21:25:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6388e5f21c3b90a3870f1d6f8d66c507911dd575681cde25bc1a04550effb8`  
		Last Modified: Tue, 17 Sep 2024 21:25:37 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.0-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:354deab8a503dc8e31a8850bef8b20fa344a9b0a15d14933ae7b5094d4a8c4ec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57533950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a17a406fb78972e5809fdbe52daa99b4e69883753a1179b956a1132227c941`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 22:00:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 22:00:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 22:00:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 22:02:14 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 22:02:14 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 22:02:14 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 22:02:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 22:02:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 22:02:14 GMT
USER varnish
# Tue, 17 Sep 2024 22:02:14 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 22:02:15 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8813ea3938ff81df50007e31b76067340c1758667bdfd7179d32551ad0bcfa2d`  
		Last Modified: Tue, 17 Sep 2024 22:03:10 GMT  
		Size: 54.6 MB (54604264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b05417369d263b7c8d8b315666096d9bab56febfc2a86595bd211969ebe18ad`  
		Last Modified: Tue, 17 Sep 2024 22:03:04 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ba7ded2285f89b8b64eb163a5f0ed74aaeec188161b3bf7fd0aaccae6788a1`  
		Last Modified: Tue, 17 Sep 2024 22:03:04 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfe1aee4c184e7663ae040322c0c31b35cd0b8d728f3865de30a67122a3b6f0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70044444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21780c1110170fc966cb4748ff00e2f7a188c43db1b48811bfecc073ecb4c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:43:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:43:49 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:43:49 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:43:49 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:43:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:43:49 GMT
USER varnish
# Tue, 17 Sep 2024 21:43:49 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:43:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28ba5a4402255fdab74468444d26ba5a450bb3bf85308c8bfa037ff0d2e4481`  
		Last Modified: Tue, 17 Sep 2024 21:44:39 GMT  
		Size: 66.7 MB (66683314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c872d5a9b252a340d0656fdcf4b6e90d931d11f137f0b44b4444ff273873a2`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2c1c538a2d3a1c5c004361f6a4b125a2483e3a3dc1816c7ea8775f6c7c7f9`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.0-alpine` - linux; 386

```console
$ docker pull varnish@sha256:3da50e3f81938d063b7849dd4d8f83dc09552bc13b68a0788b2bdaeb5e8966be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75354425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30579799344622ba130f6df5e174e986f75c31937b2056a74c7c6fb36422fccb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:44:36 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:44:37 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:44:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:44:37 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:44:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:44:37 GMT
USER varnish
# Tue, 17 Sep 2024 21:44:37 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:44:37 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cf3a67921019e12988f9ad85476068512edd6a81f7f1f8ff550e83621a3d5b`  
		Last Modified: Tue, 17 Sep 2024 21:45:52 GMT  
		Size: 72.1 MB (72098793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084453347407e41595c52dccc0c96066e579395b163b8855f44de0467535b488`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f056ae9a1c7699ea5fdc01d3dc561774699e1aa2129eb8e22bbd0390ccb475`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.0-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b33c3bf2263e07743fc34db1e1fd476bca5279d0e472948dcb4caa483dd3e079
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70852146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf71f4aa39c3d3f9cc25e091e2c80279768b5bd3188357306804ada74fe4555`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:21:40 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:21:41 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:21:41 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:21:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:21:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:21:44 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:21:44 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:21:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:21:45 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:23:09 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:23:11 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:23:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:23:12 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:23:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:23:13 GMT
USER varnish
# Tue, 17 Sep 2024 21:23:13 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:23:13 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08064ec4ae5f41f092978faf6983b834979aee5a429e973da86446bcdcfc102a`  
		Last Modified: Tue, 17 Sep 2024 21:24:27 GMT  
		Size: 67.5 MB (67485653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b5dc4a106ffaa87b00a0f8fe0dd74ee249a01a15d621662d178fe13c079e71`  
		Last Modified: Tue, 17 Sep 2024 21:24:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e905a8c021e2e7c34ba3ca625b2f1f36542c7334dfb60820e908c40d94b5678`  
		Last Modified: Tue, 17 Sep 2024 21:24:16 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:7.6.0-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:db93041e4e4775e3d4159fa1b5b7c65545a3c0dbdc12de978cded0fc36515740
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65242016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af743e848584bd94e6cf9c19729927521a094bfc5207e0be3a21a8aef0830a4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:46:31 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:46:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:46:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:47:54 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:47:56 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:47:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:47:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:47:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:47:57 GMT
USER varnish
# Tue, 17 Sep 2024 21:47:57 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:47:57 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6d1365d833d5e91a3423b89a361a19152c440c149cd7d12c26e57e64b3069`  
		Last Modified: Tue, 17 Sep 2024 21:49:17 GMT  
		Size: 62.0 MB (61986636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75daf6d5dfbb1c97cf59aa4a63c806056b36c721839e21899802891464a067a6`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85307912e9b6db6d28beb66a825b1bbaaafe821d0bc5b7156ff36f607b7b94c2`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:alpine`

```console
$ docker pull varnish@sha256:062c4ab1b637b9e9a5d9250ce8508ee167cc45f370f4d2d1f1d1b7991ce845c4
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
$ docker pull varnish@sha256:a3574e3b2bd944073722b876c29cf09702b6375036db42f908e4650bf23dbd0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73337749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bacdaeae6793680cab791ebe1361728b7eb083a1facf2a497f7a1ea4cf18d4f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:23:25 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:23:25 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:23:25 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:23:25 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:23:26 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:24:40 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:24:40 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:24:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:24:40 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:24:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:24:41 GMT
USER varnish
# Tue, 17 Sep 2024 21:24:41 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:24:41 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e644d68d0bbf715e3aaf103a5de4694aabfd642ca037acec5cd9747bbd9db1e`  
		Last Modified: Tue, 17 Sep 2024 21:25:45 GMT  
		Size: 69.9 MB (69916017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce8bff1fbb90cba56a245cd68096d687f98a03b64a2b1b2681cb21b58ad0035`  
		Last Modified: Tue, 17 Sep 2024 21:25:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6388e5f21c3b90a3870f1d6f8d66c507911dd575681cde25bc1a04550effb8`  
		Last Modified: Tue, 17 Sep 2024 21:25:37 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:354deab8a503dc8e31a8850bef8b20fa344a9b0a15d14933ae7b5094d4a8c4ec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57533950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a17a406fb78972e5809fdbe52daa99b4e69883753a1179b956a1132227c941`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 22:00:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 22:00:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 22:00:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 22:02:14 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 22:02:14 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 22:02:14 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 22:02:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 22:02:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 22:02:14 GMT
USER varnish
# Tue, 17 Sep 2024 22:02:14 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 22:02:15 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8813ea3938ff81df50007e31b76067340c1758667bdfd7179d32551ad0bcfa2d`  
		Last Modified: Tue, 17 Sep 2024 22:03:10 GMT  
		Size: 54.6 MB (54604264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b05417369d263b7c8d8b315666096d9bab56febfc2a86595bd211969ebe18ad`  
		Last Modified: Tue, 17 Sep 2024 22:03:04 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ba7ded2285f89b8b64eb163a5f0ed74aaeec188161b3bf7fd0aaccae6788a1`  
		Last Modified: Tue, 17 Sep 2024 22:03:04 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfe1aee4c184e7663ae040322c0c31b35cd0b8d728f3865de30a67122a3b6f0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70044444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21780c1110170fc966cb4748ff00e2f7a188c43db1b48811bfecc073ecb4c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:43:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:43:49 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:43:49 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:43:49 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:43:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:43:49 GMT
USER varnish
# Tue, 17 Sep 2024 21:43:49 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:43:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28ba5a4402255fdab74468444d26ba5a450bb3bf85308c8bfa037ff0d2e4481`  
		Last Modified: Tue, 17 Sep 2024 21:44:39 GMT  
		Size: 66.7 MB (66683314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c872d5a9b252a340d0656fdcf4b6e90d931d11f137f0b44b4444ff273873a2`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2c1c538a2d3a1c5c004361f6a4b125a2483e3a3dc1816c7ea8775f6c7c7f9`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:3da50e3f81938d063b7849dd4d8f83dc09552bc13b68a0788b2bdaeb5e8966be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75354425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30579799344622ba130f6df5e174e986f75c31937b2056a74c7c6fb36422fccb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:44:36 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:44:37 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:44:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:44:37 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:44:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:44:37 GMT
USER varnish
# Tue, 17 Sep 2024 21:44:37 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:44:37 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cf3a67921019e12988f9ad85476068512edd6a81f7f1f8ff550e83621a3d5b`  
		Last Modified: Tue, 17 Sep 2024 21:45:52 GMT  
		Size: 72.1 MB (72098793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084453347407e41595c52dccc0c96066e579395b163b8855f44de0467535b488`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f056ae9a1c7699ea5fdc01d3dc561774699e1aa2129eb8e22bbd0390ccb475`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b33c3bf2263e07743fc34db1e1fd476bca5279d0e472948dcb4caa483dd3e079
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70852146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf71f4aa39c3d3f9cc25e091e2c80279768b5bd3188357306804ada74fe4555`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:21:40 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:21:41 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:21:41 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:21:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:21:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:21:44 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:21:44 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:21:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:21:45 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:23:09 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:23:11 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:23:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:23:12 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:23:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:23:13 GMT
USER varnish
# Tue, 17 Sep 2024 21:23:13 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:23:13 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08064ec4ae5f41f092978faf6983b834979aee5a429e973da86446bcdcfc102a`  
		Last Modified: Tue, 17 Sep 2024 21:24:27 GMT  
		Size: 67.5 MB (67485653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b5dc4a106ffaa87b00a0f8fe0dd74ee249a01a15d621662d178fe13c079e71`  
		Last Modified: Tue, 17 Sep 2024 21:24:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e905a8c021e2e7c34ba3ca625b2f1f36542c7334dfb60820e908c40d94b5678`  
		Last Modified: Tue, 17 Sep 2024 21:24:16 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:db93041e4e4775e3d4159fa1b5b7c65545a3c0dbdc12de978cded0fc36515740
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65242016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af743e848584bd94e6cf9c19729927521a094bfc5207e0be3a21a8aef0830a4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:46:31 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:46:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:46:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:47:54 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:47:56 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:47:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:47:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:47:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:47:57 GMT
USER varnish
# Tue, 17 Sep 2024 21:47:57 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:47:57 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6d1365d833d5e91a3423b89a361a19152c440c149cd7d12c26e57e64b3069`  
		Last Modified: Tue, 17 Sep 2024 21:49:17 GMT  
		Size: 62.0 MB (61986636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75daf6d5dfbb1c97cf59aa4a63c806056b36c721839e21899802891464a067a6`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85307912e9b6db6d28beb66a825b1bbaaafe821d0bc5b7156ff36f607b7b94c2`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:8e7ba64d6a432b97fb4efb1f3c120eaf911ed1c1235b18c864da6ca7406e9eb1
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
$ docker pull varnish@sha256:a71cc6138225f2c8ba371927b994d4b5b2a6a437da8c6f81304742aa55dda57a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134982695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da37273f07e7bd9db9bb7acf5407271f4ccde6c61ccf590606567146dd885a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:51:16 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:51:16 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:51:16 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:51:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:51:17 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:51:17 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:53:55 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:53:55 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:53:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:53:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:53:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:53:56 GMT
USER varnish
# Fri, 27 Sep 2024 07:53:56 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:53:56 GMT
CMD []
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e2ce7afa100adb46c4acd2bef025c6577d68309b7153939833a5dda1b2a41b`  
		Last Modified: Fri, 27 Sep 2024 07:59:11 GMT  
		Size: 105.9 MB (105854407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea900cdc6f004e86ef8f4598a43dfb4e3c5862053f08217ae4830988bfcc3d2`  
		Last Modified: Fri, 27 Sep 2024 07:58:57 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e148ca457c952ede82841502cd9a8e3c09ddfdeb54657568fb5ae4f68b66cc1`  
		Last Modified: Fri, 27 Sep 2024 07:58:57 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5d8fe47f340d1e44020396650466bca61c29308cceb5f3dff5bf801952d10602
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105217189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0d15f054bdacd8b3c0f3733600948c003090d4aab5c967936625bf8be1864c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:20:10 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:20:10 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:20:11 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:20:11 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:23:14 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:23:15 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:23:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:23:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:23:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:23:16 GMT
USER varnish
# Fri, 27 Sep 2024 07:23:16 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:23:16 GMT
CMD []
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249c0ac843e40f12a2d525b9f3588886ab80624823564d77bae9fae28efdb2cb`  
		Last Modified: Fri, 27 Sep 2024 07:28:57 GMT  
		Size: 80.5 MB (80497030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e386ba271d5aaa8a17c7e57c779d2e1cba144fa9f086db55531c646ee89c6c`  
		Last Modified: Fri, 27 Sep 2024 07:28:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27dd9b2764bda28a7a10c33b6f50bbdf0d449f88f4345b712f716db4d88e370`  
		Last Modified: Fri, 27 Sep 2024 07:28:46 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:d42b3f4d2ac6e535a81651d29a299b117bdea7ed501a719a057938012f0b1d98
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129473676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf723ffc2300d885c7c66bd502fddf9c6e5d550b2af9e5b3a50fcbfa6202dfd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:27:00 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:27:00 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:27:01 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:27:01 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:29:23 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:29:24 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:29:24 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:29:25 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:29:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:29:25 GMT
USER varnish
# Fri, 27 Sep 2024 07:29:25 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:29:25 GMT
CMD []
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87e627a5d1611ff2d926a726f860cdcb063db55917cb3d67bcf3158f4654231`  
		Last Modified: Fri, 27 Sep 2024 07:34:04 GMT  
		Size: 100.3 MB (100315298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a171ed1f7c6532b689162145429fd4b0a586055a9c5064c19c8c4f56491223f`  
		Last Modified: Fri, 27 Sep 2024 07:33:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cf47690e5def09375fd3669ff3e10ee60d1e6d2a2004922f6902da80882891`  
		Last Modified: Fri, 27 Sep 2024 07:33:53 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:5eb9001f3912d1f7729a7abb79dc3868203c11bb88043ddbc2bff44dcf470b0f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132117398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3db10a2b743e999aa53ac989a7ec3a42e3c366ecbddfb4cd9859934a1f83fe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:46:51 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:46:51 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:46:52 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:46:52 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:50:27 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:50:29 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:50:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:50:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:50:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:50:29 GMT
USER varnish
# Fri, 27 Sep 2024 07:50:29 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:50:30 GMT
CMD []
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d7b3e36bdc8fcd710d5baa19bb03c0f9dfe8095f7ef92d0cd277770bb19892`  
		Last Modified: Fri, 27 Sep 2024 07:57:33 GMT  
		Size: 102.0 MB (101971168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6701de376e37e68d6582481d3b7f9385834d64242b2859270dc372347f47fa`  
		Last Modified: Fri, 27 Sep 2024 07:57:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86034acb950f872f20bce5e55d03c73a7ad387133b563f1f491d31cd9b324d03`  
		Last Modified: Fri, 27 Sep 2024 07:57:13 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:80ad420fb59b56e2d5be3a6ccf99314f2cd3dbff2b6d81a37b49cba3c0251168
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137921174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86941e432a392b77ff8595ced407099ae34752c235d5a41b2a245770d7d1d42f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:21:04 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:21:04 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:21:05 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:21:05 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:21:05 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:21:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:24:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:24:51 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:24:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:24:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:24:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:24:52 GMT
USER varnish
# Thu, 17 Oct 2024 03:24:52 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:24:52 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84d4766d611be78854d8bfad7378b9072ecbe3ade1457862137470ce22557a`  
		Last Modified: Thu, 17 Oct 2024 03:29:28 GMT  
		Size: 104.8 MB (104796961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826c5b5ed72493c005e765ea9fe73a61c14e57cb1ca901e9caafd0a4010793c9`  
		Last Modified: Thu, 17 Oct 2024 03:29:10 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f551de2aa30e84f97b1573542aa0647fcecd2da21329b0ce70cb86cffcdd2de`  
		Last Modified: Thu, 17 Oct 2024 03:29:10 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:a6ec5d891316fa5d9a7de24ce870da964ef4c2fa4ee44b395f7d67170fde681d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112580334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236aaceab22f4762ec0de9bbfcef5865a636024ce50e501f67041974f02a6dc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:52:07 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:52:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:52:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:54:39 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:54:42 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:54:42 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:54:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:54:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:54:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:54:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:54:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40600a7c357ca6c02d49abca4f445d2a67e0f817e8924a4bbc3dbc0ab1c07a8c`  
		Last Modified: Thu, 17 Oct 2024 03:58:35 GMT  
		Size: 85.1 MB (85088239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9308896b060d89adc522b31775c270cc70aed098d14753b9f0d1d1adf9b33b`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715abd33b2fc67e17eeb2b082afb3c4d1233b5432aac4c5f07735d030f32a7cc`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:062c4ab1b637b9e9a5d9250ce8508ee167cc45f370f4d2d1f1d1b7991ce845c4
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
$ docker pull varnish@sha256:a3574e3b2bd944073722b876c29cf09702b6375036db42f908e4650bf23dbd0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73337749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bacdaeae6793680cab791ebe1361728b7eb083a1facf2a497f7a1ea4cf18d4f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:23:25 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:23:25 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:23:25 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:23:25 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:23:26 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:24:40 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:24:40 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:24:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:24:40 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:24:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:24:41 GMT
USER varnish
# Tue, 17 Sep 2024 21:24:41 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:24:41 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e644d68d0bbf715e3aaf103a5de4694aabfd642ca037acec5cd9747bbd9db1e`  
		Last Modified: Tue, 17 Sep 2024 21:25:45 GMT  
		Size: 69.9 MB (69916017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce8bff1fbb90cba56a245cd68096d687f98a03b64a2b1b2681cb21b58ad0035`  
		Last Modified: Tue, 17 Sep 2024 21:25:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6388e5f21c3b90a3870f1d6f8d66c507911dd575681cde25bc1a04550effb8`  
		Last Modified: Tue, 17 Sep 2024 21:25:37 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:354deab8a503dc8e31a8850bef8b20fa344a9b0a15d14933ae7b5094d4a8c4ec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57533950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a17a406fb78972e5809fdbe52daa99b4e69883753a1179b956a1132227c941`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 22:00:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 22:00:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 22:00:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 22:02:14 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 22:02:14 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 22:02:14 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 22:02:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 22:02:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 22:02:14 GMT
USER varnish
# Tue, 17 Sep 2024 22:02:14 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 22:02:15 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8813ea3938ff81df50007e31b76067340c1758667bdfd7179d32551ad0bcfa2d`  
		Last Modified: Tue, 17 Sep 2024 22:03:10 GMT  
		Size: 54.6 MB (54604264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b05417369d263b7c8d8b315666096d9bab56febfc2a86595bd211969ebe18ad`  
		Last Modified: Tue, 17 Sep 2024 22:03:04 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ba7ded2285f89b8b64eb163a5f0ed74aaeec188161b3bf7fd0aaccae6788a1`  
		Last Modified: Tue, 17 Sep 2024 22:03:04 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfe1aee4c184e7663ae040322c0c31b35cd0b8d728f3865de30a67122a3b6f0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70044444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21780c1110170fc966cb4748ff00e2f7a188c43db1b48811bfecc073ecb4c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:43:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:43:49 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:43:49 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:43:49 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:43:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:43:49 GMT
USER varnish
# Tue, 17 Sep 2024 21:43:49 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:43:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28ba5a4402255fdab74468444d26ba5a450bb3bf85308c8bfa037ff0d2e4481`  
		Last Modified: Tue, 17 Sep 2024 21:44:39 GMT  
		Size: 66.7 MB (66683314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c872d5a9b252a340d0656fdcf4b6e90d931d11f137f0b44b4444ff273873a2`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2c1c538a2d3a1c5c004361f6a4b125a2483e3a3dc1816c7ea8775f6c7c7f9`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:3da50e3f81938d063b7849dd4d8f83dc09552bc13b68a0788b2bdaeb5e8966be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75354425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30579799344622ba130f6df5e174e986f75c31937b2056a74c7c6fb36422fccb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:44:36 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:44:37 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:44:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:44:37 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:44:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:44:37 GMT
USER varnish
# Tue, 17 Sep 2024 21:44:37 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:44:37 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cf3a67921019e12988f9ad85476068512edd6a81f7f1f8ff550e83621a3d5b`  
		Last Modified: Tue, 17 Sep 2024 21:45:52 GMT  
		Size: 72.1 MB (72098793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084453347407e41595c52dccc0c96066e579395b163b8855f44de0467535b488`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f056ae9a1c7699ea5fdc01d3dc561774699e1aa2129eb8e22bbd0390ccb475`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b33c3bf2263e07743fc34db1e1fd476bca5279d0e472948dcb4caa483dd3e079
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70852146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf71f4aa39c3d3f9cc25e091e2c80279768b5bd3188357306804ada74fe4555`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:21:40 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:21:41 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:21:41 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:21:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:21:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:21:44 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:21:44 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:21:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:21:45 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:23:09 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:23:11 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:23:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:23:12 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:23:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:23:13 GMT
USER varnish
# Tue, 17 Sep 2024 21:23:13 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:23:13 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08064ec4ae5f41f092978faf6983b834979aee5a429e973da86446bcdcfc102a`  
		Last Modified: Tue, 17 Sep 2024 21:24:27 GMT  
		Size: 67.5 MB (67485653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b5dc4a106ffaa87b00a0f8fe0dd74ee249a01a15d621662d178fe13c079e71`  
		Last Modified: Tue, 17 Sep 2024 21:24:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e905a8c021e2e7c34ba3ca625b2f1f36542c7334dfb60820e908c40d94b5678`  
		Last Modified: Tue, 17 Sep 2024 21:24:16 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:db93041e4e4775e3d4159fa1b5b7c65545a3c0dbdc12de978cded0fc36515740
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65242016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af743e848584bd94e6cf9c19729927521a094bfc5207e0be3a21a8aef0830a4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:46:31 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:46:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:46:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:47:54 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:47:56 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:47:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:47:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:47:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:47:57 GMT
USER varnish
# Tue, 17 Sep 2024 21:47:57 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:47:57 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6d1365d833d5e91a3423b89a361a19152c440c149cd7d12c26e57e64b3069`  
		Last Modified: Tue, 17 Sep 2024 21:49:17 GMT  
		Size: 62.0 MB (61986636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75daf6d5dfbb1c97cf59aa4a63c806056b36c721839e21899802891464a067a6`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85307912e9b6db6d28beb66a825b1bbaaafe821d0bc5b7156ff36f607b7b94c2`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:8e7ba64d6a432b97fb4efb1f3c120eaf911ed1c1235b18c864da6ca7406e9eb1
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
$ docker pull varnish@sha256:a71cc6138225f2c8ba371927b994d4b5b2a6a437da8c6f81304742aa55dda57a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134982695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da37273f07e7bd9db9bb7acf5407271f4ccde6c61ccf590606567146dd885a43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:51:16 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:51:16 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:51:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:51:16 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:51:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:51:17 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:51:17 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:53:55 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:53:55 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:53:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:53:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:53:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:53:56 GMT
USER varnish
# Fri, 27 Sep 2024 07:53:56 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:53:56 GMT
CMD []
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e2ce7afa100adb46c4acd2bef025c6577d68309b7153939833a5dda1b2a41b`  
		Last Modified: Fri, 27 Sep 2024 07:59:11 GMT  
		Size: 105.9 MB (105854407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea900cdc6f004e86ef8f4598a43dfb4e3c5862053f08217ae4830988bfcc3d2`  
		Last Modified: Fri, 27 Sep 2024 07:58:57 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e148ca457c952ede82841502cd9a8e3c09ddfdeb54657568fb5ae4f68b66cc1`  
		Last Modified: Fri, 27 Sep 2024 07:58:57 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5d8fe47f340d1e44020396650466bca61c29308cceb5f3dff5bf801952d10602
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105217189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0d15f054bdacd8b3c0f3733600948c003090d4aab5c967936625bf8be1864c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:20:10 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:20:10 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:20:10 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:20:11 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:20:11 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:20:11 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:23:14 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:23:15 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:23:15 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:23:15 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:23:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:23:16 GMT
USER varnish
# Fri, 27 Sep 2024 07:23:16 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:23:16 GMT
CMD []
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249c0ac843e40f12a2d525b9f3588886ab80624823564d77bae9fae28efdb2cb`  
		Last Modified: Fri, 27 Sep 2024 07:28:57 GMT  
		Size: 80.5 MB (80497030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e386ba271d5aaa8a17c7e57c779d2e1cba144fa9f086db55531c646ee89c6c`  
		Last Modified: Fri, 27 Sep 2024 07:28:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27dd9b2764bda28a7a10c33b6f50bbdf0d449f88f4345b712f716db4d88e370`  
		Last Modified: Fri, 27 Sep 2024 07:28:46 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:d42b3f4d2ac6e535a81651d29a299b117bdea7ed501a719a057938012f0b1d98
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129473676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf723ffc2300d885c7c66bd502fddf9c6e5d550b2af9e5b3a50fcbfa6202dfd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:27:00 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:27:00 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:27:00 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:27:01 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:27:01 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:27:01 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:29:23 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:29:24 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:29:24 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:29:25 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:29:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:29:25 GMT
USER varnish
# Fri, 27 Sep 2024 07:29:25 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:29:25 GMT
CMD []
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87e627a5d1611ff2d926a726f860cdcb063db55917cb3d67bcf3158f4654231`  
		Last Modified: Fri, 27 Sep 2024 07:34:04 GMT  
		Size: 100.3 MB (100315298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a171ed1f7c6532b689162145429fd4b0a586055a9c5064c19c8c4f56491223f`  
		Last Modified: Fri, 27 Sep 2024 07:33:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cf47690e5def09375fd3669ff3e10ee60d1e6d2a2004922f6902da80882891`  
		Last Modified: Fri, 27 Sep 2024 07:33:53 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:5eb9001f3912d1f7729a7abb79dc3868203c11bb88043ddbc2bff44dcf470b0f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132117398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3db10a2b743e999aa53ac989a7ec3a42e3c366ecbddfb4cd9859934a1f83fe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:46:51 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_VERSION=7.6.0
# Fri, 27 Sep 2024 07:46:51 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Fri, 27 Sep 2024 07:46:51 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Fri, 27 Sep 2024 07:46:52 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Fri, 27 Sep 2024 07:46:52 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:46:52 GMT
ENV VSM_NOPID=1
# Fri, 27 Sep 2024 07:50:27 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:50:29 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:50:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:50:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:50:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:50:29 GMT
USER varnish
# Fri, 27 Sep 2024 07:50:29 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:50:30 GMT
CMD []
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d7b3e36bdc8fcd710d5baa19bb03c0f9dfe8095f7ef92d0cd277770bb19892`  
		Last Modified: Fri, 27 Sep 2024 07:57:33 GMT  
		Size: 102.0 MB (101971168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6701de376e37e68d6582481d3b7f9385834d64242b2859270dc372347f47fa`  
		Last Modified: Fri, 27 Sep 2024 07:57:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86034acb950f872f20bce5e55d03c73a7ad387133b563f1f491d31cd9b324d03`  
		Last Modified: Fri, 27 Sep 2024 07:57:13 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:80ad420fb59b56e2d5be3a6ccf99314f2cd3dbff2b6d81a37b49cba3c0251168
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137921174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86941e432a392b77ff8595ced407099ae34752c235d5a41b2a245770d7d1d42f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:21:04 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:21:04 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:21:05 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:21:05 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:21:05 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:21:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:21:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:21:07 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:24:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:24:51 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:24:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:24:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:24:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:24:52 GMT
USER varnish
# Thu, 17 Oct 2024 03:24:52 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:24:52 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84d4766d611be78854d8bfad7378b9072ecbe3ade1457862137470ce22557a`  
		Last Modified: Thu, 17 Oct 2024 03:29:28 GMT  
		Size: 104.8 MB (104796961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826c5b5ed72493c005e765ea9fe73a61c14e57cb1ca901e9caafd0a4010793c9`  
		Last Modified: Thu, 17 Oct 2024 03:29:10 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f551de2aa30e84f97b1573542aa0647fcecd2da21329b0ce70cb86cffcdd2de`  
		Last Modified: Thu, 17 Oct 2024 03:29:10 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:a6ec5d891316fa5d9a7de24ce870da964ef4c2fa4ee44b395f7d67170fde681d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112580334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236aaceab22f4762ec0de9bbfcef5865a636024ce50e501f67041974f02a6dc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:52:07 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_VERSION=7.6.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Thu, 17 Oct 2024 03:52:07 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Thu, 17 Oct 2024 03:52:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:52:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:52:08 GMT
ENV VSM_NOPID=1
# Thu, 17 Oct 2024 03:54:39 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:54:42 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:54:42 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:54:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:54:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:54:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:54:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:54:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40600a7c357ca6c02d49abca4f445d2a67e0f817e8924a4bbc3dbc0ab1c07a8c`  
		Last Modified: Thu, 17 Oct 2024 03:58:35 GMT  
		Size: 85.1 MB (85088239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9308896b060d89adc522b31775c270cc70aed098d14753b9f0d1d1adf9b33b`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715abd33b2fc67e17eeb2b082afb3c4d1233b5432aac4c5f07735d030f32a7cc`  
		Last Modified: Thu, 17 Oct 2024 03:58:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old`

```console
$ docker pull varnish@sha256:6d19633286d18b65c951f0a6d9502585f8a571e76793972be397863dc12cae49
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
$ docker pull varnish@sha256:11453f7b435794761ad123289f68f13370b0e8f89a4bb3ba69ac3bf5c75e143a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134863533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aee31c556044c78e0318034656db8ed1fcfbc6f9ea30938ca8b1b26e0dbda34`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:54:12 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 27 Sep 2024 07:54:12 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 27 Sep 2024 07:54:12 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 27 Sep 2024 07:54:12 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 27 Sep 2024 07:54:12 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 27 Sep 2024 07:54:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 27 Sep 2024 07:54:13 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 27 Sep 2024 07:54:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 27 Sep 2024 07:54:13 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:54:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:54:13 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:56:44 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:56:45 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:56:45 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:56:45 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:56:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:56:45 GMT
USER varnish
# Fri, 27 Sep 2024 07:56:45 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:56:45 GMT
CMD []
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02a4e7c021f6492d9c50acb1c2f4f452e153374cfd1e6af5c5505d5d6988c53`  
		Last Modified: Fri, 27 Sep 2024 07:59:38 GMT  
		Size: 105.7 MB (105735245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19e64bf76c53681a32ce126ba90e08e913ca9bf5ec55b5cb8c2e33e951a4186`  
		Last Modified: Fri, 27 Sep 2024 07:59:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4ca367263950790d54ff31a9c62fc9d4afa281d7aa62662a0ead97e4fd4b0f`  
		Last Modified: Fri, 27 Sep 2024 07:59:24 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a956b30e5790720816bd60aecd9f624a288de8f0b240396b6265555be223691f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105118345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f611b80cb071073c0af049ffebf1e69145dcac306b44a17d879a8d96406bba60`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:23:32 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 27 Sep 2024 07:23:32 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 27 Sep 2024 07:23:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 27 Sep 2024 07:23:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:23:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:23:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:26:12 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:26:13 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:26:14 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:26:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:26:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:26:14 GMT
USER varnish
# Fri, 27 Sep 2024 07:26:14 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:26:14 GMT
CMD []
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997f1e272111508113a00d5375b210295e4f7ffc5540ba58877e2f84ea1fa05f`  
		Last Modified: Fri, 27 Sep 2024 07:29:22 GMT  
		Size: 80.4 MB (80398188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3184f278cd4c69faaef01f839fd9d45a09ff0e4dc90f10f1d518b31666dfbe5`  
		Last Modified: Fri, 27 Sep 2024 07:29:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36719d9cb8521abf6cec05d65249ca84d1ba590fea19238a6ce546061e6ba388`  
		Last Modified: Fri, 27 Sep 2024 07:29:10 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:fdec206ee6f9a0b3ab4f073474ca2f66c008afbd16909d4c09c091f7e6ddbee2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129343816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0465fb994d6a0f03c44728072de7276389b58b0c63cae0748e0d28504256e464`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:29:40 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 27 Sep 2024 07:29:40 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 27 Sep 2024 07:29:40 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 27 Sep 2024 07:29:40 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:29:40 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:29:40 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:31:51 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:31:53 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:31:53 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:31:53 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:31:53 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:31:53 GMT
USER varnish
# Fri, 27 Sep 2024 07:31:53 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:31:53 GMT
CMD []
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4e9f24eccb113f41ee75df838c443bf4f4b20a16d03f89cb3f993781bbd294`  
		Last Modified: Fri, 27 Sep 2024 07:34:29 GMT  
		Size: 100.2 MB (100185439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1890beea66eda00eba833c026dc74a50c86c0abf0b85b7b28a05301e2890717`  
		Last Modified: Fri, 27 Sep 2024 07:34:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd464ee94b50fed23a996381ae7b0ddd14eb6363e51c7b70bcb59183ac13e24`  
		Last Modified: Fri, 27 Sep 2024 07:34:18 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:90c2ce9f591d2345b6e9d96b2c99e91543e4c3941ca67a2ac8db491266cd0633
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132016871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24721978345a739069bc49d0ffd58faf7873c26fbc5b923cfeecfc5f20f5cc61`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:50:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 27 Sep 2024 07:50:46 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 27 Sep 2024 07:50:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 27 Sep 2024 07:50:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 27 Sep 2024 07:50:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Fri, 27 Sep 2024 07:50:47 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:54:08 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 27 Sep 2024 07:54:10 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:54:10 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:54:10 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 27 Sep 2024 07:54:10 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:54:10 GMT
USER varnish
# Fri, 27 Sep 2024 07:54:11 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:54:11 GMT
CMD []
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a237cbfcdd9567204336e4c4dccaed9ed3876d0420b7e0f2ea642a142175a0`  
		Last Modified: Fri, 27 Sep 2024 07:58:07 GMT  
		Size: 101.9 MB (101870642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2176053ccdf02a07e6016241368fd1c8b6b762549bb78a9571e56845c13a3c5`  
		Last Modified: Fri, 27 Sep 2024 07:57:47 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d19b56512f6b50ddd6f596875309ba1ac75d6a2a83932f928a96ebdddc0aec`  
		Last Modified: Fri, 27 Sep 2024 07:57:47 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:9da2339b7c4f5fbc3df9e284868c821c81d77f309b54db2bbc764e534516ca4d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137797884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc79a1b5a152d76ce01bae93f78e6d7ae09ac0a63dbb45ac5ce6d4eb9c825a5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:25:01 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 03:25:02 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 03:25:02 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 03:25:03 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 03:25:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 03:25:03 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:25:03 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:25:03 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:28:37 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:28:40 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:28:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:28:41 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:28:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:28:41 GMT
USER varnish
# Thu, 17 Oct 2024 03:28:41 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:28:42 GMT
CMD []
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991d76c211cf2a830615bad768d92d195caf1d6e2619b51c8eb761e653788f31`  
		Last Modified: Thu, 17 Oct 2024 03:29:58 GMT  
		Size: 104.7 MB (104673673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0aca5c509ba6f97231d47b9babaa090d823353b46b4a935003063b5ba0c3ea`  
		Last Modified: Thu, 17 Oct 2024 03:29:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9936b87d11cac7008368bb672920d65fc0b57fa32deee7ea18bc08d46e3ca0`  
		Last Modified: Thu, 17 Oct 2024 03:29:41 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:3b34914b870a2edcd4dd9a97188bbb81856632bab5c2a8995edde96f1cc02223
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112468709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507d02e4180de236b10a91c68373d0cc6e694c2846cd995591b7b9fb14990a5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:55:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Thu, 17 Oct 2024 03:55:11 GMT
ARG VARNISH_VERSION=7.5.0
# Thu, 17 Oct 2024 03:55:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Thu, 17 Oct 2024 03:55:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Thu, 17 Oct 2024 03:55:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Thu, 17 Oct 2024 03:55:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Thu, 17 Oct 2024 03:55:12 GMT
ENV VARNISH_SIZE=100M
# Thu, 17 Oct 2024 03:57:38 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Thu, 17 Oct 2024 03:57:41 GMT
WORKDIR /etc/varnish
# Thu, 17 Oct 2024 03:57:41 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:57:42 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Thu, 17 Oct 2024 03:57:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 17 Oct 2024 03:57:42 GMT
USER varnish
# Thu, 17 Oct 2024 03:57:42 GMT
EXPOSE 80 8443
# Thu, 17 Oct 2024 03:57:42 GMT
CMD []
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd94e8d5ab3de910e95edb78fdde0ea66df13e7ad9bf916690b28bafe248b6d`  
		Last Modified: Thu, 17 Oct 2024 03:58:58 GMT  
		Size: 85.0 MB (84976615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d9b29663f7a9f46b498ff8d0ec7cc98b7dbbc8fc084607283f531c314bd3ec`  
		Last Modified: Thu, 17 Oct 2024 03:58:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de3b12e1922df954d52eb1e54ca2ac9a195a03b65fc0169437b9deebc0ce263`  
		Last Modified: Thu, 17 Oct 2024 03:58:45 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:d92362a83ce30bfd76c14777917466e76ce02e5ae154d08097435d28aed181be
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
$ docker pull varnish@sha256:59c3a09fc5abfcf1e68bd38d438688b7d0c83569e0a65c816969f83c90c13273
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73215829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f0db10e5790bfe29bd8386463af42eb77b410cb236646e6cd7360a0a9cd1d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:46:47 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 02:46:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 02:46:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 02:46:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 02:46:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 02:46:48 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:48:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:48:01 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:48:01 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:48:01 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:48:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:48:01 GMT
USER varnish
# Sat, 07 Sep 2024 02:48:02 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:48:02 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d285cdda36ba02e39fb5db5899ec835cee363b7ad2b87db63f3466c8e3527e`  
		Last Modified: Sat, 07 Sep 2024 02:53:41 GMT  
		Size: 69.8 MB (69794098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c3d3db1cd5550aceec91aca8a9a5acc85970f5d33b92957a32cb32b8653f63`  
		Last Modified: Sat, 07 Sep 2024 02:53:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babcaa75a49952cbb065a2d7ac35803afdabcc27c20e4167bee80ebe34d7d2b4`  
		Last Modified: Sat, 07 Sep 2024 02:53:33 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7fa07b0786b863dc266f351943439c8aafe5c3f1b93a8ac717ba1b00c802e9c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57421050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e86e2caef22106bf8ecd12f84c635b831a9666146b0dd59490107dad72d475a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:53:17 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 06 Sep 2024 23:53:17 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 06 Sep 2024 23:53:17 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 06 Sep 2024 23:53:18 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 06 Sep 2024 23:53:18 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 06 Sep 2024 23:53:18 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 06 Sep 2024 23:53:18 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 06 Sep 2024 23:53:18 GMT
ENV VARNISH_SIZE=100M
# Fri, 06 Sep 2024 23:54:36 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 06 Sep 2024 23:54:37 GMT
WORKDIR /etc/varnish
# Fri, 06 Sep 2024 23:54:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:54:38 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 06 Sep 2024 23:54:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 06 Sep 2024 23:54:38 GMT
USER varnish
# Fri, 06 Sep 2024 23:54:38 GMT
EXPOSE 80 8443
# Fri, 06 Sep 2024 23:54:38 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41154e939d991f21ae1b190b52d812049226a428aa6bed870d4e144e9496d9c7`  
		Last Modified: Sat, 07 Sep 2024 00:00:34 GMT  
		Size: 54.5 MB (54491364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6660d44e064182554dc06b729533de25fcc0f86a3b8274bc4f1f15100ea84`  
		Last Modified: Sat, 07 Sep 2024 00:00:28 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf5f2ac481a3f8c6a07650a539c5e858231e5eff291d331151f75229b0d6216`  
		Last Modified: Sat, 07 Sep 2024 00:00:28 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a6ea3915acfc6f2cff98f8e6397b051c2f1486e0b1abffc2a9b5f4b6fcf44726
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69922870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6fa80545d0146358c54e3b460875cbe64c34292c8ec0e2a5ee4d89825e37d8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:32:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 02:32:42 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 02:32:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 02:32:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 02:32:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 02:32:43 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 02:32:43 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 02:32:43 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:33:48 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:33:48 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:33:48 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:33:48 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:33:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:33:48 GMT
USER varnish
# Sat, 07 Sep 2024 02:33:49 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:33:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7c041f1a08d6904c5fc431550f1b46f386b1e8a0a15f60420d3f1c3f8e4956`  
		Last Modified: Sat, 07 Sep 2024 02:38:29 GMT  
		Size: 66.6 MB (66561743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13493d62ebb9230283c31f2c29616815b7261d8ea5ce1fef5cee06eca895d48a`  
		Last Modified: Sat, 07 Sep 2024 02:38:23 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b528f8eb0911d23806e92337fc161ee9f7ffd889a3fc47faac4df88c1ff84d`  
		Last Modified: Sat, 07 Sep 2024 02:38:23 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:055811aff351b9a4185b26939c7b779ba64ef187e21b5c1ab3ebfae72c5dd2b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75241120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b353d90e6191bdd87206bdce7c566b1a283c71ab91f523afb89549543eb7c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:57:46 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 01:57:46 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 01:57:47 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 01:57:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 01:57:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 01:57:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 01:57:47 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 01:59:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 01:59:50 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 01:59:50 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 01:59:51 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 01:59:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 01:59:51 GMT
USER varnish
# Sat, 07 Sep 2024 01:59:51 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 01:59:51 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60754c4db0c99b69e16cf7a780fe7598d9436a865cac09ee645434b131389f24`  
		Last Modified: Sat, 07 Sep 2024 02:06:53 GMT  
		Size: 72.0 MB (71985490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f0f44ea3af290ddd37e769969c21b165b3cefc3b2b6b6f2987ffe285c643c3`  
		Last Modified: Sat, 07 Sep 2024 02:06:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ecb4e83c13f39bf24e6f0249ae24efc4a9b03f78fb80807592920214edf0d3`  
		Last Modified: Sat, 07 Sep 2024 02:06:41 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:aa76e10acc20b1fb7084f61677fc684cfed97b7af8517311b64343a792ef2ce4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70745749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288e480738fe2b36328c2abf2943fa9a47d7ca87a45ccd079f4024dc985cad78`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:59:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 07 Sep 2024 01:59:43 GMT
ARG VARNISH_VERSION=7.5.0
# Sat, 07 Sep 2024 01:59:43 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Sat, 07 Sep 2024 01:59:43 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Sat, 07 Sep 2024 01:59:44 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Sat, 07 Sep 2024 01:59:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 07 Sep 2024 01:59:45 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Sat, 07 Sep 2024 01:59:45 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Sat, 07 Sep 2024 01:59:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Sat, 07 Sep 2024 01:59:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 07 Sep 2024 01:59:46 GMT
ENV VARNISH_SIZE=100M
# Sat, 07 Sep 2024 02:01:10 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Sat, 07 Sep 2024 02:01:13 GMT
WORKDIR /etc/varnish
# Sat, 07 Sep 2024 02:01:13 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 07 Sep 2024 02:01:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Sat, 07 Sep 2024 02:01:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 07 Sep 2024 02:01:14 GMT
USER varnish
# Sat, 07 Sep 2024 02:01:15 GMT
EXPOSE 80 8443
# Sat, 07 Sep 2024 02:01:15 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3498df33b2a1081026de1cfb84850fe2c222aab212e52e98eab4ff6476b50b3b`  
		Last Modified: Sat, 07 Sep 2024 02:06:57 GMT  
		Size: 67.4 MB (67379260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff4a12d0055dfaf864b93acd92e976c57dd6f419497e874f975fb708b18d9f2`  
		Last Modified: Sat, 07 Sep 2024 02:06:47 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a34c42ae7729aeb3a5fdb84562bf98b976005e144797c0774ee4dde3c9ba29`  
		Last Modified: Sat, 07 Sep 2024 02:06:47 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:ebc3c7d1e6ec9e99118c774dbc40e74cbee9596bcd758b9ef0d883e5b8221676
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65126002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd6b7c87f2e0740249182cd21889878ccfc7e1ebcd9b00a210f3f696b98373a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:10:28 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_VERSION=7.5.0
# Fri, 06 Sep 2024 23:10:29 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Fri, 06 Sep 2024 23:10:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Fri, 06 Sep 2024 23:10:29 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Fri, 06 Sep 2024 23:10:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Fri, 06 Sep 2024 23:10:29 GMT
ENV VARNISH_SIZE=100M
# Fri, 06 Sep 2024 23:11:50 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Fri, 06 Sep 2024 23:11:51 GMT
WORKDIR /etc/varnish
# Fri, 06 Sep 2024 23:11:51 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:11:52 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Fri, 06 Sep 2024 23:11:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 06 Sep 2024 23:11:52 GMT
USER varnish
# Fri, 06 Sep 2024 23:11:52 GMT
EXPOSE 80 8443
# Fri, 06 Sep 2024 23:11:52 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0118bc1dbba5c82d06fdfed695d8e80e8044a23b2970f2be0b57056e8cf88c48`  
		Last Modified: Fri, 06 Sep 2024 23:17:56 GMT  
		Size: 61.9 MB (61870619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d03fb424bdb1471e62681e8eceff4cd027a748ea17df08c21c4e3e4fb13763`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72312bc2baecd766ef19ab42b9999881f9ac906a0aa00b1897913ade4e9af474`  
		Last Modified: Fri, 06 Sep 2024 23:17:49 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:bfd6cf3bc107200b6feac23071cce59ce28e910805e58f97b67280721e062c0c
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
$ docker pull varnish@sha256:672b71e5883cefd983bab2dbf3634f2cc5ee0ef341bfb33050446e5dfd4f8595
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95867078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6057c46accf738b2d68e68f5803b049689957714857a4e3270b7965b2ee098c1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:56:53 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 27 Sep 2024 07:56:53 GMT
ARG VARNISH_VERSION=6.0.13
# Fri, 27 Sep 2024 07:56:54 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Fri, 27 Sep 2024 07:56:54 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:58:40 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Fri, 27 Sep 2024 07:58:40 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:58:40 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:58:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:58:40 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:58:40 GMT
CMD []
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b6651c40c47f71c9486af005d55471e17d8a90aa852ed051a7e4ba1a3348ed`  
		Last Modified: Fri, 27 Sep 2024 07:59:56 GMT  
		Size: 64.4 MB (64437764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c046b9fb8849d1f1d68eedb3fc15fdb5469610f06a54ba908d173d8e396feb1`  
		Last Modified: Fri, 27 Sep 2024 07:59:48 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:c0e75a091223dc30da50c78da9b32dfb6ebf8a61a7fde62ac08d72c8b9e4f86e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72864140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc154e7c6bb5593ea4e110cdf1869c0059bf606d05dbeb397be19e9f36296758`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 05:14:05 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
# Fri, 27 Sep 2024 05:14:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:26:26 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 27 Sep 2024 07:26:27 GMT
ARG VARNISH_VERSION=6.0.13
# Fri, 27 Sep 2024 07:26:27 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Fri, 27 Sep 2024 07:26:27 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:28:28 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Fri, 27 Sep 2024 07:28:28 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:28:28 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:28:28 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:28:29 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:28:29 GMT
CMD []
```

-	Layers:
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7d4933da79ac1087836dc24bfb8ba8ae3e80cede005988a89d4e7d8feaf874`  
		Last Modified: Fri, 27 Sep 2024 07:29:38 GMT  
		Size: 46.3 MB (46274112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e705e915ccaa6302ee24bc00b349bdb9403be35b7a813145cbaeda347828b49a`  
		Last Modified: Fri, 27 Sep 2024 07:29:32 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f5f81da76f5e69e98006b3733a4f9082952033d459558e9fa56c8ed915c752db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89961577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d6730b0996d43d67c19836bd61d7fbebe76ff38bb1fafb246e2ea97e9e695c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:32:04 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 27 Sep 2024 07:32:04 GMT
ARG VARNISH_VERSION=6.0.13
# Fri, 27 Sep 2024 07:32:04 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Fri, 27 Sep 2024 07:32:04 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:33:35 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Fri, 27 Sep 2024 07:33:36 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:33:36 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:33:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:33:36 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:33:36 GMT
CMD []
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c11049a7bb44f1c287f63d0c337404483102a7055f33124aea5fe489ca9589`  
		Last Modified: Fri, 27 Sep 2024 07:34:46 GMT  
		Size: 59.9 MB (59885703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b81c9012312de01b188f659e443f50952e138bac1371b03dc84558f10849b7`  
		Last Modified: Fri, 27 Sep 2024 07:34:39 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:173b1de36a4d17ea1799e1bb74537b5f2fcb43312e8cbfa78dfe515479d8ab66
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97132611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4177ce3a56a71e449c2a875605082cf5ccb475126d7ebbf33fd937f9ac9e6abc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Sep 2024 07:23:23 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
# Fri, 27 Sep 2024 07:23:24 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:54:25 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Fri, 27 Sep 2024 07:54:25 GMT
ARG VARNISH_VERSION=6.0.13
# Fri, 27 Sep 2024 07:54:26 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Fri, 27 Sep 2024 07:54:26 GMT
ENV VARNISH_SIZE=100M
# Fri, 27 Sep 2024 07:56:46 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Fri, 27 Sep 2024 07:56:46 GMT
WORKDIR /etc/varnish
# Fri, 27 Sep 2024 07:56:46 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Fri, 27 Sep 2024 07:56:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 27 Sep 2024 07:56:47 GMT
EXPOSE 80 8443
# Fri, 27 Sep 2024 07:56:47 GMT
CMD []
```

-	Layers:
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de14ddae1aa0ebd1b4b6f365a428f18241ed79c7eca15ad87985885fea17625c`  
		Last Modified: Fri, 27 Sep 2024 07:58:29 GMT  
		Size: 64.7 MB (64718399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389ed122f33c9b42cd54aa8e4e994ff51e0787b7e1daa8a74d1393654a944fa0`  
		Last Modified: Fri, 27 Sep 2024 07:58:17 GMT  
		Size: 713.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:053579a9edb1c0ecd98f26ada06d72fcfeb69ed1e49940c05e60e25ff5f25371
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94647026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fd07f2ef42ca87942053c400a4785380dce3bb54e606fb1d63097a8cfe068f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 04 Sep 2024 22:26:18 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Wed, 04 Sep 2024 22:26:20 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:27:32 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Wed, 04 Sep 2024 23:27:33 GMT
ARG VARNISH_VERSION=6.0.13
# Wed, 04 Sep 2024 23:27:34 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Wed, 04 Sep 2024 23:27:34 GMT
ENV VARNISH_SIZE=100M
# Wed, 04 Sep 2024 23:30:49 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Wed, 04 Sep 2024 23:30:51 GMT
WORKDIR /etc/varnish
# Wed, 04 Sep 2024 23:30:52 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Wed, 04 Sep 2024 23:30:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 04 Sep 2024 23:30:52 GMT
EXPOSE 80 8443
# Wed, 04 Sep 2024 23:30:53 GMT
CMD []
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ad53399901533b0371d62560f54aaa95448a92fa2cc0e637b23440ebec222b`  
		Last Modified: Wed, 04 Sep 2024 23:44:07 GMT  
		Size: 59.3 MB (59347035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4eb9dcfc226e07bc3c4fa4ab30656eda5ab65803c658f6082bccdd1e5edfac`  
		Last Modified: Wed, 04 Sep 2024 23:43:57 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:32841bc0f7503dfd6c456ad94c8f78007b3100045965cadbe18f456099ac8abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76258728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded5fdd03ff15a069138878b85906a9196b3fc3ba8c26fafc22d244e44a35304`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 04 Sep 2024 21:43:26 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Wed, 04 Sep 2024 21:43:27 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:09:00 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Thu, 05 Sep 2024 00:09:00 GMT
ARG VARNISH_VERSION=6.0.13
# Thu, 05 Sep 2024 00:09:01 GMT
ARG DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703
# Thu, 05 Sep 2024 00:09:01 GMT
ENV VARNISH_SIZE=100M
# Thu, 05 Sep 2024 00:10:22 GMT
# ARGS: DIST_SHA512=3bdb4f04bdb22789ebe04a1e57dc814a7d7e642456cce2696f7e05fe557a277f18d5dc4a2df22a27fa9445447af3356ebdb3c5d63c01bb32d9bff7881aa8a703 PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.13
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 05 Sep 2024 00:10:23 GMT
WORKDIR /etc/varnish
# Thu, 05 Sep 2024 00:10:23 GMT
COPY dir:70ca6de1505e99367a417b2ec0c091d5e6d2379f760be9da7079e2cd535138e2 in /usr/local/bin/ 
# Thu, 05 Sep 2024 00:10:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 05 Sep 2024 00:10:23 GMT
EXPOSE 80 8443
# Thu, 05 Sep 2024 00:10:23 GMT
CMD []
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea184e408ee8a3bda0cdce477eb9806a10f7582bd36e0d18c1a36e645d4a8524`  
		Last Modified: Thu, 05 Sep 2024 00:17:59 GMT  
		Size: 46.6 MB (46594565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce81c8f7a8af9c632886d9382a8489c48b529c3a16f50cd485b6cd0cc3a2a19`  
		Last Modified: Thu, 05 Sep 2024 00:17:53 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
